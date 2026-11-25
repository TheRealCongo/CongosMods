---
repo: TheRealCongo/Tactical-Graphics  # private source repo
workshop_id: 6A4F3EF9908A604F         # Workshop GUID (from the mod's addon.gproj)
version: 3.1.0                        # last version documented on this page
updated: 2026-11-17                   # date of that version
documented_commit: 9fa488c            # update-1.9 branch head; 3.1.0 was documented from the published package
---

# Tactical Graphics

<div class="infobox" markdown>
![Tactical Graphics](../assets/images/tactical-graphics/thumbnail.jpg)

| | |
|---|---|
| **Version** | 3.1.0 |
| **Updated** | 2026-11-17 |
| **Author** | Congo |
| **Game version** | 1.9.0.37 |
| **Dependencies** | None (base game only) |
| **Works with** | [Squad Composition](squad-composition.md) |
| **Workshop** | [Congos Tactical Graphics](https://reforger.armaplatform.com/workshop/6A4F3EF9908A604F-CongosTacticalGraphics) |
</div>

**Tactical Graphics** turns the Arma Reforger map into a full planning workspace. Draw APP-6 / MIL-STD-2525 graphics, share them with your faction, brief them on a TV or sand table, and pass fire-support requests with ready-made scratch pads.

!!! info "Squads moved to Squad Composition"
    Since 3.1.0, fire teams, roles, Sections, the compass HUD, name tag colours and the <kbd>~</kbd> order wheel live in [Squad Composition](squad-composition.md). With both loaded, Tactical Graphics' roster and map dots show Squad Composition's team colours and role icons.

## Quick start

1. Open your map (<kbd>M</kbd>). The Tactical Graphics workspace opens over it.
2. Pick a **category** tab along the top, then a **tool** in the GRAPHICS pane on the right.
3. **Click the map** to place it. Lines and areas take several clicks; press <kbd>Enter</kbd> to finish.
4. Press <kbd>Ctrl</kbd>+<kbd>S</kbd> to **save**: your graphics are shared with your faction.

!!! tip "Find anything fast"
    Type in **SEARCH** on the right: a name, part of one, or a code like `CKP`, `FSCL`, `R3P` or `SBF`. Add an echelon word ("mortar platoon", "recon company") to set it too.

## The workspace

| Where | What it is |
|---|---|
| **Top bar** | **SCRATCH PAD** and **GRAPHICS** (show or hide each pane), the eight **category** tabs, and readouts for **TIME**, **GRAPHICS** (how many you can see) and **PLAYERS** |
| **Left pane: SCRATCH PAD** | Your **GROUPS** roster and the **9-LINE**, **5-LINE**, **CFF** and **MEDEVAC** pads |
| **Right pane: GRAPHICS** | **SEARCH**, the tool gallery, the graphic's name and settings, sharing, colour, fill, and saved layouts |
| **Bottom bar** | **NEW**, **SELECT**, **UNDO POINT**, **SAVE**, **CANCEL**, **DELETE**, **REFRESH**, **LOCKED**/**UNLOCKED**, **RESET UI**, the 8-digit cursor grid, the game's map tools, **OVERLAYS** and the settings gear |

- **Move panes:** click **LOCKED** to unlock, then drag a pane by its header or resize it from the corner. **RESET UI** puts them back.
- **Hide a pane:** right-click its header.
- The **sync chip** reads **SYNCHRONIZED**: green when your map matches the server, red when something isn't shared yet.

## Categories

| Tab | Category | Holds |
|:---:|---|---|
| ![Unit](../assets/images/tactical-graphics/tab-unit.png){ .piece-icon } | **Unit** | 31 unit symbols with affiliation, echelon, designation and higher HQ |
| ![Maneuver](../assets/images/tactical-graphics/tab-maneuver.png){ .piece-icon } | **Maneuver** | Lines, axes and attacks, positions, objectives, OP/FO, LZ and PZ |
| ![Tasks](../assets/images/tactical-graphics/tab-tasks.png){ .piece-icon } | **Tasks** | 23 mission tasks with their APP-6 letters |
| ![Obstacles](../assets/images/tactical-graphics/tab-obstacle.png){ .piece-icon } | **Obstacles** | Minefields, belts, zones, wire, ditches, trenches, mines |
| ![C2](../assets/images/tactical-graphics/tab-control.png){ .piece-icon } | **C2** | Areas of operation, boundaries, NAI and TAI, action points |
| ![Fires](../assets/images/tactical-graphics/tab-fires.png){ .piece-icon } | **Fires** | TRPs, targets, smoke, FPF and fire-support coordination measures |
| ![Airspace](../assets/images/tactical-graphics/tab-aviation.png){ .piece-icon } | **Airspace** | Air control points, corridors, routes, ROZ and FARPs |
| ![Sustainment](../assets/images/tactical-graphics/tab-sustainment.png){ .piece-icon } | **Sustainment** | Casualty collection, MEDEVAC, logistics and R3P points |

Every symbol in each category, with what it means, is in the [Symbol legend](#symbol-legend) at the bottom of this page.

## Drawing

### Placing

| Kind | How |
|---|---|
| **Point** or **unit** | One click. The next click places another |
| **Line** or **area** | Click each point, then <kbd>Enter</kbd> (or **ADD NEXT**). An area closes itself; don't click the first point again |
| **Fixed shapes** (SBF, ABF, roadblock, targets...) | Finish by themselves on the last click |
| **Tasks** | Two or three clicks, in the order below |

??? info "Click order for tasks"
    | Task | Letter | Clicks |
    |---|---|---|
    | Block | B | 1 – 2 the bar, 3 the end of the stem |
    | Breach point | BP | Origin, then direction |
    | Bypass | BYPASS | Origin, then direction |
    | Canalize | C | 1 – 2 the open mouth, 3 the depth |
    | Clear | CLEAR | Origin, then direction |
    | Contain | C | 1 – 2 the half circle, 3 the arrow tail (enemy side) |
    | Cover | C | 1 the unit, 2 – 3 the flank arms |
    | Delay | D | 1 arrow tip, 2 end of the shaft, 3 end of the hook |
    | Destroy | D | One point |
    | Disrupt | D | 1 – 2 the bar, 3 the long arrow tip |
    | Fix | F | 1 arrow tip, 2 tail |
    | Guard | G | As Cover |
    | Isolate | I | 1 centre, 2 where the arc starts |
    | Neutralize | N | One point |
    | Occupy | O | As Isolate |
    | Penetrate | P | 1 – 2 the bar, 3 the arrow tail |
    | Reduce | REDUCE | Origin, then direction |
    | Retain | R | As Isolate |
    | Screen | S | As Cover |
    | Secure | SECURE | Origin, then direction |
    | Seize | S | 1 the unit, 2 the objective, 3 the side the arc bows to |
    | Suppress | S | One point |
    | Withdraw | W | As Delay |

Finished graphics wait in an unsaved **batch** (up to 16). **SAVE** or <kbd>Ctrl</kbd>+<kbd>S</kbd> shares them; **CANCEL** drops them.

### Editing

1. Click **SELECT**, then click a graphic. You can click inside filled areas too.
2. Change its name, colour, fill, sharing or unit fields, or drag its points.
3. **SAVE**.

On free-shaped lines and areas, click a point to select it, then **INSERT AFTER** (adds a point), **REMOVE POINT** or **DONE POINT**.

### Delete and undo

- **Delete:** select the graphic, click **DELETE**, then click it again. Or hover it and press <kbd>Delete</kbd>.
- **Undo** (<kbd>Ctrl</kbd>+<kbd>Z</kbd>) steps back through: the last point, the last unsaved graphic, then your **last deleted graphics** (up to 20 this mission).

### Colour and fill

**LINE COLOR** has eight swatches:

| | | | |
|---|---|---|---|
| <span class="swatch" style="background:#0C45DE"></span> Blue (default) | <span class="swatch" style="background:#C81113"></span> Red | <span class="swatch" style="background:#020202"></span> Black | <span class="swatch" style="background:#0C8B1D"></span> Green |
| <span class="swatch" style="background:#E28A08"></span> Yellow | <span class="swatch" style="background:#FFFFFF"></span> White | <span class="swatch" style="background:#B12904"></span> Orange | <span class="swatch" style="background:#6425DE"></span> Purple |

**AREA FILL** (areas only): None, Light (15%, default), Medium (25%), Strong (35%).

### Unit symbols

On the **Unit** tab, pick a unit type, then set:

| Field | Options |
|---|---|
| **AFFILIATION** | Friendly (default), Hostile, Neutral, Unknown, Civilian, and the Assumed versions of each |
| **ECHELON** | Unspecified, Team, Squad, Section, Platoon (default), Company, Battalion, Regiment, Brigade, Division, Corps, Army, Army group, Theatre |
| **UNIT DESIGNATION** | Shown to the left of the symbol |
| **HIGHER HQ** | Shown to the right of the symbol |

| Affiliation | Fill |
|---|---|
| Friendly | <span class="swatch" style="background:#0C45DE"></span> Blue |
| Hostile | <span class="swatch" style="background:#C81113"></span> Red |
| Neutral | <span class="swatch" style="background:#0C8B1D"></span> Green |
| Unknown | <span class="swatch" style="background:#E28A08"></span> Yellow |
| Civilian | <span class="swatch" style="background:#6425DE"></span> Purple |

### Limits

- Up to 64 points per graphic. Names up to 80 characters of plain text. A phase line needs a name.
- Up to 1024 graphics per mission, and 128 per player.

## Sharing and who sees what

**SHARE WITH:** **Faction** (default) or **My group**.

| Who | Sees |
|---|---|
| Players | Graphics shared with their faction, plus their own group's |
| Game Masters | Every graphic of every faction |

**Layers:** Game Master graphics sit at the bottom, then leaders', then members'. When you click, the top one is picked.

| Who | Can edit or delete |
|---|---|
| Members | Their own graphics |
| Group leaders | Any graphic by their group |
| Game Masters | Everything |

Game Master graphics are view-only for players.

**Game Masters** pick the faction new graphics go to in **GM SHARE TO**, and **SEND** shares the selected graphic (or the unsaved batch) with that faction.

## Overlays

**OVERLAYS** on the bottom bar:

- **Tactical graphics** on or off.
- **By category:** turn any of the eight categories on or off.
- **Building numbers:** numbers every enterable building, the same for every player on the same map, so "building 14" means the same house to the whole team. Zoom in to see them.

### Player locations

Set on the **GROUPS** page (**Show player positions**). The Game Master's setting is the most anyone sees.

| Style | Shows |
|---|---|
| **MARKER** | Your group with name and look direction; other groups of your faction as grey rings. With Squad Composition, your group shows team colours and role icons |
| **APP-6** | The friendly APP-6 symbol of each player's group type (recon, mortar, medic...), with no names or look direction |
| **OFF** | Nothing |

## Scratch pads

Four forms on the left pane. Empty boxes show grey examples. Your notes stay on your PC for the rest of the mission.

| Pad | For |
|---|---|
| **9-LINE** | CAS: game plan, lines 1 – 9, remarks and restrictions |
| **5-LINE** | Rotary-wing CAS brief. Items marked * are mandatory readback |
| **CFF** | Call for fire: the three transmissions, corrections and end of mission |
| **MEDEVAC** | The standard 9-line MEDEVAC request |

- **PLOT** turns the grid on that line into a shared map marker: a point target, or a MEDEVAC pickup point. Use a 6, 8 or 10-digit grid (`1234 5678`). Press PLOT again to move the same marker.
- **SEND TO** sends the open pad to a **GROUP** or **PLAYER** of your faction. They get a panel on the right of their screen; <kbd>H</kbd> hides it or shows the last one again.

## Briefing TV, sand table, laser and WarBoard

### Briefing TV

A Game Master places **Briefing TV (BLUFOR)**, **(REDFOR)** or **(FIA)**.

- Use **Brief map** at the stand (close your own map first). Drag to pan, scroll to zoom, middle-click to fit the terrain.
- Everyone nearby sees your view and your cursor as a pointer on the screen, with your faction's shared graphics.
- **Brighten screen** / **Dim screen** on the power button change only your own view.

### Sand table

A Game Master places **Briefing Sandtable (BLUFOR)**, **(REDFOR)** or **(FIA)**. It starts empty.

1. Use **Brief terrain**.
2. Drag across complete 100 m grid squares, in a square area.
3. **Build** (<kbd>Q</kbd>) raises the terrain, 4× height, with your faction's graphics on it. **Clear** (<kbd>E</kbd>) empties it.

### CLight laser pointer

**CLight Laser Pointer**, in the US, USSR and FIA arsenals, and on every Briefing TV stand. Hold it like a flashlight and left-click to switch it on. Everyone sees the red dot. Point it at a briefing TV or sand table and the dot shows on it.

### WarBoard

The **WarBoard** replaces the folded paper map: open it like the map to get the workspace. Camo versions (**MARPAT**, **MCAM**, **EMR**) are in the arsenals.

## Saved layouts

Save the plan on your PC and load it again later, even on another server.

- **SAVED LAYOUT:** type a name, **SAVE LAYOUT**. Pick one from the list, **LOAD LAYOUT**.
- Up to **16 layouts**, each up to **128 graphics**. A layout saves every graphic you can see, and loading re-creates them as yours.

## Controls

Map keys are in **Settings → Congo's Mods → Tactical Graphics: keys**, all rebindable.

| Action | Keyboard | Controller |
|---|---|---|
| Save graphics | <kbd>Ctrl</kbd>+<kbd>S</kbd> | — (use **SAVE**) |
| Undo | <kbd>Ctrl</kbd>+<kbd>Z</kbd> | — (use **UNDO**) |
| Finish line or area | <kbd>Enter</kbd> | — (use **ADD NEXT**) |
| Delete hovered graphic | <kbd>Delete</kbd> | — (use **DELETE**) |
| Previous / next tab | <kbd>Q</kbd> / <kbd>E</kbd> | LB / RB |
| Previous / next tool page | <kbd>←</kbd> / <kbd>→</kbd> | D-pad left / right |
| Hide or show a received message | <kbd>H</kbd> | View + A |

On a controller, the D-pad moves between controls and across panes; a focus outline shows where you are.

## Player settings

The **gear** button on the bottom bar opens **INTERFACE**:

| Setting | Does |
|---|---|
| **Transparency** | How see-through the panes are (0 – 85%) |
| **Accent colour** | The workspace's highlight colour, with presets plus black and white |
| **Display name** | A **PREFIX** and **NAME** shown as `[PREFIX] Name` across the game |

## Game Masters

- **GM SHARE TO** and **SEND** on the GRAPHICS pane (see [Sharing](#sharing-and-who-sees-what)).
- **Enable player locations** on the GROUPS page sets the most anyone sees: MARKER, APP-6 or OFF.
- **CTG Graphics on GM Map** (in Playable Factions): tick the factions whose graphics you want on your own Game Master map.
- Place the Briefing TVs and sand tables from the editor.

## Server setup

Add the mod to your server config's mod list:

```json
{
  "modId": "6A4F3EF9908A604F",
  "name": "Congos Tactical Graphics"
}
```

The server keeps its files in the profile folder under `CongosTacticalGraphics/`.

### ServerSettings.txt

Plain `Key=value` lines, read when each mission starts.

| Key | Values | Default |
|---|---|---|
| `PlayerLocations` | `marker`, `app6` or `off` | `marker` |

A Game Master can still change it during the mission.

### Mission graphics

Faction-shared graphics are saved as they change and come back after a server restart on the same map. "My group" graphics aren't kept, and a finished match starts the next one with a clean map.

### Custom names

`PlayerNames_Config.txt` controls the display names players set: on or off, length limits, and reserved or blocked words. Servers that used BFS Custom Player Names keep their saved names. Another naming mod's names always win.

### REST export (optional)

Off by default. It lets the server send the mission's graphics to your unit's website, receive graphics from it, and optionally record the operation (player positions, health, shots, hits and kills, including player names and platform IDs; players see an "Operation recording on" notice). The server writes a full setup guide, `REST-EXPORT-SETUP.md`, beside `RestExport.json` every time it starts.

!!! warning "Performance"
    Turning the export on, especially operation recording, may affect server performance. Watch the server's FPS.

## Compatibility

- **[Squad Composition](squad-composition.md):** with both loaded, the roster and map dots show its team colours and role icons. Neither mod needs the other.
- **Other map mods** (tablets, cockpit and drone maps): they show the graphics you can see, read-only.
- **Naming mods:** their names show in Tactical Graphics, and win over its own display names.
- **Other mods** that change the map screen, map tools, paper map or player names may conflict.

## Symbol legend

Every symbol Tactical Graphics can draw, as it appears in the tool gallery, with the label it carries on the map and what it means. The drawings come straight from the mod's own drawing code; on the map they take the line colour you pick.

!!! tip "Telling look-alikes apart"
    In the gallery several symbols share a shape: the action points are all pins, many control lines are plain lines, and most areas are plain outlines. On the map they're told apart by their **map label** (CKP, LD, FSCL...). You can also type that label into **SEARCH**.

=== "Unit"

    Unit symbols use the APP-6 frame filled in the affiliation colour (friendly shown here), with a black frame and icon. Echelon, designation and higher HQ are added around the frame.

    | Symbol | Unit | What it is |
    |:---:|---|---|
    | ![Infantry](../assets/images/tactical-graphics/units/infantry.svg) | **Infantry** | Soldiers who fight on foot. |
    | ![Headquarters](../assets/images/tactical-graphics/units/headquarters.svg) | **Headquarters** | A command post or headquarters. The staff on the frame marks it as a headquarters. |
    | ![Light infantry](../assets/images/tactical-graphics/units/light-infantry.svg) | **Light infantry** | Infantry with few vehicles, moving and fighting mostly on foot. |
    | ![Airborne infantry](../assets/images/tactical-graphics/units/airborne-infantry.svg) | **Airborne infantry** | Infantry trained to arrive by parachute. |
    | ![Air assault infantry](../assets/images/tactical-graphics/units/air-assault-infantry.svg) | **Air assault infantry** | Infantry that moves into battle by helicopter. |
    | ![Mechanized infantry](../assets/images/tactical-graphics/units/mechanized-infantry.svg) | **Mechanized infantry** | Infantry mounted in armoured fighting vehicles. |
    | ![Motorized infantry](../assets/images/tactical-graphics/units/motorized-infantry.svg) | **Motorized infantry** | Infantry carried in trucks or light wheeled vehicles. |
    | ![Machine gun](../assets/images/tactical-graphics/units/machine-gun.svg) | **Machine gun** | A team or section built around machine guns. |
    | ![Grenade launcher](../assets/images/tactical-graphics/units/grenade-launcher.svg) | **Grenade launcher** | A team built around grenade launchers. |
    | ![Sniper](../assets/images/tactical-graphics/units/sniper.svg) | **Sniper** | A sniper or marksman team. |
    | ![Armor](../assets/images/tactical-graphics/units/armor.svg) | **Armor** | Tanks. |
    | ![Combined arms](../assets/images/tactical-graphics/units/combined-arms.svg) | **Combined arms** | A mixed force (infantry, armour and support) under one commander. |
    | ![Amphibious](../assets/images/tactical-graphics/units/amphibious.svg) | **Amphibious** | A unit that can operate from the water onto land. |
    | ![Reconnaissance](../assets/images/tactical-graphics/units/reconnaissance.svg) | **Reconnaissance** | Scouts finding out about the enemy and the ground. |
    | ![Mortar](../assets/images/tactical-graphics/units/mortar.svg) | **Mortar** | Mortars giving indirect fire. |
    | ![Artillery](../assets/images/tactical-graphics/units/artillery.svg) | **Artillery** | Field artillery: howitzers and guns. |
    | ![Antitank](../assets/images/tactical-graphics/units/antitank.svg) | **Antitank** | Weapons teams that kill armoured vehicles. |
    | ![Rotary-wing aviation](../assets/images/tactical-graphics/units/rotary-wing-aviation.svg) | **Rotary-wing aviation** | Helicopters. |
    | ![Fixed-wing aviation](../assets/images/tactical-graphics/units/fixed-wing-aviation.svg) | **Fixed-wing aviation** | Aircraft. |
    | ![Medical](../assets/images/tactical-graphics/units/medical.svg) | **Medical** | Medics, an aid station or a medical unit. |
    | ![Supply](../assets/images/tactical-graphics/units/supply.svg) | **Supply** | Logistics bringing ammunition, fuel and supplies. |
    | ![Transportation](../assets/images/tactical-graphics/units/transportation.svg) | **Transportation** | Trucks and motor transport. |
    | ![Maintenance](../assets/images/tactical-graphics/units/maintenance.svg) | **Maintenance** | Repair and recovery of vehicles and equipment. |
    | ![Signal](../assets/images/tactical-graphics/units/signal.svg) | **Signal** | Communications. |
    | ![Radio relay](../assets/images/tactical-graphics/units/radio-relay.svg) | **Radio relay** | A retransmission station that extends radio range. |
    | ![Engineer](../assets/images/tactical-graphics/units/engineer.svg) | **Engineer** | Engineers: obstacles, breaching, bridging and building. |
    | ![Air defense](../assets/images/tactical-graphics/units/air-defense.svg) | **Air defense** | Anti-aircraft weapons. |
    | ![CBRN](../assets/images/tactical-graphics/units/cbrn.svg) | **CBRN** | Chemical, biological, radiological and nuclear defence and decontamination. |
    | ![Military police](../assets/images/tactical-graphics/units/military-police.svg) | **Military police** | Military police: traffic control, security and detainees. |
    | ![EOD](../assets/images/tactical-graphics/units/eod.svg) | **EOD** | Explosive ordnance disposal: clears bombs, mines and IEDs. |
    | ![UAS](../assets/images/tactical-graphics/units/uas.svg) | **UAS** | Drones (unmanned aircraft) and their operators. |

=== "Maneuver"

    | Symbol | Graphic | Map label | What it means |
    |:---:|---|---|---|
    | ![Line](../assets/images/tactical-graphics/symbols/line.svg){ width="96" } | **Line** | Name only | A plain line, for anything you need to mark that has no special symbol. |
    | ![Curved route](../assets/images/tactical-graphics/symbols/curved-route.svg){ width="96" } | **Curved route** | Name only | A route drawn as a smooth curve: a road move, a patrol route or a path to follow. |
    | ![Direction of attack](../assets/images/tactical-graphics/symbols/direction-of-attack.svg){ width="96" } | **Direction of attack** | Name only | The direction a unit attacks in. Use it for a specific assault into an objective. |
    | ![Phase line](../assets/images/tactical-graphics/symbols/phase-line.svg){ width="96" } | **Phase line** | Your name, at both ends (required) | A named line used to control movement and report progress ("crossing PL Blue"). Always named. |
    | ![Axis of advance](../assets/images/tactical-graphics/symbols/axis-of-advance.svg){ width="96" } | **Axis of advance** | Name only | The general route of a unit's advance, leaving it room to manoeuvre along the way. |
    | ![Avenue of approach](../assets/images/tactical-graphics/symbols/avenue-of-approach.svg){ width="96" } | **Avenue of approach** | Name only | A route a force could use to reach an objective. Often drawn for the enemy's likely approach. |
    | ![Main attack](../assets/images/tactical-graphics/symbols/main-attack.svg){ width="96" } | **Main attack** | Name only | The main effort's attack: where the commander puts the most combat power. |
    | ![Supporting attack](../assets/images/tactical-graphics/symbols/supporting-attack.svg){ width="96" } | **Supporting attack** | Name only | An attack that helps the main attack, by fixing, distracting or drawing off the enemy. |
    | ![Line of departure](../assets/images/tactical-graphics/symbols/line-of-departure.svg){ width="96" } | **Line of departure** | LD | The line units cross, at a set time, to start an attack. |
    | ![Limit of advance](../assets/images/tactical-graphics/symbols/limit-of-advance.svg){ width="96" } | **Limit of advance** | LOA | A line units must not attack past, to keep them from overrunning or fratricide. |
    | ![Line of contact](../assets/images/tactical-graphics/symbols/line-of-contact.svg){ width="96" } | **Line of contact** | LC | The line where friendly and enemy forces are in contact. |
    | ![Forward line of own troops](../assets/images/tactical-graphics/symbols/forward-line-of-own-troops.svg){ width="96" } | **Forward line of own troops** | FLOT | The most forward line of friendly forces. The scallops face the enemy. |
    | ![Final coordination line](../assets/images/tactical-graphics/symbols/final-coordination-line.svg){ width="96" } | **Final coordination line** | FCL | The last line where assaulting units coordinate fires and movement before the assault. |
    | ![Probable line of deployment](../assets/images/tactical-graphics/symbols/probable-line-of-deployment.svg){ width="96" } | **Probable line of deployment** | PLD | Where attacking units are expected to deploy into assault formation. |
    | ![Holding line](../assets/images/tactical-graphics/symbols/holding-line.svg){ width="96" } | **Holding line** | HL | A line where a force holds while another passes through it, often in a passage of lines. |
    | ![Battle handover line](../assets/images/tactical-graphics/symbols/battle-handover-line.svg){ width="96" } | **Battle handover line** | BHL | The line where responsibility for the fight passes from one unit to another. |
    | ![Final protective line](../assets/images/tactical-graphics/symbols/final-protective-line.svg){ width="96" } | **Final protective line** | FPL | A line of grazing machine-gun fire that stops an assault on a defensive position. |
    | ![Ambush](../assets/images/tactical-graphics/symbols/ambush.svg){ width="96" } | **Ambush** | — | An ambush position, facing the kill zone. |
    | ![Assembly area](../assets/images/tactical-graphics/symbols/assembly-area.svg){ width="96" } | **Assembly area** | AA | Where a unit gathers and prepares before its next mission. |
    | ![Attack position](../assets/images/tactical-graphics/symbols/attack-position.svg){ width="96" } | **Attack position** | ATK POS | The last position an attacking unit occupies before crossing the line of departure. |
    | ![Assault position](../assets/images/tactical-graphics/symbols/assault-position.svg){ width="96" } | **Assault position** | ASLT POS | The last covered spot before the objective, where the assault force readies for the final rush. |
    | ![Objective area](../assets/images/tactical-graphics/symbols/objective-area.svg){ width="96" } | **Objective area** | OBJ | The objective: ground or a feature a unit must seize or control. |
    | ![Engagement area](../assets/images/tactical-graphics/symbols/engagement-area.svg){ width="96" } | **Engagement area** | EA | Where the commander plans to trap and destroy the enemy with massed fire. |
    | ![Battle position](../assets/images/tactical-graphics/symbols/battle-position.svg){ width="96" } | **Battle position** | BP | A defensive position a unit occupies and fights from. |
    | ![Support-by-fire position](../assets/images/tactical-graphics/symbols/support-by-fire-position.svg){ width="96" } | **Support-by-fire position** | SBF | Where a unit fires to support another unit's movement (base of fire). |
    | ![Attack-by-fire position](../assets/images/tactical-graphics/symbols/attack-by-fire-position.svg){ width="96" } | **Attack-by-fire position** | ABF | Where a unit fires to destroy the enemy without closing with it. |
    | ![Strong point](../assets/images/tactical-graphics/symbols/strong-point.svg){ width="96" } | **Strong point** | — | A heavily fortified defensive position, meant to be held. |
    | ![Observation post](../assets/images/tactical-graphics/symbols/observation-post.svg){ width="96" } | **Observation post** | — | A position for watching an area and reporting what you see. |
    | ![Forward observer](../assets/images/tactical-graphics/symbols/forward-observer.svg){ width="96" } | **Forward observer** | — | An observer who calls and adjusts indirect fire. |
    | ![Landing zone](../assets/images/tactical-graphics/symbols/landing-zone.svg){ width="96" } | **Landing zone** | LZ | Where helicopters land to drop off troops or cargo. |
    | ![Pickup zone](../assets/images/tactical-graphics/symbols/pickup-zone.svg){ width="96" } | **Pickup zone** | PZ | Where helicopters land to pick troops up. |

=== "Tasks"

    Each task shows its APP-6 letter beside it in the gallery and on the map.

    | Symbol | Task | Letter / label | What it means |
    |:---:|---|---|---|
    | ![Block](../assets/images/tactical-graphics/symbols/block.svg){ width="96" } | **Block** | B | Stop the enemy from getting through an area or along a route. |
    | ![Breach point](../assets/images/tactical-graphics/symbols/breach-point.svg){ width="96" } | **Breach point** | BP | Where a force will break through an obstacle. |
    | ![Bypass](../assets/images/tactical-graphics/symbols/bypass.svg){ width="96" } | **Bypass** | BYPASS | Go around an obstacle or enemy position without engaging it. |
    | ![Canalize](../assets/images/tactical-graphics/symbols/canalize.svg){ width="96" } | **Canalize** | C | Force the enemy into a narrower route, usually with obstacles or fire. |
    | ![Clear](../assets/images/tactical-graphics/symbols/clear.svg){ width="96" } | **Clear** | CLEAR | Remove all enemy from an area. |
    | ![Contain](../assets/images/tactical-graphics/symbols/contain.svg){ width="96" } | **Contain** | C | Stop the enemy from leaving an area, keeping its forces where they are. |
    | ![Cover](../assets/images/tactical-graphics/symbols/cover.svg){ width="96" } | **Cover** | C | A security task: fight to protect the main body and give it time, ahead of or beside it. |
    | ![Delay](../assets/images/tactical-graphics/symbols/delay.svg){ width="96" } | **Delay** | D | Trade ground for time: slow the enemy down without becoming decisively engaged. |
    | ![Destroy](../assets/images/tactical-graphics/symbols/destroy.svg){ width="96" } | **Destroy** | D | Physically make the enemy unable to fight. |
    | ![Disrupt](../assets/images/tactical-graphics/symbols/disrupt.svg){ width="96" } | **Disrupt** | D | Upset the enemy's formation or timing before it can attack. |
    | ![Fix](../assets/images/tactical-graphics/symbols/fix.svg){ width="96" } | **Fix** | F | Pin the enemy in place so it can't move or reinforce elsewhere. |
    | ![Guard](../assets/images/tactical-graphics/symbols/guard.svg){ width="96" } | **Guard** | G | A security task: protect the main body by fighting to gain time, staying within supporting range. |
    | ![Isolate](../assets/images/tactical-graphics/symbols/isolate.svg){ width="96" } | **Isolate** | I | Cut the enemy off from support and reinforcement. |
    | ![Neutralize](../assets/images/tactical-graphics/symbols/neutralize.svg){ width="96" } | **Neutralize** | N | Make the enemy unable to interfere with an operation for a time. |
    | ![Occupy](../assets/images/tactical-graphics/symbols/occupy.svg){ width="96" } | **Occupy** | O | Move into an area and control it, with no enemy to fight. |
    | ![Penetrate](../assets/images/tactical-graphics/symbols/penetrate.svg){ width="96" } | **Penetrate** | P | Break through the enemy's defence to disrupt it. |
    | ![Reduce](../assets/images/tactical-graphics/symbols/reduce.svg){ width="96" } | **Reduce** | REDUCE | Destroy an encircled or bypassed enemy force. |
    | ![Retain](../assets/images/tactical-graphics/symbols/retain.svg){ width="96" } | **Retain** | R | Keep the enemy from taking ground you already hold. |
    | ![Screen](../assets/images/tactical-graphics/symbols/screen.svg){ width="96" } | **Screen** | S | A security task: watch and report, giving early warning, fighting only in self-defence. |
    | ![Secure](../assets/images/tactical-graphics/symbols/secure.svg){ width="96" } | **Secure** | SECURE | Protect a unit, place or equipment from being taken or damaged. |
    | ![Seize](../assets/images/tactical-graphics/symbols/seize.svg){ width="96" } | **Seize** | S | Take and hold ground from the enemy. |
    | ![Suppress](../assets/images/tactical-graphics/symbols/suppress.svg){ width="96" } | **Suppress** | S | Stop the enemy from firing or observing for a time, usually with fire. |
    | ![Withdraw](../assets/images/tactical-graphics/symbols/withdraw.svg){ width="96" } | **Withdraw** | W | Break contact and move away from the enemy. |

=== "Obstacles"

    | Symbol | Graphic | Map label | What it means |
    |:---:|---|---|---|
    | ![Minefield](../assets/images/tactical-graphics/symbols/minefield.svg){ width="96" } | **Minefield** | MINEFIELD | An area laid with mines. |
    | ![Obstacle belt](../assets/images/tactical-graphics/symbols/obstacle-belt.svg){ width="96" } | **Obstacle belt** | OBSTACLE BELT | A planned belt of obstacles, inside which units may build their obstacles. |
    | ![Obstacle zone](../assets/images/tactical-graphics/symbols/obstacle-zone.svg){ width="96" } | **Obstacle zone** | OBSTACLE ZONE | A larger area where obstacles are allowed, holding one or more belts. |
    | ![Roadblock](../assets/images/tactical-graphics/symbols/roadblock.svg){ width="96" } | **Roadblock** | ROADBLOCK | An obstacle blocking a road. |
    | ![Wire](../assets/images/tactical-graphics/symbols/wire.svg){ width="96" } | **Wire** | WIRE | A wire obstacle, such as concertina or barbed wire. |
    | ![Generic obstacle](../assets/images/tactical-graphics/symbols/generic-obstacle.svg){ width="96" } | **Generic obstacle** | OBSTACLE | An obstacle of any type, where the exact kind doesn't matter or isn't known. |
    | ![Breach lane](../assets/images/tactical-graphics/symbols/breach-lane.svg){ width="96" } | **Breach lane** | LANE | A lane cleared through an obstacle for units to pass. |
    | ![Anti-tank ditch](../assets/images/tactical-graphics/symbols/anti-tank-ditch.svg){ width="96" } | **Anti-tank ditch** | AT DITCH | A ditch dug to stop vehicles. |
    | ![Anti-tank wall](../assets/images/tactical-graphics/symbols/anti-tank-wall.svg){ width="96" } | **Anti-tank wall** | AT WALL | A wall built to stop vehicles. |
    | ![Fortified trench line](../assets/images/tactical-graphics/symbols/fortified-trench-line.svg){ width="96" } | **Fortified trench line** | FORTIFIED | A fortified trench line. |
    | ![Antitank mine](../assets/images/tactical-graphics/symbols/antitank-mine.svg){ width="96" } | **Antitank mine** | — | A single anti-tank mine. |
    | ![Antipersonnel mine](../assets/images/tactical-graphics/symbols/antipersonnel-mine.svg){ width="96" } | **Antipersonnel mine** | — | A single anti-personnel mine. |

=== "C2"

    | Symbol | Graphic | Map label | What it means |
    |:---:|---|---|---|
    | ![Area](../assets/images/tactical-graphics/symbols/area.svg){ width="96" } | **Area** | Name only | A plain area, for anything you need to outline that has no special symbol. |
    | ![Area of operations](../assets/images/tactical-graphics/symbols/area-of-operations.svg){ width="96" } | **Area of operations** | AO | A unit's area of responsibility. |
    | ![Boundary](../assets/images/tactical-graphics/symbols/boundary.svg){ width="96" } | **Boundary** | Name only | The line between two units' areas: neither fires or moves across it without coordinating. |
    | ![Named area of interest](../assets/images/tactical-graphics/symbols/named-area-of-interest.svg){ width="96" } | **Named area of interest** | NAI | An area to watch for enemy activity, to confirm or deny what the enemy is doing. |
    | ![Target area of interest](../assets/images/tactical-graphics/symbols/target-area-of-interest.svg){ width="96" } | **Target area of interest** | TAI | An area where the enemy can be engaged once it is spotted there. |
    | ![Checkpoint](../assets/images/tactical-graphics/symbols/checkpoint.svg){ width="96" } | **Checkpoint** | CKP (in the pin) | A reference point for controlling movement and reporting position. |
    | ![Passage point](../assets/images/tactical-graphics/symbols/passage-point.svg){ width="96" } | **Passage point** | PP (in the pin) | Where one unit passes through another's position. |
    | ![Release point](../assets/images/tactical-graphics/symbols/release-point.svg){ width="96" } | **Release point** | RP (in the pin) | Where units leave a route and go to their own destinations. |
    | ![Start point](../assets/images/tactical-graphics/symbols/start-point.svg){ width="96" } | **Start point** | SP (in the pin) | Where units start a route or a march, often at a set time. |
    | ![Contact point](../assets/images/tactical-graphics/symbols/contact-point.svg){ width="96" } | **Contact point** | Your name or number, in the sign | Where two units meet to coordinate. Its number or name goes inside the sign. |
    | ![Coordination point](../assets/images/tactical-graphics/symbols/coordination-point.svg){ width="96" } | **Coordination point** | — | Where boundaries meet and adjacent units coordinate fires and movement. |
    | ![Linkup point](../assets/images/tactical-graphics/symbols/linkup-point.svg){ width="96" } | **Linkup point** | LU (in the pin) | Where two friendly forces join up. |
    | ![Rally point](../assets/images/tactical-graphics/symbols/rally-point.svg){ width="96" } | **Rally point** | RLY (in the pin) | Where a unit regroups after being split up, or before or after an action. |
    | ![Decision point](../assets/images/tactical-graphics/symbols/decision-point.svg){ width="96" } | **Decision point** | DP | A point where the commander expects to make a decision, often tied to an enemy action. |

=== "Fires"

    | Symbol | Graphic | Map label | What it means |
    |:---:|---|---|---|
    | ![Target reference point](../assets/images/tactical-graphics/symbols/target-reference-point.svg){ width="96" } | **Target reference point** | TRP | An easy-to-see point used to direct and adjust fire. |
    | ![Point target](../assets/images/tactical-graphics/symbols/point-target.svg){ width="96" } | **Point target** | — | A single target needing fire on one spot. |
    | ![Linear target](../assets/images/tactical-graphics/symbols/linear-target.svg){ width="96" } | **Linear target** | TGT | A target in a line, such as a road or tree line. |
    | ![Rectangular target](../assets/images/tactical-graphics/symbols/rectangular-target.svg){ width="96" } | **Rectangular target** | TGT | A target covering a rectangular area. |
    | ![Circular target](../assets/images/tactical-graphics/symbols/circular-target.svg){ width="96" } | **Circular target** | TGT | A target covering a circular area. |
    | ![Irregular target](../assets/images/tactical-graphics/symbols/irregular-target.svg){ width="96" } | **Irregular target** | TGT | A target covering an irregular area. |
    | ![Linear smoke target](../assets/images/tactical-graphics/symbols/linear-smoke-target.svg){ width="96" } | **Linear smoke target** | SMK | A line where smoke is fired to screen movement or block observation. |
    | ![Final protective fire](../assets/images/tactical-graphics/symbols/final-protective-fire.svg){ width="96" } | **Final protective fire** | FPF | Pre-planned fire that stops an enemy assault on a defensive position. |
    | ![No-fire area](../assets/images/tactical-graphics/symbols/no-fire-area.svg){ width="96" } | **No-fire area** | NFA | No fire into this area without approval. |
    | ![Restrictive fire area](../assets/images/tactical-graphics/symbols/restrictive-fire-area.svg){ width="96" } | **Restrictive fire area** | RFA | Fire into this area only under set limits. |
    | ![Restrictive fire line](../assets/images/tactical-graphics/symbols/restrictive-fire-line.svg){ width="96" } | **Restrictive fire line** | RFL | A line between converging friendly forces that fire must not cross without coordination. |
    | ![Free-fire area](../assets/images/tactical-graphics/symbols/free-fire-area.svg){ width="96" } | **Free-fire area** | FFA | Fire can be delivered here without further coordination. |
    | ![Position area for artillery](../assets/images/tactical-graphics/symbols/position-area-for-artillery.svg){ width="96" } | **Position area for artillery** | PAA | Where artillery units set up and fire from. |
    | ![Coordinated fire line](../assets/images/tactical-graphics/symbols/coordinated-fire-line.svg){ width="96" } | **Coordinated fire line** | CFL | Beyond this line, indirect fire can be delivered without further coordination. |
    | ![Fire support coordination line](../assets/images/tactical-graphics/symbols/fire-support-coordination-line.svg){ width="96" } | **Fire support coordination line** | FSCL | Beyond this line, attacks need no coordination with the ground commander. |
    | ![Airspace coordination area](../assets/images/tactical-graphics/symbols/airspace-coordination-area.svg){ width="96" } | **Airspace coordination area** | ACA | A block of airspace where friendly aircraft are safe from friendly surface fire. |

=== "Airspace"

    | Symbol | Graphic | Map label | What it means |
    |:---:|---|---|---|
    | ![Air control point](../assets/images/tactical-graphics/symbols/air-control-point.svg){ width="96" } | **Air control point** | ACP | A point aircraft fly to or report at, used to control air traffic. |
    | ![Air corridor](../assets/images/tactical-graphics/symbols/air-corridor.svg){ width="96" } | **Air corridor** | AC | A route for friendly aircraft, keeping them clear of friendly fire. |
    | ![Restricted operations zone](../assets/images/tactical-graphics/symbols/restricted-operations-zone.svg){ width="96" } | **Restricted operations zone** | ROZ | Airspace reserved for a specific use, closed to other aircraft. |
    | ![Low-level transit route](../assets/images/tactical-graphics/symbols/low-level-transit-route.svg){ width="96" } | **Low-level transit route** | LLTR | A low-altitude route for friendly aircraft through air defence areas. |
    | ![Minimum-risk route](../assets/images/tactical-graphics/symbols/minimum-risk-route.svg){ width="96" } | **Minimum-risk route** | MRR | A temporary route of least risk for friendly aircraft. |
    | ![Standard use Army aircraft flight route](../assets/images/tactical-graphics/symbols/standard-use-army-aircraft-flight-route.svg){ width="96" } | **Standard use Army aircraft flight route** | SAAFR | A route for army aviation moving in the rear area. |
    | ![UAS route](../assets/images/tactical-graphics/symbols/uas-route.svg){ width="96" } | **UAS route** | UAS | A route for drones. |
    | ![FARP](../assets/images/tactical-graphics/symbols/farp.svg){ width="96" } | **FARP** | FARP | Forward arming and refuelling point: where helicopters rearm and refuel near the fight. |

=== "Sustainment"

    | Symbol | Graphic | Map label | What it means |
    |:---:|---|---|---|
    | ![Casualty collection point](../assets/images/tactical-graphics/symbols/casualty-collection-point.svg){ width="96" } | **Casualty collection point** | CCP (in the pin) | Where casualties are gathered for treatment and evacuation. |
    | ![MEDEVAC pickup point](../assets/images/tactical-graphics/symbols/medevac-pickup-point.svg){ width="96" } | **MEDEVAC pickup point** | MEP (in the pin) | Where casualties are picked up for medical evacuation. |
    | ![Logistics release point](../assets/images/tactical-graphics/symbols/logistics-release-point.svg){ width="96" } | **Logistics release point** | LRP (in the pin) | Where supplies are handed over to the units that use them. |
    | ![Maintenance collection point](../assets/images/tactical-graphics/symbols/maintenance-collection-point.svg){ width="96" } | **Maintenance collection point** | MCP (in the pin) | Where damaged vehicles and equipment are gathered for repair. |
    | ![Rearm/refuel/resupply point](../assets/images/tactical-graphics/symbols/rearm-refuel-resupply-point.svg){ width="96" } | **Rearm/refuel/resupply point** | R3P (in the pin) | Where units rearm, refuel and resupply (R3P). |
    | ![Refuel on the move point](../assets/images/tactical-graphics/symbols/refuel-on-the-move-point.svg){ width="96" } | **Refuel on the move point** | ROM (in the pin) | Where vehicles refuel quickly without stopping for long. |


## Changelog

???+ info "3.1.0 — 2026-11-17: Squad layer moves to Squad Composition"
    **New**

    - Player locations have three styles: MARKER (as before), APP-6 (the friendly symbol of each player's group type, without names or look direction) and OFF. Each player picks their own; the Game Master's choice is the most anyone sees.
    - Server setting `PlayerLocations=marker`, `app6` or `off` in ServerSettings.txt sets the style every mission starts with.

    **Changed**

    - Fire teams and roles, Sections and group size, the compass HUD and group list, name tag colours and role icons, roles from carried gear, the ~ order wheel and order notices have moved to [Squad Composition](squad-composition.md). Add it to your server to keep them.
    - With Squad Composition loaded, the group list and map dots show its team colours and role icons.
    - PlayerCompassRequired is now set in Squad Composition's own ServerSettings.txt.

    **Fixed**

    - Start-up cleanup following a start-up crash report from a large server.

??? info "3.0.1 — 2026-11-11"
    - Steps aside when COALITION Squad Interface is loaded, adds PlayerCompassRequired, and assigns squad roles from carried gear.

??? info "3.0.0 — 2026-11-11: Squad Integration Overhaul"
    - Categories regrouped after APP-6, with a new Tasks category (18 new mission tasks), new maneuver lines, AT and AP mines, start and decision points, and 19 new unit types.
    - Overlays per category; scratch pads can be sent to a group or player; rebindable map keys; restyled task list and weather panes.
    - Point markers redrawn to APP-6; unit symbols in true proportions; drawing colours matched to the team colours.

??? info "2.1.x — 2026-11"
    - 2.1.3: controller fixes for placing and panels; player graphics sit above Game Master graphics.
    - 2.1.2: updated for Arma Reforger 1.9.
    - 2.1.1: receive graphics from your unit website; building numbers improved.
    - 2.1.0: click to place, Ctrl+S and Ctrl+Z, GM SEND, custom player names, radio frequencies in the roster, overlays with building numbers, optional REST export.

??? info "2.0.x and 1.x — 2026-09 / 2026-10"
    - 2.0.0: full-screen map interface with top and bottom bars, SCRATCH PAD and GRAPHICS panes, and interface settings.
    - 1.3.0: 9-line, 5-line, call for fire and MEDEVAC pads with Plot; 8-digit grid.
    - 1.2.x: briefing laser, sand table, briefing TV improvements, catalogue search, player location controls, WarBoard.
    - 1.1.x: controller support, saved layouts, interface and multiplayer fixes.
