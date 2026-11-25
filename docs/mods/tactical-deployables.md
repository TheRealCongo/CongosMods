---
repo: TheRealCongo/Tactical-Deployables   # private source repo
workshop_id: 6AAB37A58353B0BE             # Workshop GUID (from the mod's addon.gproj)
version: 0.10.0                           # last version documented on this page
updated: 2026-11-06                       # date of that version
documented_commit: ae2838c                # baseline commit the day before 0.10.0; documented from the published 0.10.0 package
---

# Tactical Deployables

<div class="infobox" markdown>
![Tactical Deployables thumbnail](../assets/images/placeholder-screenshot.svg)

| | |
|---|---|
| **Version** | 0.10.0 |
| **Updated** | 2026-11-06 |
| **Author** | Congo |
| **Game version** | 1.9.0.37 |
| **Dependencies** | None (base game only) |
| **Workshop** | [Congos Tactical Deployables](https://reforger.armaplatform.com/workshop/6AAB37A58353B0BE-CongosTacticalDeployables) |
</div>

**Tactical Deployables** adds field gear that you carry, set up and pack away again: a sniper tripod and spotting scope with a laser rangefinder, a mast antenna that extends radio range, camo nets for vehicles, engineer tape, trip flares, chemlights and marker panels.

## What's in it

- [**STAK Case**](#stak-sniper-tripod-advanced-kit): a tripod for your rifle, or a spotting scope stand
- [**M151 Spotting Scope**](#m151-spotting-scope-and-storm-rangefinder): 12–40× scope with a mil reticle
- [**STORM SLX Rangefinder**](#m151-spotting-scope-and-storm-rangefinder): laser range readout on the M151
- [**OE-254 Antenna Kit**](#oe-254-antenna): triples radio range near the mast
- [**Vehicle Camo Net Kit**](#camo-net-hides): a camo net hide over a vehicle (US, Soviet, FIA)
- [**Steel Picket**](#steel-pickets-and-engineer-tape): stake for tape, trip flares and chemlights
- [**Engineer Tape**](#steel-pickets-and-engineer-tape): marks and blocks a line on foot
- [**Trip Flare**](#trip-flares): fires a signal star when someone crosses its wire
- [**Chemlights**](#chemlights): blue, green, red, yellow and IR light sticks, single or in boxes of 10
- [**VS-17 Marker Panel**](#vs-17-marker-panel): orange day side, pink night side

## Getting the gear

Everything is in the **Equipment** category of the US, USSR and FIA arsenals. Each faction's camo net kit is only in its own faction's arsenal.

| Item | Arsenals | Cost | Weight | Carried |
|---|---|---|---|---|
| STAK Case | US, USSR, FIA | 15 | 5 kg | Inventory |
| M151 Spotting Scope | US, USSR, FIA | 15 | 1.6 kg | Binocular slot |
| STORM SLX Rangefinder | US, USSR, FIA | 10 | 0.4 kg | Inventory |
| OE-254 Antenna Kit | US, USSR, FIA | 25 | 13 kg | Backpack slot |
| Vehicle Camo Net Kit (US / Soviet / FIA) | Own faction | 10 | 15 kg | Inventory, or vehicle storage |
| Steel Picket | US, USSR, FIA | 1 | 2.26 kg | Inventory |
| Engineer Tape (white) | US, USSR, FIA | 2 | 0.4 kg | Inventory |
| Trip Flare | US, USSR, FIA | 3 | 0.5 kg | Inventory |
| Chemlight (each colour) | US, USSR, FIA | 1 | 0.03 kg | Grenade slot |
| Chemlight Box (10) | US, USSR, FIA | 5 | 0.1 kg | Inventory |
| VS-17 Marker Panel | US, USSR, FIA | 2 | 0.6 kg | Inventory |

## STAK (Sniper Tripod Advanced Kit)

The STAK comes in a hard case. Set it up as a **rifle STAK** for your own rifle, or as a **spotter tripod** with the M151 scope.

### Set up and pack away

1. Put the case on the ground.
2. Hold **Deploy Rifle STAK** or **Deploy Spotter Scope** (5 s). The tripod stands where the case lay, facing the way you face, and the case lies open beside it.
3. To pack it, hold **Pack Rifle STAK** or **Pack Spotter Scope** on the case (5 s). Nobody can be on it, and the rifle has to come off first.

The scope and STORM stay with the case: pack a spotter tripod and the next set-up comes back with the same parts.

### Height

Hold **Adjust height** on the tripod and turn the **mouse wheel** (2.5 cm a step). The label shows the height. Your pose follows it:

| Height | Legs | You shoot |
|---|---|---|
| 24 – 42 cm | Splayed wide | Prone |
| 48 – 63 cm | Middle | Kneeling |
| 64 cm and up | Upright | Standing (rifle STAK up to 115 cm, spotter up to 147 cm) |

Nobody can be on it while you change the height.

### Rifle STAK

1. Hold your rifle, sniper rifle or machine gun (modded ones too).
2. Use **Mount rifle** on the empty STAK (at 115 cm or lower). Your rifle goes onto the mount with its attachments and the rounds in its magazine, and your spare magazines that fit move into the STAK so you can reload from it.
3. Get on the gunner seat and shoot. **Right mouse** aims through the rifle's own optic or iron sights; the usual magnification keys work.
4. Use **Take rifle** to get your rifle back with the rounds it has left, plus your remaining magazines.

| Position | Traverse | Elevation |
|---|---|---|
| Standing or kneeling | 45° each side | −25° to +10° |
| Prone | 20° each side | −10° to +15° |

### Spotter tripod

- Get on the seat, then **right mouse** opens the scope view: the mouse turns the tripod, the wheel zooms, and holding **left mouse** ranges (with a STORM fitted). **X** gets you off.
- **Mount scope** puts an M151 from your hands or inventory on the tripod (with its STORM, if fitted). **Take scope** takes it back off.

## M151 Spotting Scope and STORM Rangefinder

### Using the scope by hand

| Do | Key |
|---|---|
| Take it out | <kbd>B</kbd> |
| Raise it to your eye | Right mouse |
| Zoom | Mouse wheel |
| Range (with a STORM fitted) | Hold left mouse |
| Lower it | <kbd>X</kbd> |
| Fit or remove the STORM | Hold <kbd>R</kbd> (inspect), then **Attach STORM SLX** / **Detach STORM SLX** |

You can't walk while looking through it, and it sways less the lower you are (prone is steadiest). For a steady view, put it on the STAK.

### Reading the reticle

- Zoom runs from **12×** to **40×**; the current zoom shows bottom right.
- The reticle is in **mils** and stays true at every zoom.
- Long ticks every 1 mil, short ticks at the half mils, and fine 0.2-mil marks near the ends of the side and bottom arms.
- The arms reach 6 mils left and right, 8 up and 11 down.

!!! tip "Range by mils"
    **Height ÷ mils × 1000 = range.** A 2 m tall target that spans 4 mils is 2 ÷ 4 × 1000 = **500 m** away. The formula is printed in the scope view.

### STORM SLX

Fit it to the M151's rail: **Use** it from your inventory, or hold **R** with the scope in hand and **Attach STORM SLX**.

Then hold **left mouse** while looking through the scope. After half a second it reads the range, and keeps updating while you hold:

| Readout | Means |
|---|---|
| `RNG 1234 m` | The range to the first thing in your crosshair |
| `RNG . . .` | Still ranging |
| `RNG ---- m` | Nothing hit within 5000 m |

## OE-254 Antenna

1. Wear the **OE-254 Antenna Kit** on your back, then drop it.
2. Hold **Erect antenna** on the bag (10 s). A 12.7 m mast goes up, straight up on any slope, with stakes, guy lines and a coax run. The bag lies open at its base.
3. Hold **Take down antenna** on the bag to pack it (10 s).

**What it does:** like a relay station, with nothing to switch on. Any player standing within their radio's normal range of the mast **transmits three times as far**. Walk out of that range and the radio is back to normal within a second.

- It boosts **every** player near the mast, on either side.
- Several masts don't stack.
- It only changes radios carried by players, not vehicle radios or radio stations.
- The mast can be destroyed. Destroying it or taking it down ends the boost.

## Camo Net Hides

There are US, Soviet and FIA nets, each with its own pattern, in three sizes. The right size is picked for the vehicle.

### Deploy and stow

- **From the ground:** put the kit within 8 m of the vehicle and hold **Deploy camo net over vehicle** (10 s). It nets the closest vehicle.
- **From the vehicle's storage:** keep the kit in the vehicle, select it in the inventory and press **Use**. Stay put for 10 seconds while the net goes up.
- **Stow:** hold **Stow camo net** at the back wall of the net (8 s). The kit lands at your feet.

The net is **open at the front**, so the crew can drive in and out and shoot from under it.

| Net | Clear space (W × H × L) | Fits vehicles up to (W / H / L) | For example |
|---|---|---|---|
| Small | 3.6 × 2.3 × 5.0 m | 2.6 / 3.3 / 6.5 m | A car or light truck |
| Medium | 4.2 × 3.0 × 7.6 m | 3.2 / 4.0 / 9.1 m | A truck or APC |
| Large | 4.8 × 3.6 × 10.0 m | 3.8 / 4.6 / 11.5 m | A large truck or tank |

??? question "Why won't it deploy?"
    | Message | Fix |
    |---|---|
    | No vehicle close enough | Move the kit within 8 m of the vehicle |
    | Vehicle is moving | Stop the vehicle |
    | Vehicle too large for a net | It's bigger than the large net |
    | Vehicle already netted | It already has one |
    | Vehicle is destroyed | — |
    | You moved away / Too far from the vehicle | Stay where you started while it goes up |

## Steel Pickets and Engineer Tape

### Pickets

Take a **Steel Picket** in your hand and place it to drive it into the ground (straight down on any slope). Pickets hold **engineer tape**, **trip flares** and **chemlights**. Take the tape, trip flare or tripwire off before pulling a picket back up.

### Running tape

You need a roll of **Engineer Tape** in your inventory. One roll holds **60 m**, and one stretch between pickets can be up to **25 m**.

1. On the first picket: **Start engineer tape here** (2 s).
2. On the next: **Run engineer tape to here** (3 s). Repeat to keep going.
3. On the last: **Tie off engineer tape here (finish)** (3 s), or **Cut engineer tape here** to stop.
4. To take it down: **Remove engineer tape** on a picket removes every stretch tied to it.

**What it stops:** tape blocks people **on foot**, standing, crouched or prone. Bullets pass through, and a moving vehicle tears straight through it. Pulling up or knocking over a picket drops the tape on that stretch.

## Trip Flares

1. Plant two **Steel Pickets** 1 to 12 m apart.
2. On the first: **Set trip flare** (4 s), with a Trip Flare in your inventory. You now carry its tripwire.
3. On the second: **Tie off tripwire here (arms the flare)** (3 s).
4. **3 seconds later it's live.** That includes for you.

**Anyone** who walks through the wire (it's 15 cm off the ground) or drives a vehicle across it sets it off. Jumping over it works. It fires a **white signal star** into the sky and burns bright on the ground for **a minute**, lighting about 70 m around.

- **Disarm trip flare** (4 s) at its picket takes it back. Anyone can disarm it.
- **Remove spent trip flare** clears a used one.
- A dropped tripwire can be picked up with **Pick up loose tripwire**.
- Pull up the far picket and the flare goes back to unarmed.

## Chemlights

Blue, green, red, yellow and **IR**, single or in boxes of 10. They burn for **one hour** and build up to full brightness over a few seconds.

### Cracking and placing

| Do | How |
|---|---|
| Crack it in your hand | Equip it, press <kbd>R</kbd> |
| Crack it and drop it at your feet | Hold <kbd>R</kbd> |
| Crack it in your inventory | **Use** |
| Place it on the ground, a wall or a tree | Place it from the inventory (it cracks as you place it) |
| Crack one lying on the ground | **Crack chemlight** |
| Hang one on a picket | **Hang chemlight** on the picket (uses a wrapped one first) |
| Open a box | In your hand: <kbd>R</kbd>. On the ground: **Open box (take 10 chemlights)** |

### IR chemlights

The IR chemlight's glow only shows to players **looking through night vision**: night-vision sights on weapons and vehicles (vanilla included), and night-vision goggles from NVG mods.

## VS-17 Marker Panel

Take the panel in your hand and place it to lay it out. Press <kbd>V</kbd> while placing to flip the side:

| Side | For |
|---|---|
| **Orange** | Day |
| **Pink** | Night: it shows bright to players looking through night vision |

Picking it up folds it back into its pouch.

## Controls

| Where | Do | Mouse and keyboard | Controller |
|---|---|---|---|
| M151 scope view | Look around | Mouse | Right stick |
| M151 scope view | Zoom | Mouse wheel | — |
| M151 scope view | Range (STORM) | Hold left mouse | <kbd>X</kbd> |
| M151 scope view | Step back / get off | <kbd>X</kbd> | <kbd>B</kbd> |
| M151 in hand | Take out / raise | <kbd>B</kbd>, then right mouse | — |
| STAK | Adjust height | Hold the action + mouse wheel | — |
| Chemlight | Crack / crack and drop | <kbd>R</kbd> / hold <kbd>R</kbd> | — |
| VS-17 | Flip side while placing | <kbd>V</kbd> | D-pad left |

## Game Master

These can be placed from Game Master:

| Entry | Factions |
|---|---|
| Camo Net Hide, Small / Medium / Large | US, Soviet and FIA, each under its own faction filter |
| Rifle STAK (set up) | All |
| Spotter Scope Tripod (M151 + STORM) | All |
| OE-254 Antenna (erected) | All |
| Steel Picket, Engineer Tape (white), Trip Flare, VS-17 Marker Panel | All |
| Chemlight and Chemlight Box (10), each colour | All |

- A placed **rifle STAK** or **spotter tripod** has no case, so players can't pack it.
- A placed **OE-254** has no bag, so only a Game Master can remove it.
- A placed camo net stows into its faction's kit.

## Compatibility

- **Modded rifles** work on the rifle STAK, with their optics and attachments.
- **NVG mods:** IR chemlights and the VS-17 night side show through night vision from the game's own sights and from several popular NVG mods. None of them is required.
- **Radio mods:** the OE-254 boosts radios built on the game's own radio system.

## Server setup

Add the mod to your server config's mod list:

```json
{
  "modId": "6AAB37A58353B0BE",
  "name": "Congos Tactical Deployables"
}
```

There are no server or Game Master settings.

## Changelog

???+ info "0.10.0 — 2026-11-06"
    Updated for Arma Reforger 1.9.

    **Animations**

    - New animations for unwrapping and cracking a chemlight and opening a chemlight box.
    - New animation when putting tape, a trip flare or a chemlight on a picket.

    **Chemlights**

    - Chemlight boxes can now be opened in your hands.
    - Cracked chemlights now build up to full brightness over a few seconds.
    - The glow now stays visible at longer range.
    - Cleaner glow colours.
    - IR chemlights and the VS-17 night side now also show through night vision sights.
    - Fixed missing material errors on cracked chemlights.

    **OE-254 Antenna**

    - Now works like a relay station with nothing to switch on. Once it stands, players within their radio's normal range of the mast transmit three times as far.

    **Other**

    - Script cleanup to reduce the mod's load on game start-up.

??? info "0.9.1 — 2026-10-30"
    - The spotter scope now shows its reticle.
    - The STAK works better with modded weapons.

??? info "0.9.0 — 2026-10-30"
    - First Workshop release.
