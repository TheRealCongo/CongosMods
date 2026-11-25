# CongosMods wiki

The source for the public mod wiki at https://therealcongo.github.io/CongosMods/.
This repo only holds wiki pages and images. **No mod source code goes here.**

## After a Workshop update

Open Claude Code in this repo and say what you published (for example "I published Congo's Map Symbols 1.3.0"), or type `/wiki-update`. Claude gathers the changes from the mod's repo and Workshop page, drafts the wiki edits, and shows you a proposal with a preview. Nothing goes live until you approve it. Then it merges through a PR and the site republishes.

## Editing a page by hand

`main` is protected, so every change goes through a pull request:

1. Open the file under `docs/` on GitHub and click the pencil icon. Each page on the live wiki also has an edit button.
2. When you save, choose **Create a new branch and start a pull request**.
3. Once the **Build check** passes, merge the PR. The site rebuilds automatically in about a minute. You can watch it in the **Actions** tab.

Mod pages start with a small front-matter block (`repo`, `workshop_id`, `version`, `updated`, `documented_commit`). It isn't shown on the site, and it tells `/wiki-update` what's already documented. Keep it when editing.

## Adding a mod page

1. Copy `docs/mods/example-mod.md` to `docs/mods/<new-mod>.md` and fill it in.
2. Add it to the `nav:` list in `mkdocs.yml` and to the tables in `docs/index.md` and `docs/mods/index.md`.
3. Put screenshots in `docs/assets/images/`.

## Cheat sheet

| Want | Write |
|------|-------|
| Image | `![alt text](../assets/images/file.png)` |
| Smaller image | `![alt text](../assets/images/file.png){ width="400" }` |
| Table | `\| A \| B \|` rows, with a `\|---\|---\|` line under the header |
| Note box | `!!! note` then the text indented 4 spaces |
| Warning box | `!!! warning` |
| Collapsible box | `??? info "Title"` |
| YouTube video | Copy the `<div class="video">` block from `example-mod.md` and change the video ID |

## Previewing locally (optional)

```
pip install -r requirements.txt
mkdocs serve
```

Then open http://127.0.0.1:8000/CongosMods/.

## One-time GitHub setup

Repo **Settings → Pages → Source: GitHub Actions**.
