---
name: wiki-update
description: Update the public CongosMods wiki after a mod update is published to the Arma Reforger Workshop (or to add a new mod's page). Gathers what changed from the mod's private repo and Workshop page, drafts the wiki edits, and shows the user a proposal. Nothing is pushed until the user approves that specific proposal; then the change merges into main through a short-lived PR and the site republishes. Use when the user says they published, released or updated a mod, asks to update or add to the wiki, or types /wiki-update.
---

# /wiki-update

The wiki at https://therealcongo.github.io/CongosMods/ is built from this repo (`TheRealCongo/CongosMods`, public). The mods themselves live in **private** repos under `TheRealCongo`. This workflow is the same on every machine: never use machine-named branches (Laptop, Desktop) here.

## Golden rules

1. **Propose first, push never without approval.** Draft everything locally, show the proposal, and stop. Commit, push and merge only after the user approves *this* proposal in chat ("approved", "looks good, merge it" and so on). Approval of an earlier proposal does not carry over. If they ask for changes, revise and show the proposal again.
2. **The wiki is public and the mod repos are private.** Copy only player- and server-admin-facing facts into the wiki: features, items, settings, compatibility, known issues, changelog entries. Never copy source code, script or class names that aren't meant for players, internal file paths, internal docs (handoffs, roadmaps, drafts, decision records, session notes, advertising plans), unreleased or planned features, credentials, server IPs, or anything from `draft/`, `test/` or `tools/`. When unsure whether something is public, leave it out and list it under "Left out — confirm?" in the proposal.
3. **Don't invent.** If a fact isn't in the sources, ask the user or mark it `TODO` in the proposal. Never make up version numbers, dates, item stats or screenshots.

## Steps

### 1. Pin down what was published
Get from the user, or work out: **which mod(s)**, the **new version**, and the **publish date** (default: today). If several mods were updated, handle them in one proposal.

### 2. Get a clean working copy
- Work in a local clone of `TheRealCongo/CongosMods` (clone it if needed with `gh repo clone`).
- `git fetch origin`, then create `wiki/<mod-slug>-<version>` from `origin/main` (for several mods: `wiki/update-<YYYY-MM-DD>`).
- Never edit `main` directly. It is protected and pushes to it are rejected.

### 3. Find the mod's page and its last documented state
Mod pages are `docs/mods/<mod-slug>.md`. Their front matter records where the page is up to:

```yaml
---
repo: TheRealCongo/CongosMapSymbols     # private source repo
workshop_id: 6A4F3EF9908A604F           # Workshop GUID (in the mod's addon.gproj)
version: 1.2.0                          # last version documented
updated: 2026-11-25                     # date of that version
documented_commit: 1a2b3c4              # mod repo commit the page was last updated against
---
```

**New mod (no page yet):** copy `docs/mods/example-mod.md` to `docs/mods/<mod-slug>.md`, and fill in the front matter (find the repo with `gh repo list TheRealCongo`, and the GUID in its `addon.gproj`). Add the page to `nav:` in `mkdocs.yml` and to the tables in `docs/index.md` and `docs/mods/index.md`.

### 4. Gather what changed
Use every source available, roughly in this order of trust:

1. **The Workshop page**, where the changelog the user typed when publishing is the public record. URL: `https://reforger.armaplatform.com/workshop/<workshop_id>-<ModName>`. If it can't be read, ask the user to paste the Workshop changelog or link.
2. **Release-notes files in the mod repo**, if there are any: `CHANGELOG.md`, `RELEASE-NOTES-*.md`, `WORKSHOP.md`, `README.md`. Read them with `gh api repos/<repo>/contents/<path>` (decode the base64), or from a local clone.
3. **Commits since the last update:** `gh api repos/<repo>/compare/<documented_commit>...HEAD` gives the commit messages and changed files. Use these to spot player-facing changes the notes missed: new prefabs or items, new settings, UI changes. Don't paste commit messages straight in, but translate them into plain player language.
4. **The user**, for anything still unclear.

### 5. Draft the edits (locally only)
On each affected mod page:
- Front matter: `version`, `updated`, and `documented_commit` (the mod repo's HEAD SHA you compared against).
- The infobox: **Version** and **Updated**.
- **Changelog**: add a new `??? info "<version> — <date>"` entry at the **top**. Turn the previous newest entry from `???+` (open) into `???` (closed) if needed, and make the new one `???+` so it shows open.
- Update **Features**, **Items / Content**, **Server setup**, known-issue boxes, and anything else the update made out of date. Remove things the update removed.
- If the update changes how something looks, flag "screenshot may be outdated" in the proposal. Don't remove or replace images yourself unless the user gives you new ones.

Also update the version column in `docs/index.md` and `docs/mods/index.md`.

### 6. Check it builds and preview it
- `mkdocs build --strict` must pass. If `mkdocs` isn't installed, create a virtual env **outside the repo** (a temp or scratch folder) and `pip install -r requirements.txt` into it.
- Start `mkdocs serve` and open the changed pages in the browser pane, if there is one, so the user can see them rendered.

### 7. Present the proposal, then STOP
Show, in this order:
1. **Summary:** one line per mod, like "Congo's Map Symbols 1.2.0 → 1.3.0: 3 changelog items, 1 new item, 1 server setting".
2. **What changes on the wiki:** a short bullet list per page.
3. **The diff:** `git diff` of the working tree, trimmed to the relevant hunks if it's long.
4. **Left out — confirm?:** anything you deliberately didn't publish (rule 2), and why.
5. **Open questions / TODOs:** missing facts and possibly outdated screenshots.

Then ask whether to publish it. Don't commit, push or open a PR yet.

### 8. On approval: merge and publish
Only after the user approves this proposal:
1. `git add` and `git commit` with a message like `Wiki: <Mod> <version>`.
2. `git push -u origin <branch>`
3. `gh pr create --base main --title "Wiki: <Mod> <version>" --body "<the proposal summary>"`
4. Wait for the **Build check** to pass: `gh pr checks <pr> --watch`. If it fails, fix it, show the user what changed, and re-check.
5. `gh pr merge <pr> --squash --delete-branch`
6. Watch the **Publish wiki** run on `main` (`gh run list` / `gh run watch`), then open the live page and confirm it shows the new version.
7. Report: the PR link, the live page URL, and anything left as a TODO.

## Repo protections (for reference)
- `main` requires a pull request and a passing **Build check**, applies to admins too, and blocks force-pushes and deletion. So every change, including from collaborators, goes through a PR.
- The repo's built-in GitHub Wiki tab is turned off. The site is the only wiki.
- Pull requests from strangers can't merge without a maintainer, so the public can suggest changes but not make them.
