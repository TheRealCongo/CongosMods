---
repo: TheRealCongo/Mission-Architect   # private source repo
workshop_id: 6AD6C63AAC2A63D1         # Workshop GUID (from the mod's addon.gproj)
version: 1.1.0                        # last version documented on this page
updated: 2026-11-18                   # date of that version
documented_commit: fc9c136            # mod repo commit this page was last updated against
---

# Mission Architect

<div class="infobox" markdown>
![Mission Architect thumbnail](../assets/images/placeholder-screenshot.svg)

| | |
|---|---|
| **Version** | 1.1.0 |
| **Updated** | 2026-11-18 |
| **Author** | Congo |
| **Game version** | 1.9.0.37 |
| **Dependencies** | None (base game only) |
| **Workshop** | [Congos Mission Architect](https://reforger.armaplatform.com/workshop/6AD6C63AAC2A63D1-CongosMissionArchitect) |
</div>

**Mission Architect** adds a Mission Architect mode to Game Master. Instead of moving every unit by hand, you lay out a mission ahead of time: place pieces on the map, link them with "when this happens, do that", and the mission runs itself while you watch or step in. Missions save and load, links included.

Built for dedicated servers and tested on one, including players who join mid-mission.

## Quick start

1. Open **Game Master** and use the **mode switch** (bottom right) to pick **Mission Architect**.
2. A short **guided tour** runs the first time. You can replay it any time from the bottom bar.
3. Place a **Trigger Area** where players will go, and a **Unit Spawner** nearby. Right-click the spawner and choose **Select squad...**.
4. Select the trigger, drag its **amber handle** onto the spawner, and pick **When Triggered**.
5. Walk a player into the area: the squad appears and follows the waypoints you gave it.

!!! tip "Start small"
    One trigger, one spawner, one link. **Help** in the bottom bar keeps the common setups one click away.

## The screen

<figure markdown>
  ![The Mission Architect screen](../assets/images/placeholder-screenshot.svg){ width="700" }
  <figcaption>The Mission Architect screen. (Screenshot to come.)</figcaption>
</figure>

| Where | What it is |
|---|---|
| **Top: library dock** | Every piece you can place, in tabs: **All**, **Triggers**, **Units**, **Objectives**, **Events**, **Fire**, **Logic**. The mouse wheel over the dock scrolls it sideways. |
| **Top left: Time, Weather** | The mission's time of day and current weather. |
| **Top right: Pieces, Links, AI** | How many pieces and links the mission has, and how much of the AI budget is in use. |
| **Strip** (select one piece) | The piece's kind, its number (`#12`), its armed state, and the buttons **Link**, **Properties**, its own actions (for example **Select squad...**) and **Delete**. An **amber handle** sits beside the piece for linking. |
| **Properties card** | The piece's settings in tabs (**Squad**, **Orders**, **Area**, **Settings**, **Links**). Changes apply at once. **More settings** opens the game's own Properties window. |
| **Bottom bar** | Pause / Resume, Map, hide the interface, **Guided tour**, **Help**, **Save**, **Load**, and the **mode switch** on the right (back to Game Master). |
| **Order bar** | The game's usual Game Master orders for a selected squad, just above the bottom bar. Helicopter orders appear in a row above it. |

Everything else from Game Master still works: selecting, the camera, the right-click menu, move and rotate handles.

## Pieces at a glance

Everything you place lives in the **library dock**, sorted into tabs. Click a piece, then click the ground to put it down. Press <kbd>Tab</kbd> to search by name or by what it does; <kbd>Enter</kbd> puts the first match where the camera looks.

| Tab | Piece | Icon | What it does |
|---|---|:---:|---|
| Triggers | **Trigger Area** | ![Trigger Area icon](../assets/images/mission-architect/CMA_Icon_TriggerArea.png){ .piece-icon } | Fires when people are inside, and when they leave |
| Triggers | **Trigger Line** | ![Trigger Line icon](../assets/images/mission-architect/CMA_Icon_TriggerLine.png){ .piece-icon } | A tripwire across a road or gap |
| Triggers | **No Fire Zone** | ![No Fire Zone icon](../assets/images/mission-architect/CMA_Icon_TriggerArea.png){ .piece-icon } | Nobody inside can fire or be hurt |
| Triggers | **Containment Zone** | ![Containment Zone icon](../assets/images/mission-architect/CMA_Icon_TriggerArea.png){ .piece-icon } | Holds players inside until a link releases it |
| Units | **Unit Spawner** | ![Unit Spawner icon](../assets/images/mission-architect/CMA_Icon_UnitSpawner.png){ .piece-icon } | A squad waiting with its route and orders |
| Units | **Convoy Spawner** | ![Convoy Spawner icon](../assets/images/mission-architect/CMA_Icon_ConvoySpawner.png){ .piece-icon } | Up to four crewed vehicles on a road route |
| Units | **Helicopter Spawner** | ![Helicopter Spawner icon](../assets/images/mission-architect/CMA_Icon_HelicopterSpawner.png){ .piece-icon } | A crewed helicopter: inserts troops or attacks, then flies home |
| Units | **Ambush Staging** | ![Ambush Staging icon](../assets/images/mission-architect/CMA_Icon_AmbushStaging.png){ .piece-icon } | A hidden squad, crouched and holding fire |
| Units | **Ambush Kill Box** | ![Ambush Kill Box icon](../assets/images/mission-architect/CMA_Icon_AmbushKillBox.png){ .piece-icon } | Crossing it springs the ambush |
| Units | **Order** | ![Order icon](../assets/images/mission-architect/CMA_Icon_Order.png){ .piece-icon } | Gives squads already out a new order |
| Objectives | **Clear Area** | ![Clear Area icon](../assets/images/mission-architect/CMA_Icon_ObjectiveClear.png){ .piece-icon } | Kill every defender inside |
| Objectives | **Capture** | ![Capture icon](../assets/images/mission-architect/CMA_Icon_ObjectiveCapture.png){ .piece-icon } | Hold the area until the bar fills |
| Events | **Weather Change** | ![Weather Change icon](../assets/images/mission-architect/CMA_Icon_Weather.png){ .piece-icon } | Turns the weather |
| Events | **Explosion** | ![Explosion icon](../assets/images/mission-architect/CMA_Icon_Explosion.png){ .piece-icon } | Grenade, charge, shell or IED |
| Events | **Message** | ![Message icon](../assets/images/mission-architect/CMA_Icon_Message.png){ .piece-icon } | Words on players' screens |
| Events | **Mission End** | ![Mission End icon](../assets/images/mission-architect/CMA_Icon_MissionEnd.png){ .piece-icon } | End screen with a winner |
| Fire | **Artillery** | ![Artillery icon](../assets/images/mission-architect/CMA_Icon_Artillery.png){ .piece-icon } | Shells on the box: HE, airburst, smoke, illumination |
| Fire | **Rocket Salvo** | ![Rocket Salvo icon](../assets/images/mission-architect/CMA_Icon_RocketStrike.png){ .piece-icon } | A rocket salvo walking through the box |
| Fire | **Gun Run** | ![Gun Run icon](../assets/images/mission-architect/CMA_Icon_GunRun.png){ .piece-icon } | A strafing run along the box |
| Fire | **Smoke** | ![Smoke icon](../assets/images/mission-architect/CMA_Icon_Smoke.png){ .piece-icon } | Coloured smoke |
| Fire | **Signal Flare** | ![Signal Flare icon](../assets/images/mission-architect/CMA_Icon_SignalFlare.png){ .piece-icon } | A signal flare |
| Fire | **Minefield** | ![Minefield icon](../assets/images/mission-architect/CMA_Icon_Minefield.png){ .piece-icon } | Lays a minefield |
| Logic | **All Of** | ![All Of icon](../assets/images/mission-architect/CMA_Icon_AllOf.png){ .piece-icon } | Waits until every link into it has fired |
| Logic | **Timer** | ![Timer icon](../assets/images/mission-architect/CMA_Icon_Timer.png){ .piece-icon } | A wait, a deadline or reinforcements later |
| Logic | **Mod Action** | ![Mod Action icon](../assets/images/mission-architect/CMA_Icon_ModAction.png){ .piece-icon } | Runs an action another mod offers |
| Logic | **Mod Event** | ![Mod Event icon](../assets/images/mission-architect/CMA_Icon_ModEvent.png){ .piece-icon } | Listens for another mod's event |

Three more pieces aren't in the dock. You make them by **right-clicking something already in the world** (this also works in the normal Game Master mode):

| Right-click | Choose | Icon | Makes |
|---|---|:---:|---|
| A living enemy soldier | **Make HVT** | ![HVT icon](../assets/images/mission-architect/CMA_Icon_ObjectiveHVT.png){ .piece-icon } | **Eliminate HVT** objective: hostile factions get a task to kill that soldier |
| A vehicle, cache or object | **Make Destroy target** | ![Destroy icon](../assets/images/mission-architect/CMA_Icon_ObjectiveDestroy.png){ .piece-icon } | **Destroy** objective: hostile factions get a task to destroy it |
| Any prop | **Make interactive** | ![Interaction icon](../assets/images/mission-architect/CMA_Icon_Interaction.png){ .piece-icon } | **Interaction**: players get an action on the prop (search, take intel, plant charge...) |

## Links: how pieces talk to each other

A link means **"when this happens, do that"**.

1. Select a piece and drag its **amber handle** onto another piece.
2. Pick the **event** that sets it off (for example *When Triggered* or *When Completed*).
3. A line with arrows shows what fires what. Links, routes and timings show on the map as you build.

- **Several links into one piece** mean *any* of them sets it off.
- For *all* of them, put an **All Of** in between.
- For a wait, put a **Timer** in between.
- **Properties** opens a card beside the piece with its settings, and a **Links** tab to remove a link.

You can also link by **selecting both pieces and right-clicking one**: the menu offers **Link: When ...** entries for every event that fits. **Unlink** removes links. A piece can hold up to 32 links out.

**Link delay:** pieces that fire events have a *Link delay* (0 to 60 s) in Properties. Their links wait that long before firing. The line's label shows it, for example *When Triggered +5 s*.

### Events

Each event has its own line colour on the map.

| Event | Colour | Fired by | When |
|---|---|---|---|
| **When Triggered** | <span class="swatch" style="background:#5CC8FF"></span> light blue | Trigger Area, All Of, Timer, Mod Event | The area has the right people inside for long enough; every link into an All Of has fired; a Timer ran out; another mod reported its event |
| **When Cleared** | <span class="swatch" style="background:#A8B8C8"></span> grey-blue | Trigger Area | After triggering, the people it counts have left |
| **When Crossed** | <span class="swatch" style="background:#FFB347"></span> orange | Trigger Line | Someone it counts crossed the line |
| **When Spawned** | <span class="swatch" style="background:#4FD08A"></span> green | Unit Spawner, Convoy Spawner | Every soldier has arrived; the convoy has set off |
| **When All Dead** | <span class="swatch" style="background:#FF7A6E"></span> salmon | Unit Spawner, Convoy Spawner, Helicopter Spawner, Ambush Staging | Nobody it brought in is left alive |
| **When Sprung** | <span class="swatch" style="background:#FF5A5A"></span> red | Ambush Kill Box, Ambush Staging | An enemy crossed the kill box line; the ambush opened |
| **When Completed** | <span class="swatch" style="background:#8FA8FF"></span> periwinkle | Clear Area, Capture, HVT, Destroy | The objective is done |
| **When Used** | — | Interaction | A player used the action |
| **When Landed** | <span class="swatch" style="background:#6FE3D2"></span> teal | Helicopter Spawner | The helicopter touched down (a Land or Pick Up point, or home) |
| **Must be cleared** | <span class="swatch" style="background:#C08CFF"></span> violet | Unit Spawner, Ambush Staging → Clear Area | Not an event: that squad defends the Clear Area, which can't complete until they're all dead |
| **Gives orders** | <span class="swatch" style="background:#FFD84F"></span> yellow | Order → squads | Not an event: the Order commands those squads when it's set off |

### What a link does to the piece it reaches

| Piece | A link into it... |
|---|---|
| Trigger Area, Trigger Line, Kill Box | **Arms** it again (so it can fire again) |
| Clear Area, Capture, HVT, Destroy | **Arms** it (use this to chain objectives) |
| Unit, Convoy, Helicopter Spawner | **Brings in** its squad, column or helicopter |
| Ambush Staging | **Springs** the ambush |
| Containment Zone | **Releases** it |
| Events, Fire, Order, Timer, All Of, Mod Action | **Sets it off** |
| Interaction, Mod Event, No Fire Zone | Can't be linked into |

## Legend

Only Game Masters see these. Players never see outlines or lines, and they all hide when the Game Master hides the interface.

### Armed state

Triggers, kill boxes, objectives and containment zones show a badge on their strip and card. Click the badge on the card to change it.

| Badge | Means |
|---|---|
| <span class="swatch" style="background:#0D8525"></span> **ARMED** | Watching, and will fire |
| <span class="swatch" style="background:#D9892B"></span> **USED** | Fired once and used up (Repeat is off). Click to re-arm; its links stay |
| <span class="swatch" style="background:#DE3229"></span> **NOT ARMED** | Switched off. It won't fire until armed, by hand or by a link into it |

### Area outlines

Areas are drawn on the ground as a coloured, striped rim. You can change the colour of most of them in Properties (white, red, green, blue, yellow, orange).

| Piece | Default colour | Shape |
|---|---|---|
| Trigger Area | Yellow | Circle or rectangle |
| Trigger Line | Orange | A band; arrows on one side when it only counts one direction |
| Ambush Staging | Red | Rectangle |
| Ambush Kill Box | Green | Rectangle, with its trip line a third of the way in and arrows pointing forward |
| Clear Area, Capture | Blue | Circle or rectangle |
| No Fire Zone | Blue | Circle or rectangle |
| Containment Zone | Red | Circle or rectangle, with an **amber ring 10 m outside** while armed |
| Artillery | Orange | Rectangle, with arrows showing the way the fire walks |
| Rocket Salvo, Gun Run | Red | Rectangle, with arrows showing the direction of attack |

- **White outline:** a trigger or containment zone that is not armed, or a trigger or kill box that is used up.
- **Blinking:** a piece blinks three times when it fires.

### Lines and labels

| You see | Means |
|---|---|
| A solid coloured line with arrowheads | A link. The arrowheads point at the piece it sets off. The colour is the event (see [Events](#events)) |
| A label in the middle of a line | The event, plus any delay (*When Triggered +5 s*) |
| A dashed amber line to the mouse | You're in the middle of making a link |
| A teal line with arrowheads | A helicopter's flight path. Points read **ETA**, **LAND**, **PICKUP** (amber) or **ATTACK** (red) with a time |
| **WAITS 1:00** (grey) over a Timer | The timer is idle |
| **TIMER 0:42** (amber) over a Timer | The timer is counting down |

### What players see

| On screen | Means |
|---|---|
| A task in the task list, with a marker | An objective. HVT and Destroy markers follow the target |
| A timer at the top of the screen | They're inside a Capture area. Red, then yellow from half time, green when done |
| **NO FIRE ZONE** | They're inside a No Fire Zone and can't use weapons |
| **RETURN TO THE AREA** | They're leaving a Containment Zone |

## How-to recipes

These are the same setups the in-game **Help** card lists. Arrows read "link from → to: event".

??? example "Ambush"
    Put **Ambush Staging** in cover and an **Ambush Kill Box** on the road. Link kill box → staging: **When Sprung**. Pick the squad with **Select squad...**

    Nobody is there until the enemy crosses the line a third of the way into the kill box. Then the squad appears and opens fire.

    The kill box only fires once it's linked to a staging box: that's how it knows who the enemy is.

??? example "Reinforcements and QRF"
    Trigger Area or Trigger Line → **Unit Spawner**: *When Triggered* / *When Crossed*. Give the waiting squad waypoints first.

    - **QRF:** set **Go to: Where it was set off** and the squad hunts whoever tripped the link.
    - **Mounted:** right-click the spawner: **Select vehicle...** The squad drives its Move waypoints on the roads, and mounted squads called together drive as one column.

??? example "Convoy"
    **Convoy Spawner**: right-click: **Add vehicle...** (up to four, in march order), set **Faction** in Properties, and give its waiting group Move waypoints along the road. Link a trigger to it: the column appears crewed at the box and drives the route.

??? example "Garrison a building or village"
    Unit Spawner Properties: **Garrison**: *Nearest building*, or *Buildings in radius* (a base, a village). The squad takes window and room spots when it spawns and holds them. Give it a waypoint to send it out.

??? example "Clear a compound"
    Put a **Clear Area** over it. Unit Spawners → Clear Area: **Must be cleared**. The squads come in when the area goes live.

??? example "Hold a point"
    Place a **Capture** area and set **Objective timer** in Properties. Enemies inside pause it.

??? example "Chain objectives"
    Objective → next objective: **When Completed**. Set the next one **not armed** so it waits its turn: objectives start armed, with a task, as soon as they're placed.

??? example "Only when both happen, or after a time"
    Both pieces → **All Of**, All Of → what should happen. Or **Timer** (Starts: as soon as placed) → what should happen.

??? example "Eliminate an HVT or destroy a target"
    Right-click an enemy soldier: **Make HVT**. Right-click a vehicle, cache or object: **Make Destroy target**.

??? example "Change the weather"
    Trigger Area or Line → **Weather Change**: *When Triggered* / *When Crossed*. Pick the weather in Properties.

??? example "IED"
    **Explosion** on the road, **Trigger Line** across it → Explosion: **When Crossed**. Pick the explosive in Properties.

??? example "Fire support"
    **Artillery**, **Rocket Salvo** or **Gun Run** over the target, its arrows pointing the way the fire should walk (rockets and gun runs come in from behind the box). Trigger or objective → it.

    Properties: pattern, shell (HE, airburst, smoke, illumination), calibre (60 to 120 mm), rounds; rocket; gun.

??? example "Smoke, flares and mines"
    **Smoke** (colour), **Signal Flare** (colour) or **Minefield** (type and size, US or Soviet mines). Link anything to it. A minefield is armed as soon as it is laid.

??? example "Helicopters"
    **Helicopter Spawner**: right-click: **Add vehicle...** (a helicopter), **Select squad...** for passengers, and set **Faction** for the crew. Select its waiting group: the aviation orders sit above the order bar.

    | Order | What it does |
    |---|---|
    | **Fly To** | Flies through the point |
    | **Land** | Lands, passengers and players get out, flies on |
    | **Pick Up** | Lands, waits the *Pickup wait* for players to climb in, flies on |
    | **Attack Run** | Rockets and guns on the point |

    Trigger → it. After its last order it flies home and lands. It never lifts off while a player climbs in or out, nor from a landing with players aboard. Events: *When Landed*, *When All Dead*.

??? example "Orders for squads already out"
    An **Order** piece gives squads already out a new order: move, forced move, relaxed move, defend, search and destroy, or withdraw a set distance away from whoever set it off. Select it and a group icon, right-click: **Order: command this group**. Trigger → Order piece.

    For direct orders, select a squad and use the order bar at the bottom.

??? example "Tell players something"
    Place a **Message**, right-click: **Write message...** Trigger or objective → Message. Properties: who reads it, hint or centre text.

??? example "Intel or actions on a prop"
    Right-click the prop: **Make interactive**. Interaction → Message (or spawner, objective): **When Used**. Properties: action, hold time, uses, remove prop.

??? example "Win or lose"
    Last objective → **Mission End**: *When Completed* (Result: your side wins). A squad's *When All Dead* → Mission End works for a loss.

??? example "Save and load a mission"
    Bottom bar, **Save**: give it a name, then **Save on server** (every Game Master on that server can load it) or **Save on my PC** (take it to another server). **Load** adds a saved mission to the current one, links included.

!!! warning "A white trigger won't fire"
    A white Trigger Area or Line is **not armed**. Arm it on its card, or link something to it that arms it.

## Piece reference

Every setting below is in the piece's **Properties**. Sizes and timers have sliders; the numbers in brackets are the range and default.

!!! info "Rules every piece follows"
    - All mission logic runs on the server, so it works the same for every player, including players who join mid-mission.
    - **Who counts:** unconscious characters never set off triggers. Someone in a vehicle counts where the vehicle is. Height is ignored, so hilltops and upper floors inside the outline count as inside.
    - Moving or turning a box shows a ghost of where it will land. Rectangles turn with the piece.

### Triggers

??? abstract "Trigger Area"
    A circle or rectangle that fires **When Triggered** when the right people have been inside long enough, and **When Cleared** when they're gone.

    | Setting | Options | Default |
    |---|---|---|
    | Armed | on / off | On |
    | Area shape | Circle, Rectangle | Circle |
    | Colour | White, Red, Green, Blue, Yellow, Orange | Yellow |
    | Radius or width | 5 – 1000 m | 25 m |
    | Length | 5 – 1000 m (rectangle) | 25 m |
    | Who sets it off | Anyone, Players only, AI only, One faction, Enemies of a faction | Anyone |
    | Faction | The mission's factions (for the two faction choices) | — |
    | Fire when empty | On: fires when nobody who counts is inside | Off |
    | At least | 1 – 50 people | 1 |
    | Must stay | 0 – 60 s | 0 s |
    | Repeat | On: fires again each time it has been cleared | Off |
    | Cooldown | 0 – 60 s, with Repeat on | 0 s |
    | Link delay | 0 – 60 s | 0 s |

    With Repeat off it fires once and shows **USED**. Right-click **Re-arm** (or link something into it) to use it again.

??? abstract "Trigger Line"
    A tripwire. Fires **When Crossed** when someone it counts walks or drives across it. No speed can skip it.

    | Setting | Options | Default |
    |---|---|---|
    | Armed | on / off | On |
    | Colour | six colours | Orange |
    | Line length | 2 – 1000 m | 30 m |
    | Direction | Both ways, Along the arrows only | Both ways |
    | Who sets it off | as Trigger Area | Anyone |
    | Faction | — | — |
    | Repeat, Cooldown, Link delay | as Trigger Area | Off, 0 s, 0 s |

    Turn the line to turn it. With **Along the arrows only**, arrows show the direction that counts.

??? abstract "No Fire Zone"
    Always on while it's placed; it has no links in or out.

    - Players inside can't fire, throw grenades, melee, or use vehicle or helicopter weapons, and see **NO FIRE ZONE**.
    - AI inside hold their fire.
    - Nothing inside can be hurt by fire from anywhere, including the Game Master's own explosions and fire support. Healing still works.

    | Setting | Options | Default |
    |---|---|---|
    | Area shape | Circle, Rectangle | Circle |
    | Radius or width, Length | 5 – 1000 m | 50 m |
    | Colour | six colours | Blue |

??? abstract "Containment Zone"
    Holds players inside. Armed when placed.

    - A player who has been inside while it's armed is held.
    - Up to 10 m outside, they see **RETURN TO THE AREA**. Further out, they're moved back to a clear spot near the centre (in a vehicle, the vehicle goes back with everyone in it).
    - **Any link into it releases it.** Arming it again holds whoever is inside.
    - Affects players only, not AI.

    | Setting | Options | Default |
    |---|---|---|
    | Armed | on / off | On |
    | Area shape | Circle, Rectangle | Circle |
    | Radius or width, Length | 5 – 1000 m | 50 m |
    | Colour | six colours | Red |

### Units

??? abstract "Unit Spawner"
    Holds a **waiting squad** at the box. Nobody is there until a link fires; then the soldiers appear and follow the waypoints you gave the waiting squad. Every later call brings a fresh squad that walks the same route.

    **Right-click:** **Select squad...**, **Select vehicle...**, **Remove vehicle**. After choosing Select squad or vehicle, place it from the browser near the box (within 20 m, within a minute): it isn't placed, it becomes the box's squad.

    | Setting | Options | Default |
    |---|---|---|
    | Group | Any squad from the factions' lists | — |
    | Soldiers | 0 – 32 (0 = the whole group) | 0 |
    | Go to | Its own waypoints only, Where it was set off (QRF) | Own waypoints |
    | Garrison | Off, Nearest building, Buildings in radius | Off |
    | Garrison radius | 10 – 200 m | 50 m |
    | Drive speed | 10 – 90 km/h (mounted) | 40 km/h |
    | Spacing | 5 – 60 m (mounted) | 15 m |
    | Stance | Auto, Stand, Crouch, Prone | Auto |
    | Pace | Auto, Walk, Run, Sprint | Auto |
    | Formation | Group default, Wedge, Line, Column, Staggered column | Group default |
    | Alertness | None, Safe, Aware, Combat, Stealth | None |
    | Fire | Auto, Fire at will, Return fire, Hold fire | Auto |
    | Link delay | 0 – 60 s | 0 s |

    - **Alertness:** Safe = walk, weapons lowered, return fire. Aware = run, fire at will. Combat = run, crouched, fire at will. Stealth = walk, crouched, hold fire. The Stance, Pace and Fire rows override it.
    - **QRF:** with *Where it was set off*, the squad walks its route, then hunts whoever set off the link.
    - **Mounted:** the squad appears in its vehicle in front of the box and drives its Move waypoints on the roads. Mounted squads called together drive as one column.
    - **Garrison:** the squad takes window, door and room spots and holds them. *Nearest building* looks up to 40 m from the box; *Buildings in radius* can fill a base or village. Give it a waypoint to send it out.
    - **Calling again:** a call while a squad is out brings another. **When All Dead** waits for every squad this spawner brought in.
    - Events: **When Spawned**, **When All Dead**, and **Must be cleared** into a Clear Area.

??? abstract "Convoy Spawner"
    Up to four crewed wheeled vehicles that drive a road route.

    **Right-click:** **Add vehicle...** (once per vehicle, in march order), **Clear vehicles**.

    | Setting | Options | Default |
    |---|---|---|
    | Faction | The crew's faction | — |
    | Drive speed | 10 – 90 km/h | 40 km/h |
    | Spacing | 5 – 60 m | 15 m |
    | Link delay | 0 – 60 s | 0 s |

    - **The route:** give the convoy's waiting group **Move** waypoints along the road. Every call drives the whole route again.
    - On a call, the column appears at the box with drivers and gunners, sets off together, follows the roads, slows for bends and keeps its spacing. At the end it stops and parks.
    - Give a crew a new waypoint and it leaves the convoy and is yours again.
    - Events: **When Spawned** (the column sets off), **When All Dead**.

??? abstract "Helicopter Spawner"
    A crewed helicopter that flies a list of orders, then flies home and lands.

    **Right-click:** **Add vehicle...** (one helicopter), **Select squad...** (passengers, optional), **Clear vehicles**.

    | Setting | Options | Default |
    |---|---|---|
    | Faction | The crew's faction | — |
    | Pickup wait | 5 – 300 s on the ground at a Pick Up | 30 s |
    | Link delay | 0 – 60 s | 0 s |

    **Orders:** select the helicopter's waiting group; the aviation orders appear above the order bar.

    | Order | What it does |
    |---|---|
    | **Fly To** | Flies through the point |
    | **Land** | Lands, passengers and players get out, flies on |
    | **Pick Up** | Lands, waits the *Pickup wait* for players to climb in, flies on |
    | **Attack Run** | A rocket and gun dive on the point, then flies on |

    - It checks each landing spot for slopes, rocks and trees, and moves up to 60 m to find a clear, flat one.
    - It never lifts off while a player is climbing in or out, nor from a Land point with a player still aboard.
    - Passengers only get out at **Land** points.
    - Every call flies the same orders again.
    - Events: **When Landed**, **When All Dead**.

??? abstract "Ambush Staging"
    Where the ambush squad waits, crouched and holding fire. Works as a pair with an **Ambush Kill Box**.

    **Right-click:** **Select squad...**, **Spring ambush** (open now, without waiting), **Re-arm ambush** (a fresh squad, ready again).

    | Setting | Options | Default |
    |---|---|---|
    | Colour | six colours | Red |
    | Radius or width, Length | 5 – 1000 m | 20 m, 10 m |
    | Squad appears | When the kill box is crossed, At once, waiting crouched | When the kill box is crossed |
    | Opener | Suppressive fire (5 s), Grenades, Open fire | Suppressive fire |
    | Group, Soldiers | as Unit Spawner | — |
    | Link delay | 0 – 60 s | 0 s |

    - By default nobody is in the box until it springs, so the ambush can't be spotted early.
    - **Any** link springs it, not only a kill box.
    - On springing, the ambushers pick targets from the unit that set it off and open with the chosen opener.
    - If the waiting squad comes under fire first, it springs at once, without the opener.
    - Events: **When Sprung**, **When All Dead**, **Must be cleared** into a Clear Area.

??? abstract "Ambush Kill Box"
    The box the target moves through. Fires **When Sprung** when an **enemy of the ambush squad** crosses its line, a third of the way in, going forward along the arrows.

    | Setting | Options | Default |
    |---|---|---|
    | Armed | on / off | On |
    | Colour | six colours | Green |
    | Radius or width | 5 – 1000 m | 20 m |
    | Length | 5 – 1000 m | 60 m |
    | Link delay | 0 – 60 s | 0 s |

    !!! warning "Link it to an Ambush Staging box"
        The kill box works out who the enemy is from the staging box it's linked to. **With no Ambush Staging linked, it never fires.**

??? abstract "Order"
    Gives squads that are already out a new order when it's set off. They drop their waypoints and take the new one at the Order piece.

    | Setting | Options | Default |
    |---|---|---|
    | Order | Move here, Forced move here (no stopping to fight), Relaxed move here (walking), Defend here, Search and destroy here, Withdraw (away from who set it off) | Move here |
    | Fall back | 25 – 1000 m (for Withdraw) | 200 m |

    **Choosing the squads:** select the Order and a group, right-click: **Order: command this group**. Or drag the Order's handle onto a spawner, group or soldier.

    - A spawner or staging box you tie it to passes the order to all its squads, now and later, and the tie saves with the mission.
    - A group placed from the game's own menu works live only, up to four per Order.

### Objectives

!!! note "Objectives start armed"
    A Clear Area or Capture goes live, with a task for players, as soon as it's placed. To chain objectives, switch **Armed** off on the later ones and link **When Completed** into them.

??? abstract "Clear Area"
    The chosen side gets the task **Clear the area**. It completes when every defender is dead and the side holds the area.

    | Setting | Options | Default |
    |---|---|---|
    | Armed | on / off | On |
    | Area shape, Colour | as Trigger Area | Circle, Blue |
    | Radius or width, Length | 5 – 1000 m | 25 m |
    | Faction | The side that gets the task | — |
    | At least | 1 – 50 of the side inside | 1 |
    | Must stay | 0 – 60 s | 10 s |
    | Link delay | 0 – 60 s | 0 s |

    - **Defenders:** enemy AI seen inside, and every soldier of any squad linked to it with **Must be cleared**. A defender must die wherever they go afterwards.
    - When it goes live, it brings in the linked squads that haven't appeared yet.
    - Defender squads with no orders defend the area.

??? abstract "Capture"
    The chosen side gets the task **Capture the objective** and must hold the area for the **Objective timer**.

    | Setting | Options | Default |
    |---|---|---|
    | Armed | on / off | On |
    | Area shape, Colour | as Trigger Area | Circle, Blue |
    | Radius or width, Length | 5 – 1000 m | 25 m |
    | Faction | The side that gets the task | — |
    | At least | 1 – 50 of the side inside | 1 |
    | Objective timer | 1 – 60 s | 60 s |
    | Link delay | 0 – 60 s | 0 s |

    The timer runs while the side holds the area alone, **pauses** while enemies are inside with them, and **winds back** while only enemies are inside. Everyone inside sees it at the top of the screen.

??? abstract "Eliminate HVT"
    Right-click a living soldier: **Make HVT**. Every faction hostile to that soldier gets the task **Eliminate the HVT**, with a marker that follows the target. Completes when the soldier dies. If a Game Master deletes the target, the task is cancelled.

??? abstract "Destroy"
    Right-click a vehicle, cache or object: **Make Destroy target**. Factions hostile to its owner (every faction, if it has none) get the task **Destroy the target**. Completes when it's destroyed. If a Game Master deletes it undamaged, the task is cancelled.

### Event pieces

??? abstract "Weather Change"
    Turns the weather when a link fires.

    | Setting | Options | Default |
    |---|---|---|
    | Weather | The map's weather (weather mods replace this list) | — |
    | Change over | 0 – 600 s (0 = at once) | 15 s |

??? abstract "Explosion"
    A real explosion at the piece, with the game's normal damage. Each link sets it off again.

    | Setting | Options | Default |
    |---|---|---|
    | Explosive | Grenade, Demolition charge, Artillery shell, IED, Large IED | IED |

??? abstract "Message"
    Right-click: **Write message...** to type a title (up to 60 characters) and text (up to 400).

    | Setting | Options | Default |
    |---|---|---|
    | Shown to | Everyone, One faction, Who set it off, and their squad | Everyone |
    | Faction | For One faction | — |
    | Shown as | Hint box, Big centre text | Hint box |
    | Shown for | 3 – 30 s | 8 s |

    *Who set it off, and their squad* reaches only players: if an AI or a timer set it off, nobody sees it.

??? abstract "Mission End"
    Ends the mission with the game's own end screen.

    | Setting | Options | Default |
    |---|---|---|
    | Result | A faction wins, Mission over, no winner | A faction wins |
    | Faction | The winner | — |

??? abstract "Interaction"
    Right-click a prop: **Make interactive**. Players within 4.5 m who can see the prop get an action on it. Using it fires **When Used**.

    | Setting | Options | Default |
    |---|---|---|
    | Action | Search, Take intel, Plant charge, Disarm, Free hostage, Use | Search |
    | Hold time | 0 – 15 s (0 = at once) | 3 s |
    | Uses | Once, Once per player, Every time | Once |
    | Remove prop | Removes the prop after use | Off |
    | Link delay | 0 – 60 s | 0 s |

### Fire support

??? abstract "Artillery"
    Shells land in the box, walking the way its arrows point.

    | Setting | Options | Default |
    |---|---|---|
    | Radius or width, Length | 5 – 1000 m | 40 m, 60 m |
    | Pattern | Single round, Focused, Scattered, Creeping, Line | Scattered |
    | Shell | High explosive, Smoke (81/82 mm), Illumination (81/82 mm), Airburst (not 82 mm) | High explosive |
    | Calibre | 60 mm mortar, 81 mm mortar (US M252), 82 mm mortar (Soviet 2B14), 105 mm howitzer, 120 mm mortar | 81 mm |
    | Rounds | 1 – 40 | 8 |
    | Between rounds | 0.5 – 10 s | 1.5 s |

    The first round lands about half a second after the link. Moving or deleting the piece mid-barrage doesn't stop it.

??? abstract "Rocket Salvo"
    Rockets come in from behind the box along its arrows, one every eighth of a second.

    | Setting | Options | Default |
    |---|---|---|
    | Radius or width, Length | 5 – 1000 m | 20 m, 40 m |
    | Rocket | Hydra 70 HE (US), Hydra 70 HEDP (US), S-5 Frag (Soviet), S-5 HEDP (Soviet) | Hydra 70 HE |
    | Rounds | 1 – 40 | 8 |

??? abstract "Gun Run"
    A 2.4-second strafing burst walked through the box along its arrows, with tracers.

    | Setting | Options | Default |
    |---|---|---|
    | Radius or width, Length | 5 – 1000 m | 8 m, 80 m |
    | Gun | 7.62 mm (US), 7.62 mm (Soviet), 12.7 mm (US), 12.7 mm (Soviet), 14.5 mm (Soviet) | 7.62 mm (US) |

??? abstract "Smoke, Signal Flare, Minefield"
    | Piece | Setting | Options | Default |
    |---|---|---|---|
    | Smoke | Smoke colour | White, Red, Green, Yellow, Purple | White |
    | Signal Flare | Flare colour | White, Red, Green | White |
    | Minefield | Minefield | Anti-tank (small, medium, large, row), Anti-personnel (small, medium) | Anti-tank, small |
    | Minefield | Mines | US mines, Soviet mines | US mines |

    A minefield is armed as soon as it's laid. Delete it like any minefield to remove the mines.

### Logic

??? abstract "All Of"
    Fires **When Triggered** once **every piece linked into it** has fired, in any order. Then it starts counting again.

??? abstract "Timer"
    Fires **When Triggered** after its wait.

    | Setting | Options | Default |
    |---|---|---|
    | Wait | 5 – 3600 s | 60 s |
    | Starts | When a link reaches it, As soon as it is placed | When a link reaches it |

    A link while it's running restarts it from full.

??? abstract "Mod Action and Mod Event"
    Hooks for other mods: see [Compatibility and hooks](#compatibility-and-hooks-for-other-mods). Pick the action or event in Properties. Nothing happens if the mod that offers it isn't loaded.

## Smarter enemy squads

Squads placed by Mission Architect react to fire: suppression throws off their aim, they take cover behind walls and rise to shoot, and they hear footsteps.

## Controls and settings

### Interface style

In the game's **Settings**, the **Congo's Mods** tab has a **Mission Architect** section with **Mission Architect Interface Style**:

- **CMA** (default): Mission Architect's own screen, described above.
- **Vanilla**: the game's own Game Master screen.

**On a controller, Mission Architect always uses the vanilla screen**, so controller players get the layout they already know. Link lines, labels and outlines still show. Mission Architect's own screen comes back when you use the mouse.

=== "Mouse and keyboard"

    | Do | How |
    |---|---|
    | Place a piece | Click it in the dock, then click the ground |
    | Search the library | <kbd>Tab</kbd>, type a name or what it does. <kbd>Enter</kbd> places the first match where the camera looks |
    | Close search, cancel a link | <kbd>Esc</kbd> |
    | Link two pieces | Drag the amber handle onto the other piece, or click **Link** then the other piece. Pick the event |
    | Link from the menu | Select both pieces, right-click one, pick **Link: When ...** |
    | Remove a link | Properties card, **Links** tab, the **X** beside it; or right-click **Unlink** |
    | Change settings | **Properties** on the strip, then the arrows on each row |
    | Orders for a squad | Select it and use the order bar at the bottom |

=== "Controller (vanilla screen)"

    | Do | How |
    |---|---|
    | Open the piece menu | Hold the radial button (hold X), as in normal Game Master |
    | Link two pieces | On the first piece pick **Link: start here**, then on the second pick **Link: When ...**. **Link: cancel** stops |
    | Tie a squad to an Order | **Link: start here** on the Order, then **Link: give this group orders** on the squad |
    | Cards (messages, save, load, help) | D-pad to move, A to press, B to close |

    The guided tour needs a mouse.

### Saving and loading missions

- **Save** (bottom bar): give the mission a name (letters, digits, spaces, `-` and `_`; the same name replaces the old save). Then **Save on server** (every Game Master on that server can load it) or **Save on my PC** (take it to another server).
- **Load** lists the missions **On the server** and **On my PC**. Loading **adds** the pieces to the current mission and rebuilds their links.
- Missions that use a **Mod Action** remember it by name. Loaded on a server without that mod, the piece does nothing.

## Compatibility and hooks for other mods

Mission Architect needs no other mod, and no other mod needs it. Other mods can plug into it through **open hooks**: they call Mission Architect by name, which quietly does nothing when Mission Architect isn't loaded. Neither mod depends on the other.

In game, these show up as two logic pieces:

- **Mod Event** listens for something another mod reports, and fires its links.
- **Mod Action** runs an action another mod offers, when a link fires it.

Pick which event or action in the piece's Properties.

### For mod makers

Register your hooks on **every machine** (the Game Masters' lists are built locally), for example from your game mode's start. All calls are by name, so your mod compiles and runs without Mission Architect:

```c
// Offer an action. Game Masters see the label on Mod Action pieces.
int unused;
GetGame().GetScriptModule().Call(null, "CMA_RegisterHook", false, unused, "action", "Call artillery", "MyMod_Artillery");

// Offer an event. Game Masters see the label on Mod Event pieces.
GetGame().GetScriptModule().Call(null, "CMA_RegisterHook", false, unused, "event", "Alarm raised", "mymod_alarm");
```

An action is a global function that runs **on the server**:

```c
void MyMod_Artillery(int nodeId, IEntity cause, vector position)
{
    // nodeId: the Mod Action piece that fired; cause: who set it off; position: where the piece is.
}
```

Raise your event **on the server**; every Mod Event piece listening for that key fires:

```c
int unused;
GetGame().GetScriptModule().Call(null, "CMA_RaiseEvent", false, unused, "mymod_alarm", causeEntity);
```

Leave Mission Architect's squads alone (spawner, ambush and convoy squads, waiting or out), for example if your mod also manages AI:

```c
bool owned;
GetGame().GetScriptModule().Call(null, "CMA_OwnsGroup", false, owned, group);
if (owned)
    return; // a Mission Architect squad
```

!!! note "Try it without another mod"
    Mission Architect ships an example of each: **Example: write a log line** (Mod Action) and **Example event** (Mod Event).

## Server setup

Add the mod to your server config's mod list:

```json
{
  "modId": "6AD6C63AAC2A63D1",
  "name": "Congos Mission Architect"
}
```

## Changelog

???+ info "1.1.0 — 2026-11-18"
    **New**

    - Controller support: on a gamepad, Mission Architect switches to the vanilla Game Master interface and controls, so controller players get the layout they already know.
    - New setting in Congo's Mods: "Mission Architect Interface Style" (CMA / Vanilla).
    - Link pieces from the radial menu in the vanilla interface.
    - No Fire Zone: players and AI inside can't fire, throw grenades or use vehicle weapons, and fire from outside doesn't hurt anyone or anything inside.
    - Containment Zone: players who enter are held inside. A warning shows in the 10 m ring around it, and anyone who goes past the ring is moved back. Any link releases the zone, and Game Masters see the ring.
    - Link lines, labels and area outlines hide when the Game Master hides the interface.

    **Fixes**

    - Both IEDs now make their explosion sound.
    - The artillery shell in the Explosion piece now fires and explodes.
    - The demolition charge no longer throws an error when it goes off.

??? info "1.0.0 — 2026-11-17"
    - First Workshop release.
