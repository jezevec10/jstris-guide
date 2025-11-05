<h1>Jstris Usermode Guide</h1>

<h2>Table of Contents</h2>

- [Usermode basics](#usermode-basics)
  - [Getting started](#getting-started)
  - [Editor](#editor)
  - [Components](#components)
    - [Trigger](#trigger)
    - [Queue](#queue)
    - [Condition](#condition)
    - [Variable](#variable)
    - [Map](#map)
    - [Stats](#stats)
    - [Text](#text)
    - [Pause](#pause)
    - [Audio](#audio)
    - [Attack](#attack)
    - [Ruleset](#ruleset)
    - [Block skin](#block-skin)
    - [Run](#run)
    - [Relative Trigger](#relative-trigger)
    - [On/Off](#onoff)
    - [Random](#random)
- [Publishing usermodes](#publishing-usermodes)
- [Usermode peculiarities](#usermode-peculiarities)
  - [System variables](#system-variables)
  - [Local counters](#local-counters)
  - [Special functions](#special-functions)
    - [`getBoard`](#getboard)
    - [`setBoard`](#setboard)
    - [`queueReplace`](#queuereplace)
    - [`queueAppend`](#queueappend)
    - [`getX`](#getx)
    - [`getY`](#gety)
    - [`getRot`](#getrot)
    - [`getBlockName`](#getblockname)
    - [`getBlock`](#getblock)
    - [`isCollision`](#iscollision)
    - [`setX`](#setx)
    - [`setY`](#sety)
    - [`setRot`](#setrot)
    - [`setPos`](#setpos)
    - [`setBlock`](#setblock)
    - [`setToSpawnPos`](#settospawnpos)
    - [`moveToWall`](#movetowall)
    - [`hardDrop`](#harddrop)
    - [`rotate`](#rotate)
    - [`holdBlock`](#holdblock)
    - [`moveX`](#movex)
  - [Ruleset specification](#ruleset-specification)
    - [`attackTable`](#attacktable)
    - [`comboTable`](#combotable)
    - [`hasHold`](#hashold)
    - [`sgProfile`](#sgprofile)
    - [`clearDelay`](#cleardelay)
    - [`gravityLvl`](#gravitylvl)
    - [`garbageDelay`](#garbagedelay)
    - [`lockDelay`](#lockdelay)
    - [`mess`](#mess)
    - [`gapW`](#gapw)
    - [`allSpin`](#allspin)
    - [`asEx`](#asex)
    - [`gInv`](#ginv)
    - [`solidAtk`](#solidatk)
    - [`blocksSel`](#blockssel)
    - [`rndSel`](#rndsel)
    - [`gblockSel`](#gblocksel)
    - [`prSel`](#prsel)
    - [`clearLines`](#clearlines)
    - [`DAS`](#das)
    - [`ARR`](#arr)
    - [`ghost`](#ghost)
    - [`scoreMult`](#scoremult)
  - [Block name reference list](#block-name-reference-list)
    - [Set 0: Standard](#set-0-standard)
    - [Set 1: Big, moves 2 spaces left/right at a time](#set-1-big-moves-2-spaces-leftright-at-a-time)
    - [Set 2: Big, moves 1 space left/right at a time](#set-2-big-moves-1-space-leftright-at-a-time)
    - [Set 3: Arika Rotation System](#set-3-arika-rotation-system)
    - [Set 4: Pentominoes](#set-4-pentominoes)
    - [Set 5: M123](#set-5-m123)
    - [Set 6: All-29](#set-6-all-29)
    - [Set 7: Cultris II Rotation System](#set-7-cultris-ii-rotation-system)
    - [Set 8: O-spin Rotation System](#set-8-o-spin-rotation-system)
    - [Set 9: NONE](#set-9-none)

- - - 
# Usermode basics

## Getting started

Usermodes allow players to create their own custom gamemodes and share them with other players.

To get started, go to your Account Settings, then in the "Other" tab check the Experiments toggle.

Please note that you need to have at least 10 hours of playtime on your account or be a Supporter to be able to access Usermodes.

![access_usermodes]

After enabling experimental features, a new tab called "Usermodes" should be available.

![usermodes_tab]

Choose "Create" to create your first usermode, or "Browse" to explore usermodes created by other players.

## Editor

After choosing "Create", you will be presented with the Usermode Editor.

![editor]

Drag and drop components from the sidebar to the component area, or click on components to put them at the bottom of your usermode.

Be aware that there's a 2000-component limit for usermodes - though hitting it is very unlikely. If you do, please suggest changes/additions to usermodes in [Jstris Discord](https://discord.gg/RcNFCZC).

## Components

Usermodes are constructed by putting components together, starting with a "Trigger" component that triggers the components below it, from top to bottom.

If you put your component in the wrong place, you can always drag it somewhere else by dragging the component's title bar.

![mode_example]

While hovering over a component with the mouse cursor, extra options are available:
- An ON/OFF switch,
- Green (+) - duplicates a component and puts it below the current component when pressed,
- Red (-) - removes the component.

Each component gets an ID assigned to it when added (unless it's duplicated) - these IDs are used for the [On/Off](#onoff) component and the [Random](#random) component.

### Trigger

![comp_trigger]

**Triggers** are the starting point of your usermode. When a certain game action is performed, all components under that Trigger will be executed.

There must be at least one Trigger in the usermode.

Trigger options are as follows:
- **Before the game** - triggers before the "Ready-Go" sequence.<br>
- **Before the game - only the first game** - triggers before the "Ready-Go" sequence, but only on the first game, after a restart this won't be triggered.<br>
  *Before the game* only supports [Queue](#queue), [Variable](#variable), [Map](#map), [Stats](#stats), [Text](#text), [Pause](#pause), [Audio](#audio), [Ruleset](#ruleset) and [Block Skin](#block-skin) components underneath itself.
- **On game start** - triggers after the "Ready-Go" sequence.
- **After the game** - triggers after completing the usermode successfully.
- **At a specific time** - triggers when a certain amount of time passes from the start of the game.
- **On each block** - triggers after placing a block, when the next block appears, after line clears were processed.
- **On each line clear** - triggers after any line clear.
- **On specific block #** - triggers once after a certain amount of blocks were placed.
- **On specific # lines cleared** - triggers once after you cleared more than # lines.
- **Key down** - triggers when a key is pressed.
- **Key up** - triggers when a key is released.<br>
  Key up and Key down triggers react to a specified key code. You can use [this keycode utility](https://www.toptal.com/developers/keycode) to determine the key code of your desired key. Accepts both string (e.code) or integer (e.keyCode). Using string code is recommended.<br>
  Key up and Key down triggers also accept an option to prevent the default action when a player has that key bound. If you want to disable all user's controls, instead use global [Ruleset](#ruleset) with setting `disableAllUserControls` to `true`.
- **Variable changes** - triggers when a [variable](#variable) changes. Does not support [system variables](#system-variables).
- **Never** - does not trigger.
- **External/Conditional** - you can set your own external trigger name for [Condition](#condition), [Run](#run), [Relative Trigger](#relative-trigger), [On/Off](#onoff) or a [Random](#random) component to trigger.<br>
Custom trigger names must be **at most 20 characters long** and are case-sensitive.

### Queue
![comp_queue]

**Queue** components allow you to replace a queue with your own fixed queue.

Be aware that if the finite queue runs out of pieces, the game is over, no matter whether there's a piece in Hold or not.

Type the tetromino block names in the "Queue" field to set up the queue.

There are four options available:
  - **Allow refill if queue is used** - After all the pieces from the queue are used up, the game keeps dealing new pieces according to the [Ruleset](#ruleset) - 7-bag by default.
  - **Repeat this queue** - The specified queue is looped forever.
  - **Replace active block** - The active piece (the piece you are currently controlling) will be also replaced.
  - **Non-terminal last block** - Adds a NONE piece to the end of the queue, so that the game doesn't immediately end after placing all the pieces. Make sure to handle this option appropriately and refill the player's queue.

You can also enable the advanced queue input by clicking on "+ Switch to advanced queue input."

![comp_queue_plus]

**Queue+** allows you to set a queue with pieces that aren't limited to just tetrominoes. In fact, it lets you set up a queue with any piece in the game.

Check the [Block name reference list](#block-name-reference-list) for more info about usable block names.

To set the queue to any piece available in the aforementioned list, use the format:
```
[<set_ID>:<piece_ID>]
```
So for example, `[3:0]` will produce an I piece with Arika Rotation System.

### Condition

![comp_cond]

**Condition** allows you to specify a condition, after fulfilling which (or not) a certain action is triggered.

You can check for various stats:
<details>
<summary>Click here to see available stats</summary>
<ul>
<li> Number of blocks,
<li> Finesse (number of finesse faults),
<li> KPP,
<li> PPS,
<li> APM,
<li> Attack,
<li> T-spins,
<li> Active combo,
<li> Versus score,
<li> Perfect Clears,
<li> TSDs (T-spin Doubles),
<li> Garbage Cleared,
<li> Holds,
<li> B2B,
<li> Wasted Ts,
<li> Lines,
<li> Max Combo,
<li> Singles,
<li> Doubles,
<li> Triples,
<li> Jstrises (quadruples),
<li> Score,
<li> Incoming attack (the height of the red bar),
<li> Time (in seconds)
</ul>
</details>

Then you can compare it with a number - available operators are `>`, `>=`, `=`, `<=`, `<`.

You can also check for a **Custom expression**. Custom expressions require a variable on the left-hand side of the expression.
Custom expressions accept [system variables](#system-variables), [local counters](#local-counters) and [custom](#variable) variables.

For example: To check if a level (custom variable) is higher or equal to 20, a custom expression would look like this:
```
level>=20
```

Fulfilling a condition (or not) can trigger one of the actions:
- Game over - the player loses with an explanation of what condition was not fulfilled.<br>
  **Works only for "If false" conditions - setting this with "If true" condition will cause an error!**
- Successful game end - the player wins, and the usermode is considered completed.
- Run trigger actions - An External/Conditional [Trigger](#trigger) is triggered.

### Variable
![comp_variable]

**Variable** components are very powerful. Variable components allow you to specify a custom variable, and assign an expression to it.

The custom variable name must not be a name of a [system variable](#system-variables) and must be **at most 20 characters long**.
Variable names are case-sensitive.

Variables can be used in custom expressions for the [Condition](#condition) components and as placeholders for [Text](#text) components.

The right hand side of the component accepts [MathJS](https://mathjs.org/) expressions - try out its expression parser to play around.

Expressions can operate on [system variables](#system-variables).

Besides [MathJS](https://mathjs.org/) functions, expressions can also contain [special functions](#special-functions) that affect the board and the queue.

Expressions must fit within a **100-character limit**.

If your usermode goes haywire, you can debug your usermode by doing the following:
- Right-click on the Jstris page in-game and select "Inspect Element..." or hit F12,
- Go to the "Console" tab,
- In the console, if the variable changes, the change should be printed out on the console by `replayer.js`.

This only works for unpublished usermodes.

### Map
![comp_map]

**Map** allows you to manipulate the contents of the board using a specified map.

Click the *Edit map* button to enter the map editor. It functions identically to the Map Designer.

The Map component has two dropdown options that control its behavior:

#### Board manipulation modes:
- **Replace board** - The whole board is replaced by the map.
- **Subtract from current board** - If blocks are present on the board in the same position as in the map, those blocks will be removed from the board.
- **Add to current board (on top)** - The map will be overlaid on top of the board (like a layer in an image editing program). Map blocks take priority over existing board blocks.
- **Add to current board (under)** - The map will be underlaid beneath the board (like a layer in an image editing program). Existing board blocks take priority over map blocks.
- **Intersect with current board (keep stack color)** - All blocks on the board are removed, except in positions where blocks existed in both the board and the map. Block colors from the board are retained.
- **Intersect with current board (force map color)** - Same as above, but block colors are replaced with those from the map.
- **End if map collides with current piece position** - Will end the game as a failure if the map shape collides with the currently active piece. Does not modify the board or piece position.
- **End if map collides with current stack** - Will end the game as a failure if the map shape collides with the current stack (placed blocks). Does not modify the board.

#### Active Block position handling:
After the board is modified by the map (except for the two "End if" modes), you can control what happens to the active piece:

- **Reset to spawn** - The active piece is reset to its default spawn position for that piece type.
- **Move up until no collision** - If the piece is colliding with the modified board, it will be moved upward until it no longer collides. The piece will not move below its spawn height.
- **Closest valid (any direction w/o collision)** - Searches for the closest valid position in all directions (up, down, left, right, and diagonals). The search expands outward from the current position until a collision-free position is found. Piece rotation remains unchanged.
- **Closest valid (any direction except down)** - Same as above, but the piece cannot be moved downward. Only upward, left, right, and upper diagonal movements are allowed.
- **Keep unchanged** - The piece position and rotation remain exactly as they were before the map was applied. Note: This may result in the piece colliding with the modified board.

> **Note:** After any Active Block position adjustment, the lock delay is reset to prevent accidental hard drops.

### Stats

![comp_stats]

**Stats** component allows you to change the statistics displayed below the board.

In order to find out what number to insert into the textbox, open Settings, then navigate to Stats, then check your desired stats.
In the bottom right corner, there's a small number. This number determines what stats to show.
The number is interpreted in binary, so 129 from the example image shows Time (+1) and KPP (+128).

<details>
<summary>Full list of stats</summary>
<ul>
<li> Time (+1)
<li> Score (+2)
<li> Lines (+4)
<li> Attack (+8)
<li> Received (+16)
<li> Finesse (+32)
<li> PPS (+64)
<li> KPP (+128)
<li> APM (+256)
<li> Blocks (+512)
<li> VS (+1024)
<li> Wasted (+2048)
<li> Hold (+4096)
</ul>
</details>
<br>

![stats]

### Text

![comp_text]

**Text** components allow you to insert text into your usermode.
Text components can accept text and **placeholders**.

Placeholders are specified in curly brackets, and can hold [system variables](#system-variables), [local counters](#local-counters) and [custom variables](#variable), 

For example: `{PC}` will insert a number of Perfect Clears performed.

Line breaks can be inserted using `\n` (backslash followed by n) in the text field.

There are four different ways of showing Text (and a fifth one which is not yet implemented):

| Option  |             During Ready-Go (Task spec.)             | Value next to the board (lines remaining position) |                Description text of the value next to the board                 |                              Over the board (lower part)                              |
| ------- | :--------------------------------------------------: | :------------------------------------------------: | :----------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------: |
| Example |                       ![task]                        |                      ![value]                      |                                 ![description]                                 |                                        ![over]                                        |
| Notes   | Always shows "TASK".<br>Accepts line breaks (use `\n`). |                Accepts line breaks (use `\n`)                 | Accepts line breaks (use `\n`).<br>Defaults to "lines remaining" if not provided. | Actually, the text box is in the center of the board.<br>Accepts line breaks (use `\n`). |

### Pause

![comp_pause]

**Pause** components pause the game for a specified period of time in seconds. Useful for quizzes.

There are two options available:
- **Allow skip by pressing any key** - The game unpauses immediately when the player presses any key.
- **Allow some controls** - The player can buffer holds and rotations during the pause.

### Audio

![comp_audio]

**Audio** components play a specified audio clip when executed. Audio components only accept audio clips from https://audio.jezevec10.com (Dallicious voice lines)
and https://s.jezevec10.com (in-game sounds).

<details>
<summary>Available sounds from audio.jezevec10.com - click here</summary>

| Link                                                          | Transcription                                                                       | BGM                       |
| :------------------------------------------------------------ | :---------------------------------------------------------------------------------- | :------------------------ |
| https://audio.jezevec10.com/dal/2/computerintrash.ogg         | Time to throw your whole computer in the trash.                                     | -                         |
| https://audio.jezevec10.com/dal/2/creativewithpolymers.ogg    | You gotta be creative with polymers to clear this one.                              | -                         |
| https://audio.jezevec10.com/dal/2/dontplaythis.ogg            | Don't play this, please.                                                            | -                         |
| https://audio.jezevec10.com/dal/2/everyclearisatspin.ogg      | Every clear is a T-spin.                                                            | -                         |
| https://audio.jezevec10.com/dal/2/hahaha.ogg                  | Ha ha ha ha haaaa!                                                                  | -                         |
| https://audio.jezevec10.com/dal/2/isthisgood.ogg              | Is this good?                                                                       | -                         |
| https://audio.jezevec10.com/dal/2/iwasgoingtosaysomething.ogg | I was going to say something. But I forgot.                                         | -                         |
| https://audio.jezevec10.com/dal/2/levelup1.ogg                | Level up!                                                                           | -                         |
| https://audio.jezevec10.com/dal/2/levelup2.ogg                | Level up!                                                                           | -                         |
| https://audio.jezevec10.com/dal/2/levelup3.ogg                | Level up!                                                                           | -                         |
| https://audio.jezevec10.com/dal/2/peped.ogg                   | Pepe-D emote.                                                                       | -                         |
| https://audio.jezevec10.com/dal/2/takeforever.ogg             | This is gonna take forever.                                                         | -                         |
| https://audio.jezevec10.com/dal/2/terror.ogg                  | Deadly terror. Oh shit.                                                             | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/2/trytosurvive.ogg            | Try to survive.                                                                     | -                         |
| https://audio.jezevec10.com/dal/2/tspinfactory.ogg            | T-spin factory.                                                                     | -                         |
| https://audio.jezevec10.com/dal/2/wellknowsetupwithatwist.ogg | Well-known setup with a twist.                                                      | -                         |
| https://audio.jezevec10.com/dal/aboutto.ogg                   | Because... I... am... about... to do it!                                            | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/alphys.ogg                    | You gonna love this puzzle! It was made by the great Doctor Alphys!                 | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/care.ogg                      | You must care about puzzles like I do!                                              | Snowy (Undertale)         |
| https://audio.jezevec10.com/dal/chanceofvictory.ogg           | Only the tiniest chance of victory will remain.                                     | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/congratulations.ogg           | Congratulations! Good job!                                                          | -                         |
| https://audio.jezevec10.com/dal/cookie.ogg                    | You're such a smart cookie!                                                         | (no idea)                 |
| https://audio.jezevec10.com/dal/corresp1.ogg                  | Hi! I'm Dal! I'm your resident Jstris correspondent!                                | -                         |
| https://audio.jezevec10.com/dal/diao.ogg                      | Who's Diao?                                                                         | -                         |
| https://audio.jezevec10.com/dal/easy.ogg                      | It might be even too easy for you!                                                  | Snowy (Undertale)         |
| https://audio.jezevec10.com/dal/enough.ogg                    | Anyway. That's enough talking.                                                      | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/fair.ogg                      | My puzzles are very fair! And my traps are expertly cooked!                         | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/feelfree.ogg                  | Feel free to try the puzzle yourself!                                               | (no idea)                 |
| https://audio.jezevec10.com/dal/finalChallenge.ogg            | Human! This is your final and most dangerous challenge!                             | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/gauntlet.ogg                  | Behold! The gauntlet of deadly terror!                                              | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/haha.ogg                      | Nyeh heh heh heh heh!                                                               | Snowy (Undertale)         |
| https://audio.jezevec10.com/dal/incredible.ogg                | Incredible. I'm impressed.                                                          | Snowy (Undertale)         |
| https://audio.jezevec10.com/dal/internet.ogg                  | The Internet. I'm quite popular there.                                              | (only Papyrus' SFX)       |
| https://audio.jezevec10.com/dal/looking.ogg                   | What are you looking at?                                                            | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/love.ogg                      | Well, I'm sure you'll love the next puzzle then.                                    | Snowy (Undertale)         |
| https://audio.jezevec10.com/dal/meme/180.ogg                  | One eighty.                                                                         | -                         |
| https://audio.jezevec10.com/dal/meme/aydosmio.ogg             | Aydosmio! *(sic)*                                                                   | -                         |
| https://audio.jezevec10.com/dal/meme/aysobum.ogg              | Ay, so - Boom!                                                                      | -                         |
| https://audio.jezevec10.com/dal/meme/clockwise.ogg            | Clockwise.                                                                          | -                         |
| https://audio.jezevec10.com/dal/meme/combostorm.ogg           | Combooooostooooorm!                                                                 | -                         |
| https://audio.jezevec10.com/dal/meme/congratulations2.ogg     | ♪ Congratulations! ♪                                                                | -                         |
| https://audio.jezevec10.com/dal/meme/congratulations.ogg      | Congratulations!                                                                    | -                         |
| https://audio.jezevec10.com/dal/meme/correspondent.ogg        | I'm Jstris correspondent.                                                           | -                         |
| https://audio.jezevec10.com/dal/meme/counterclockwise.ogg     | Counter-clockwise.                                                                  | -                         |
| https://audio.jezevec10.com/dal/meme/fluteman.ogg             | Fluteman.                                                                           | -                         |
| https://audio.jezevec10.com/dal/meme/frick.ogg                | Frick.                                                                              | -                         |
| https://audio.jezevec10.com/dal/meme/goodjob.ogg              | Good job!                                                                           | -                         |
| https://audio.jezevec10.com/dal/meme/harddrop.ogg             | Hard drop.                                                                          | -                         |
| https://audio.jezevec10.com/dal/meme/h.ogg                    | H.                                                                                  | -                         |
| https://audio.jezevec10.com/dal/meme/hyperion.ogg             | Hyperion.                                                                           | -                         |
| https://audio.jezevec10.com/dal/meme/impissed.ogg             | Now I'm pissed!                                                                     | -                         |
| https://audio.jezevec10.com/dal/meme/izkierda.ogg             | Izkierda. *(sic)*                                                                   | -                         |
| https://audio.jezevec10.com/dal/meme/left.ogg                 | Left.                                                                               | -                         |
| https://audio.jezevec10.com/dal/meme/lockdown.ogg             | Lockdown.                                                                           | -                         |
| https://audio.jezevec10.com/dal/meme/notlikethis.ogg          | Not like this!                                                                      | -                         |
| https://audio.jezevec10.com/dal/meme/ohmygod2.ogg             | Oh my god...                                                                        | -                         |
| https://audio.jezevec10.com/dal/meme/ohmygod.ogg              | Oh my god...                                                                        | -                         |
| https://audio.jezevec10.com/dal/meme/pentris.ogg              | Pentris!                                                                            | -                         |
| https://audio.jezevec10.com/dal/meme/quad.ogg                 | Quad.                                                                               | -                         |
| https://audio.jezevec10.com/dal/meme/right.ogg                | Right.                                                                              | -                         |
| https://audio.jezevec10.com/dal/meme/softdrop.ogg             | Soft drop.                                                                          | -                         |
| https://audio.jezevec10.com/dal/meme/stop.ogg                 | Stop!                                                                               | -                         |
| https://audio.jezevec10.com/dal/meme/teretcha.ogg             | Teretcha. *(sic)*                                                                   | -                         |
| https://audio.jezevec10.com/dal/meme/tetrio.ogg               | [TETR.IO](https://tetr.io).                                                         | -                         |
| https://audio.jezevec10.com/dal/meme/welldone.ogg             | Well done.                                                                          | -                         |
| https://audio.jezevec10.com/dal/meme/yoholdthat.ogg           | Yo, hold that.                                                                      | -                         |
| https://audio.jezevec10.com/dal/mode1-task.ogg                | [Send 23 lines with the next 15 blocks.](https://jstris.jezevec10.com/usermodes/1)  | -                         |
| https://audio.jezevec10.com/dal/mode93-task.ogg               | [Send 23 lines with the next 23 blocks.](https://jstris.jezevec10.com/usermodes/93) | -                         |
| https://audio.jezevec10.com/dal/noway.ogg                     | There's no way they can get past this one.                                          | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/ready.ogg                     | Are you ready?                                                                      | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/shocking.ogg                  | I think you'll find this one... quite shocking!                                     | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/something.ogg                 | By the way - I was going to say something. But I forgot.                            | sans. (Undertale)         |
| https://audio.jezevec10.com/dal/tooeasy.ogg                   | This challenge... it seems... maybe... too easy to defeat the human with!           | Nyeh heh heh! (Undertale) |

</details>
<br>
<details>
<summary>Available sounds from s.jezevec10.com - click here</summary>

TODO: Insert sound list there
</details>

### Attack
![comp_attack]

**Attack** components send garbage to the player when executed.

If separated by commas, the component will send multiple garbage segments at once.

For example: The Attack component in the image above will send a segment of 4 garbage lines and a segment of 2 garbage lines at once.

There are two options available:
- **Specify garbage columns** - You can control in which column each segment spawns. Make sure to include the same amount of values as in the "Lines" textbox!
- **Ensure column switch** - Garbage segment won't spawn on the same column as the previous one.

### Ruleset
![comp_ruleset]

**Ruleset** components change the rules of the game when executed. Rulesets can even be changed mid-game to achieve dynamic difficulty for your usermode.

Check out the [Ruleset specification](#ruleset-specification) for more details.

There's also an option to add the specified ruleset without resetting all options - only rules specified in the ruleset will change.

### Block skin
![comp_skin]

**Block skin** components change the block skin when executed. Block skin components only accept skins from https://i.imgur.com (You can make your custom skin that way)
and https://s.jezevec10.com (built-in skins). Block skins must be in 9:1 proportions.

<details>
<summary>Available skins from s.jezevec10.com - click here</summary>

<b>Free skins</b>

| Link                                | Image                                    |
| ----------------------------------- | ---------------------------------------- |
| https://s.jezevec10.com/res/b1.png  | ![](https://s.jezevec10.com/res/b1.png)  |
| https://s.jezevec10.com/res/b2.png  | ![](https://s.jezevec10.com/res/b2.png)  |
| https://s.jezevec10.com/res/b3.png  | ![](https://s.jezevec10.com/res/b3.png)  |
| https://s.jezevec10.com/res/b4.png  | ![](https://s.jezevec10.com/res/b4.png)  |
| https://s.jezevec10.com/res/b8.png  | ![](https://s.jezevec10.com/res/b8.png)  |
| https://s.jezevec10.com/res/b9.png  | ![](https://s.jezevec10.com/res/b9.png)  |
| https://s.jezevec10.com/res/b10.png | ![](https://s.jezevec10.com/res/b10.png) |
| https://s.jezevec10.com/res/b11.png | ![](https://s.jezevec10.com/res/b11.png) |
| https://s.jezevec10.com/res/b12.png | ![](https://s.jezevec10.com/res/b12.png) |
| https://s.jezevec10.com/res/b13.png | ![](https://s.jezevec10.com/res/b13.png) |

<b>Supporter-only skins</b>

| Link                                     | Image                                         | Author              |
| ---------------------------------------- | --------------------------------------------- | ------------------- |
| https://s.jezevec10.com/res/b/19/1.png   | ![](https://s.jezevec10.com/res/b/19/1.png)   | Tetrian22           |
| https://s.jezevec10.com/res/b/19/2.png   | ![](https://s.jezevec10.com/res/b/19/2.png)   | ElliottB1           |
| https://s.jezevec10.com/res/b/19/3.png   | ![](https://s.jezevec10.com/res/b/19/3.png)   | nathanle1406        |
| https://s.jezevec10.com/res/b/19/4.png   | ![](https://s.jezevec10.com/res/b/19/4.png)   | Hanna               |
| https://s.jezevec10.com/res/b/19/5.png   | ![](https://s.jezevec10.com/res/b/19/5.png)   | Plaaosert           |
| https://s.jezevec10.com/res/b/19/6.png   | ![](https://s.jezevec10.com/res/b/19/6.png)   | minecraft tryhard   |
| https://s.jezevec10.com/res/b/19/7.png   | ![](https://s.jezevec10.com/res/b/19/7.png)   | Preschool Dropout   |
| https://s.jezevec10.com/res/b/19/8.png   | ![](https://s.jezevec10.com/res/b/19/8.png)   | slimenergy          |
| https://s.jezevec10.com/res/b/19/9.png   | ![](https://s.jezevec10.com/res/b/19/9.png)   | slimenergy          |
| https://s.jezevec10.com/res/b/19/10.png  | ![](https://s.jezevec10.com/res/b/19/10.png)  | Imagine Gamer       |
| https://s.jezevec10.com/res/b/19/11.png  | ![](https://s.jezevec10.com/res/b/19/11.png)  | Katakana Letter Tsu |
| https://s.jezevec10.com/res/b/19/12.png  | ![](https://s.jezevec10.com/res/b/19/12.png)  | slimenergy          |
| https://s.jezevec10.com/res/b/19/13.png  | ![](https://s.jezevec10.com/res/b/19/13.png)  | Axarious            |
| https://s.jezevec10.com/res/b/19/14.png  | ![](https://s.jezevec10.com/res/b/19/14.png)  | Dinir               |
| https://s.jezevec10.com/res/b/19/15.png  | ![](https://s.jezevec10.com/res/b/19/15.png)  | DerpyBanana         |
| https://s.jezevec10.com/res/b/19/16.png  | ![](https://s.jezevec10.com/res/b/19/16.png)  | Starwort            |
| https://s.jezevec10.com/res/b/19/17.png  | ![](https://s.jezevec10.com/res/b/19/17.png)  | Starwort            |
| https://s.jezevec10.com/res/b/19/18.png  | ![](https://s.jezevec10.com/res/b/19/18.png)  | misdroppi           |
| https://s.jezevec10.com/res/b/19/19.png  | ![](https://s.jezevec10.com/res/b/19/19.png)  | egguu               |
| https://s.jezevec10.com/res/b/19/20.png  | ![](https://s.jezevec10.com/res/b/19/20.png)  | egguu               |
| https://s.jezevec10.com/res/b/19/21.png  | ![](https://s.jezevec10.com/res/b/19/21.png)  | Q                   |
| https://s.jezevec10.com/res/b/19/22.png  | ![](https://s.jezevec10.com/res/b/19/22.png)  | imAddicted234       |
| https://s.jezevec10.com/res/b/19/25.png  | ![](https://s.jezevec10.com/res/b/19/25.png)  | Lil crump           |
| https://s.jezevec10.com/res/b/19/26.png  | ![](https://s.jezevec10.com/res/b/19/26.png)  | MagnumAlpasan       |
| https://s.jezevec10.com/res/b/19/27.png  | ![](https://s.jezevec10.com/res/b/19/27.png)  | MrTurnip            |
| https://s.jezevec10.com/res/b/19/28.png  | ![](https://s.jezevec10.com/res/b/19/28.png)  | Takane              |
| https://s.jezevec10.com/res/b/19/30.png  | ![](https://s.jezevec10.com/res/b/19/30.png)  | Whole Wheat Orange  |
| https://s.jezevec10.com/res/b/19/31.png  | ![](https://s.jezevec10.com/res/b/19/31.png)  | PixelPelican        |
| https://s.jezevec10.com/res/b/19/32.png  | ![](https://s.jezevec10.com/res/b/19/32.png)  | FerSave             |
| https://s.jezevec10.com/res/b/19/33.png  | ![](https://s.jezevec10.com/res/b/19/33.png)  | OSK                 |
| https://s.jezevec10.com/res/b/19/34.png  | ![](https://s.jezevec10.com/res/b/19/34.png)  | lillod              |
| https://s.jezevec10.com/res/b/19/35.png  | ![](https://s.jezevec10.com/res/b/19/35.png)  | Takane              |
| https://s.jezevec10.com/res/b/19/37.png  | ![](https://s.jezevec10.com/res/b/19/37.png)  | Han \| Dopamine     |
| https://s.jezevec10.com/res/b/19/38.png  | ![](https://s.jezevec10.com/res/b/19/38.png)  | Prismly             |
| https://s.jezevec10.com/res/b/19/39.png  | ![](https://s.jezevec10.com/res/b/19/39.png)  | StayNoided          |
| https://s.jezevec10.com/res/b/19/41.png  | ![](https://s.jezevec10.com/res/b/19/41.png)  | NekoNoTe            |
| https://s.jezevec10.com/res/b/19/42.png  | ![](https://s.jezevec10.com/res/b/19/42.png)  | NekoNoTe            |
| https://s.jezevec10.com/res/b/19/43.png  | ![](https://s.jezevec10.com/res/b/19/43.png)  | GlodRoger           |
| https://s.jezevec10.com/res/b/19/45.png  | ![](https://s.jezevec10.com/res/b/19/45.png)  | Magma_reeen         |
| https://s.jezevec10.com/res/b/19/46.png  | ![](https://s.jezevec10.com/res/b/19/46.png)  | Ok                  |
| https://s.jezevec10.com/res/b/19/47.png  | ![](https://s.jezevec10.com/res/b/19/47.png)  | Ok                  |
| https://s.jezevec10.com/res/b/19/48.png  | ![](https://s.jezevec10.com/res/b/19/48.png)  | Crep                |
| https://s.jezevec10.com/res/b/20/1.png   | ![](https://s.jezevec10.com/res/b/20/1.png)   | Justin1L8           |
| https://s.jezevec10.com/res/b/20/2.png   | ![](https://s.jezevec10.com/res/b/20/2.png)   | DerpyBanana         |
| https://s.jezevec10.com/res/b/20/3.png   | ![](https://s.jezevec10.com/res/b/20/3.png)   | Man.                |
| https://s.jezevec10.com/res/b/20/4.png   | ![](https://s.jezevec10.com/res/b/20/4.png)   | leonid              |
| https://s.jezevec10.com/res/b/20/5.png   | ![](https://s.jezevec10.com/res/b/20/5.png)   | u/KibiByte          |
| https://s.jezevec10.com/res/b/20/6.png   | ![](https://s.jezevec10.com/res/b/20/6.png)   | ColdSpade           |
| https://s.jezevec10.com/res/b/20/7.png   | ![](https://s.jezevec10.com/res/b/20/7.png)   | SmolBepis           |
| https://s.jezevec10.com/res/b/20/8.png   | ![](https://s.jezevec10.com/res/b/20/8.png)   | DrThunderous        |
| https://s.jezevec10.com/res/b/20/9.png   | ![](https://s.jezevec10.com/res/b/20/9.png)   | Tetrian22           |
| https://s.jezevec10.com/res/b/20/10.png  | ![](https://s.jezevec10.com/res/b/20/10.png)  | Kirby703            |
| https://s.jezevec10.com/res/b/20/11.png  | ![](https://s.jezevec10.com/res/b/20/11.png)  | FluxDGTL01          |
| https://s.jezevec10.com/res/b/20/12.png  | ![](https://s.jezevec10.com/res/b/20/12.png)  | ColdSpade           |
| https://s.jezevec10.com/res/b/20/13.png  | ![](https://s.jezevec10.com/res/b/20/13.png)  | darian              |
| https://s.jezevec10.com/res/b/20/14.png  | ![](https://s.jezevec10.com/res/b/20/14.png)  | Kiede               |
| https://s.jezevec10.com/res/b/20/15.png  | ![](https://s.jezevec10.com/res/b/20/15.png)  | izzy1794            |
| https://s.jezevec10.com/res/b/20/16.png  | ![](https://s.jezevec10.com/res/b/20/16.png)  | Tetrian22           |
| https://s.jezevec10.com/res/b/20/18.png  | ![](https://s.jezevec10.com/res/b/20/18.png)  | sock                |
| https://s.jezevec10.com/res/b/20/19.png  | ![](https://s.jezevec10.com/res/b/20/19.png)  | Roxie               |
| https://s.jezevec10.com/res/b/20/20.png  | ![](https://s.jezevec10.com/res/b/20/20.png)  | GeometryMations     |
| https://s.jezevec10.com/res/b/20/21.png  | ![](https://s.jezevec10.com/res/b/20/21.png)  | MrDoubleK           |
| https://s.jezevec10.com/res/b/20/23.png  | ![](https://s.jezevec10.com/res/b/20/23.png)  | GuyWithASword       |
| https://s.jezevec10.com/res/b/20/24.png  | ![](https://s.jezevec10.com/res/b/20/24.png)  | egguu               |
| https://s.jezevec10.com/res/b/20/25.png  | ![](https://s.jezevec10.com/res/b/20/25.png)  | Kiede               |
| https://s.jezevec10.com/res/b/20/26.png  | ![](https://s.jezevec10.com/res/b/20/26.png)  | darian              |
| https://s.jezevec10.com/res/b/20/27.png  | ![](https://s.jezevec10.com/res/b/20/27.png)  | Frodo               |
| https://s.jezevec10.com/res/b/20/28.png  | ![](https://s.jezevec10.com/res/b/20/28.png)  | Frodo               |
| https://s.jezevec10.com/res/b/20/29.png  | ![](https://s.jezevec10.com/res/b/20/29.png)  | Bo Tie              |
| https://s.jezevec10.com/res/b/20/30.png  | ![](https://s.jezevec10.com/res/b/20/30.png)  | Kirby703            |
| https://s.jezevec10.com/res/b/20/31.png  | ![](https://s.jezevec10.com/res/b/20/31.png)  | Bang                |
| https://s.jezevec10.com/res/b/20/32.png  | ![](https://s.jezevec10.com/res/b/20/32.png)  | Tebo_Moi            |
| https://s.jezevec10.com/res/b/20/33.png  | ![](https://s.jezevec10.com/res/b/20/33.png)  | DerpyBanana         |
| https://s.jezevec10.com/res/b/20/34.png  | ![](https://s.jezevec10.com/res/b/20/34.png)  | GeometryMations     |
| https://s.jezevec10.com/res/b/20/35.png  | ![](https://s.jezevec10.com/res/b/20/35.png)  | egguu               |
| https://s.jezevec10.com/res/b/20/36.png  | ![](https://s.jezevec10.com/res/b/20/36.png)  | Kusane              |
| https://s.jezevec10.com/res/b/20/37.png  | ![](https://s.jezevec10.com/res/b/20/37.png)  | ianh                |
| https://s.jezevec10.com/res/b/20/38.png  | ![](https://s.jezevec10.com/res/b/20/38.png)  | Kusane              |
| https://s.jezevec10.com/res/b/20/39.png  | ![](https://s.jezevec10.com/res/b/20/39.png)  | NotLegend           |
| https://s.jezevec10.com/res/b/20/40.png  | ![](https://s.jezevec10.com/res/b/20/40.png)  | NotLegend           |
| https://s.jezevec10.com/res/b/20/41.png  | ![](https://s.jezevec10.com/res/b/20/41.png)  | NotLegend           |
| https://s.jezevec10.com/res/b/20/42.png  | ![](https://s.jezevec10.com/res/b/20/42.png)  | NotLegend           |
| https://s.jezevec10.com/res/b/20/43.png  | ![](https://s.jezevec10.com/res/b/20/43.png)  | NotLegend           |
| https://s.jezevec10.com/res/b/20/44.png  | ![](https://s.jezevec10.com/res/b/20/44.png)  | LanceV              |
| https://s.jezevec10.com/res/b/20/45.png  | ![](https://s.jezevec10.com/res/b/20/45.png)  | DerpyBanana         |
| https://s.jezevec10.com/res/b/20/46.png  | ![](https://s.jezevec10.com/res/b/20/46.png)  | Kusane              |
| https://s.jezevec10.com/res/b/20/47.png  | ![](https://s.jezevec10.com/res/b/20/47.png)  | Oxy                 |
| https://s.jezevec10.com/res/b/20/48.png  | ![](https://s.jezevec10.com/res/b/20/48.png)  | astroskag           |
| https://s.jezevec10.com/res/b/20/49.png  | ![](https://s.jezevec10.com/res/b/20/49.png)  | ColdSpade           |
| https://s.jezevec10.com/res/b/20/50.png  | ![](https://s.jezevec10.com/res/b/20/50.png)  | DerpyBanana         |
| https://s.jezevec10.com/res/b/20/51.png  | ![](https://s.jezevec10.com/res/b/20/51.png)  | Nongo_              |
| https://s.jezevec10.com/res/b/20/53.png  | ![](https://s.jezevec10.com/res/b/20/53.png)  | sm999               |
| https://s.jezevec10.com/res/b/20/54.png  | ![](https://s.jezevec10.com/res/b/20/54.png)  | eight               |
| https://s.jezevec10.com/res/b/20/55.png  | ![](https://s.jezevec10.com/res/b/20/55.png)  | SmolBepis           |
| https://s.jezevec10.com/res/b/20/56.png  | ![](https://s.jezevec10.com/res/b/20/56.png)  | NotLegend           |
| https://s.jezevec10.com/res/b/20/57.png  | ![](https://s.jezevec10.com/res/b/20/57.png)  | mehbark             |
| https://s.jezevec10.com/res/b/20/58.png  | ![](https://s.jezevec10.com/res/b/20/58.png)  | eight               |
| https://s.jezevec10.com/res/b/20/59.png  | ![](https://s.jezevec10.com/res/b/20/59.png)  | Blai8               |
| https://s.jezevec10.com/res/b/20/62.png  | ![](https://s.jezevec10.com/res/b/20/62.png)  | Skyear              |
| https://s.jezevec10.com/res/b/20/63.png  | ![](https://s.jezevec10.com/res/b/20/63.png)  | SatTyler            |
| https://s.jezevec10.com/res/b/20/64.png  | ![](https://s.jezevec10.com/res/b/20/64.png)  | Freeze              |
| https://s.jezevec10.com/res/b/20/65.png  | ![](https://s.jezevec10.com/res/b/20/65.png)  | qbd                 |
| https://s.jezevec10.com/res/b/20/66.png  | ![](https://s.jezevec10.com/res/b/20/66.png)  | ColdSpade           |
| https://s.jezevec10.com/res/b/20/67.png  | ![](https://s.jezevec10.com/res/b/20/67.png)  | Mortee              |
| https://s.jezevec10.com/res/b/20/68.png  | ![](https://s.jezevec10.com/res/b/20/68.png)  | DrThunderous        |
| https://s.jezevec10.com/res/b/20/70.png  | ![](https://s.jezevec10.com/res/b/20/70.png)  | Skyear              |
| https://s.jezevec10.com/res/b/20/71.png  | ![](https://s.jezevec10.com/res/b/20/71.png)  | MitoNabarazaki      |
| https://s.jezevec10.com/res/b/20/72.png  | ![](https://s.jezevec10.com/res/b/20/72.png)  | ImAddicted234       |
| https://s.jezevec10.com/res/b/20/73.png  | ![](https://s.jezevec10.com/res/b/20/73.png)  | menofcrest          |
| https://s.jezevec10.com/res/b/20/74.png  | ![](https://s.jezevec10.com/res/b/20/74.png)  | rytone              |
| https://s.jezevec10.com/res/b/20/75.png  | ![](https://s.jezevec10.com/res/b/20/75.png)  | ColdSpade           |
| https://s.jezevec10.com/res/b/20/76.png  | ![](https://s.jezevec10.com/res/b/20/76.png)  | ColdSpade           |
| https://s.jezevec10.com/res/b/20/77.png  | ![](https://s.jezevec10.com/res/b/20/77.png)  | MitoNabarazaki      |
| https://s.jezevec10.com/res/b/20/78.png  | ![](https://s.jezevec10.com/res/b/20/78.png)  | SmolBepis           |
| https://s.jezevec10.com/res/b/20/79.png  | ![](https://s.jezevec10.com/res/b/20/79.png)  | miopasid            |
| https://s.jezevec10.com/res/b/20/80.png  | ![](https://s.jezevec10.com/res/b/20/80.png)  | DrThunderous        |
| https://s.jezevec10.com/res/b/20/81.png  | ![](https://s.jezevec10.com/res/b/20/81.png)  | imAddicted234       |
| https://s.jezevec10.com/res/b/20/82.png  | ![](https://s.jezevec10.com/res/b/20/82.png)  | artrad001           |
| https://s.jezevec10.com/res/b/20/83.png  | ![](https://s.jezevec10.com/res/b/20/83.png)  | Ukkri6              |
| https://s.jezevec10.com/res/b/20/84.png  | ![](https://s.jezevec10.com/res/b/20/84.png)  | Kirbyrocket         |
| https://s.jezevec10.com/res/b/20/85.png  | ![](https://s.jezevec10.com/res/b/20/85.png)  | egg                 |
| https://s.jezevec10.com/res/b/20/86.png  | ![](https://s.jezevec10.com/res/b/20/86.png)  | SmolBepis           |
| https://s.jezevec10.com/res/b/20/87.png  | ![](https://s.jezevec10.com/res/b/20/87.png)  | SmolBepis           |
| https://s.jezevec10.com/res/b/20/88.png  | ![](https://s.jezevec10.com/res/b/20/88.png)  | wavy_bread          |
| https://s.jezevec10.com/res/b/20/89.png  | ![](https://s.jezevec10.com/res/b/20/89.png)  | wavy_bread          |
| https://s.jezevec10.com/res/b/20/90.png  | ![](https://s.jezevec10.com/res/b/20/90.png)  | GeometryMations     |
| https://s.jezevec10.com/res/b/20/91.png  | ![](https://s.jezevec10.com/res/b/20/91.png)  | FazzBearBoiz        |
| https://s.jezevec10.com/res/b/20/92.png  | ![](https://s.jezevec10.com/res/b/20/92.png)  | asteriskblue        |
| https://s.jezevec10.com/res/b/20/93.png  | ![](https://s.jezevec10.com/res/b/20/93.png)  | mr krabs            |
| https://s.jezevec10.com/res/b/20/95.png  | ![](https://s.jezevec10.com/res/b/20/95.png)  | SmolBepis           |
| https://s.jezevec10.com/res/b/20/96.png  | ![](https://s.jezevec10.com/res/b/20/96.png)  | gattara             |
| https://s.jezevec10.com/res/b/20/97.png  | ![](https://s.jezevec10.com/res/b/20/97.png)  | Tetris Dragon       |
| https://s.jezevec10.com/res/b/20/98.png  | ![](https://s.jezevec10.com/res/b/20/98.png)  | Jonah F.            |
| https://s.jezevec10.com/res/b/20/99.png  | ![](https://s.jezevec10.com/res/b/20/99.png)  | Kirby703            |
| https://s.jezevec10.com/res/b/20/100.png | ![](https://s.jezevec10.com/res/b/20/100.png) | TechnoSpyform1      |
| https://s.jezevec10.com/res/b/20/101.png | ![](https://s.jezevec10.com/res/b/20/101.png) | HARPO               |
| https://s.jezevec10.com/res/b/20/102.png | ![](https://s.jezevec10.com/res/b/20/102.png) | noogai223           |
| https://s.jezevec10.com/res/b/20/103.png | ![](https://s.jezevec10.com/res/b/20/103.png) | andie               |
| https://s.jezevec10.com/res/b/20/104.png | ![](https://s.jezevec10.com/res/b/20/104.png) | DrThunderous        |
| https://s.jezevec10.com/res/b/20/105.png | ![](https://s.jezevec10.com/res/b/20/105.png) | GeolyteGM           |
| https://s.jezevec10.com/res/b/20/112.png | ![](https://s.jezevec10.com/res/b/20/112.png) | Vitey               |

<b>Hidden skins</b>

| Link                               | Image                                   |
| ---------------------------------- | --------------------------------------- |
| https://s.jezevec10.com/res/b5.png | ![](https://s.jezevec10.com/res/b5.png) |

</details>

[Jstris Customization Database](https://docs.google.com/spreadsheets/d/1xO8DTORacMmSJAQicpJscob7WUkOVuaNH0wzkR_X194/htmlview#) contains a list of block skins from various games, official or not, and some user-made skins too.

Use this component only when necessary (for example to give a retro climate to a mode, or when repurposing garbage as targets, or for other creative ways to use blocks).

### Run
![comp_run]

A very simple component that just triggers an External/Conditional [Trigger](#trigger).

The trigger name field supports **placeholders** with curly brackets, just like the [Text](#text) component. This allows you to dynamically select which trigger to run based on [system variables](#system-variables), [local counters](#local-counters), or [custom variables](#variable).

For example: `trigger{level}` will run a trigger named `trigger1` if the `level` variable equals 1, or `trigger2` if it equals 2.

### Relative Trigger
![comp_relative]

**Relative Trigger** components can trigger an External/Conditional [Trigger](#trigger) after:
- A certain amount of time (in seconds) passes...
- A certain amount of pieces were placed...
- A certain amount of lines were cleared...

... since the [Trigger](#trigger) under which this component is present was triggered.

For example: When a certain [Trigger](#trigger) triggers on the 5th line, and there's a Relative Trigger that runs a certain trigger after 4 lines, that trigger will run after clearing the 9th line.

### On/Off
![comp_switch]

**On/Off** components can switch components on and off.

Disabled components or [Triggers](#trigger) won't be executed.

You can toggle multiple components on or off with this component by clicking the (+) button - this will add a new textbox in which an additional component can be turned on or off.

### Random
![comp_random]

**Random** components can execute components or External/Conditional [Triggers](#trigger) at random.

Operates similarly to the [On/Off](#onoff) component.

**This component must have at least 2 options to choose from.**

You can specify the weights for each option by inputting a number after a comma.

# Publishing usermodes

If you are satisfied with your usermode, you can publish it for others to play.

You will be presented with this screen:

![publish]

Enter the mode title, description, and tags. Add tags, separating each tag with a comma.
Please note that line breaks in the description are stripped and won't show up in the mode preview.

The first map from the top of your usermode will be used as a thumbnail. If you wish to have a custom thumbnail that won't appear in the usermode, put the [Map](#map) component under the [Trigger](#trigger) that is set to Never trigger.

You can also customize the leaderboard of your mode.

You can set the leaderboard to:
- Not save anything to the leaderboard (leaderboard disabled),
- Save only the first completed game (further games won't be saved),
- Save every completed game (recommended for competitive modes).

You can change metrics for placing players in the leaderboard, and whether higher or lower scores are better.
Secondary metric will be used if two or more players tie on the primary metric.

You can also set other stats that will be shown in the leaderboard, but won't be used for placing players on the leaderboard.

There's also an option to save scores on game over - useful for survival or endurance-style modes.

# Usermode peculiarities

## System variables

**System variables** are game-reserved variables that hold certain game-related statistics.

They can be used as a placeholder in [Text](#text) components or be a part of an expression for the [Variable](#variable) or [Condition](#condition) components.

| Variable name | Explanation                                        |
| :------------ | :------------------------------------------------- |
| blocks        | Number of pieces placed                            |
| finesse       | Number of finesse faults                           |
| kpp           | Keypresses per piece                               |
| sent          | Number of lines sent                               |
| tspins        | Number of T-spins performed                        |
| combo         | Current combo                                      |
| PC            | Number of Perfect Clears                           |
| TSD           | Number of T-spin **Doubles** performed             |
| time          | Time elapsed                                       |
| APM           | Attack per minute                                  |
| PPS           | Pieces per second                                  |
| VS            | VS Score (Attack + Downstack per 100 seconds)      |
| garbage       | Number of lines containing garbage cleared         |
| hold          | Number of times the player held a piece            |
| B2B           | Number of Back-to-backs performed                  |
| wasted        | Ratio of T pieces used in a T-spin to all T pieces |
| lines         | Number of lines cleared                            |
| maxCombo      | Maximum combo                                      |
| single        | Number of Singles                                  |
| double        | Number of Doubles                                  |
| triple        | Number of Triples                                  |
| jstris        | Number of Jstrises (quadruples)                    |
| redbar        | Number of lines awaiting in queue                  |
| inputs        | Number of inputs (not counting soft drops)         |

## Local counters

**Local counters** are a specific type of [system variables](#system-variables) that hold game statistics, but **only** counting after an External/Conditional [Trigger](#trigger) was triggered.<br>
Local counters are invoked by using the following syntax:
```
<triggerName>.<systemVariable>
```
Local counters can then be used in custom expressions for the [Condition](#condition) components or as a placeholder for [Text](#text) components.

For example: `mission2.jstris` will only count Jstrises performed after the `mission2` trigger was triggered.

## Special functions

Besides MathJS functions, the [Variable](#variable) component's expression can also hold certain functions that affect the board and the next queue.

### `getBoard`

The function can be performed with two syntax variations:

- `getBoard()`<br>
  Returns: A 20x10 MathJS matrix containing the board state.

  ![getBoard]

  
- `getBoard(x, y)`<br>
  Parameters:
  - x: Column, integer between 0 and 9
  - y: Row, integer between 0 and 19

  Returns: An integer between 0 and 9 which represents the color of the block at the specified coordinates.

  ![board]

### `setBoard`
- `setBoard(x, y, color)`<br>
  Parameters:
  - x: Column, integer between 0 and 9
  - y: Row, integer between 0 and 19
  - color: Block color, integer between 0 and 9

  Returns: 1 on success, 0 on failure (index out of bounds, color does not exist).

> ⚠️ This function does not update the board visually! Use a blank [Map](#map) with "Add to current board" to update the board.

### `queueReplace`
- `queueReplace(index, piece)`<br>
  Parameters:
  - index - Integer, starting from -1.<br>
    Index -1 replaces the active piece, 0 and higher replace the Next queue.
  - piece - A string representing a piece. Check the [Block name reference list](#block-name-reference-list) for the list of usable pieces.
  `"[setID:pieceID]"` can be used to pick any piece from the game.
- `queueReplace(index, setID, pieceID)`<br>
  Alternative syntax with 3 numeric parameters.

  Returns: 1 on success, 0 on failure (queue index out of bounds, piece does not exist).

### `queueAppend`
- `queueAppend(piece)`<br>
  Parameters:
  - piece - A string representing a piece. Check the [Block name reference list](#block-name-reference-list) for the list of usable pieces.
  `"[setID:pieceID]"` can be used to pick any piece from the game.
- `queueAppend(setID, pieceID)`<br>
   Alternative syntax with 2 numeric parameters.

  Returns: 1 on success, 0 on failure (piece does not exist).

### `getX`
- `getX()`<br>
  Returns: The current X position of the active piece (integer between 0 and 9).

### `getY`
- `getY()`<br>
  Returns: The current Y position of the active piece (integer between spawn height and 19).

### `getRot`
- `getRot()`<br>
  Returns: The current rotation of the active piece (integer between 0 and 3).

### `getBlockName`
- `getBlockName()`<br>
  Returns: A string representing the current active piece in `"[setID:pieceID]"` format (e.g., `"[0:2]"` for T piece).

### `getBlock`
- `getBlock()`<br>
  Returns: A MathJS matrix `[setID, pieceID]` representing the current active piece (e.g., `[0, 2]` for T piece).
  
  This function is useful for mathematical operations in MathJS expressions since matrices are easier to work with than strings.
  
  Example usage:
  ```
  block = getBlock()
  setID = block[1]    # Get first element (setID)
  pieceID = block[2]  # Get second element (pieceID)
  ```

### `isCollision`
- `isCollision(x, y, rot)`<br>
  Parameters:
  - x: Column, integer between 0 and 9
  - y: Row, integer between spawn height and 19
  - rot: Rotation, integer between 0 and 3

  Returns: 1 if the active piece would collide at the specified position and rotation, 0 if the position is valid.

  This function temporarily tests the collision without modifying the actual piece state.

### `setX`
- `setX(x)`<br>
  Parameters:
  - x: Column, integer between 0 and 9

  Returns: 1 on success, 0 on failure (out of bounds).

  Sets the X position of the active piece and updates the ghost piece.

### `setY`
- `setY(y)`<br>
  Parameters:
  - y: Row, integer between spawn height and 19

  Returns: 1 on success, 0 on failure (out of bounds).

  Sets the Y position of the active piece and updates the ghost piece.

### `setRot`
- `setRot(rot)`<br>
  Parameters:
  - rot: Rotation, integer between 0 and 3

  Returns: 1 on success, 0 on failure (invalid rotation).

  Sets the rotation of the active piece and updates the ghost piece.

### `setPos`
- `setPos(x, y, rot)`<br>
  Parameters:
  - x: Column, integer between 0 and 9
  - y: Row, integer between spawn height and 19
  - rot: Rotation, integer between 0 and 3

  Returns: 1 on success, 0 on failure (any parameter out of bounds).

  Sets the position and rotation of the active piece and updates the ghost piece.

### `setBlock`
- `setBlock(blockName)`<br>
  Parameters:
  - blockName: A string representing a piece. Check the [Block name reference list](#block-name-reference-list) for the list of usable pieces.
  `"[setID:pieceID]"` can be used to pick any piece from the game.
- `setBlock(setID, pieceID)`<br>
  Alternative syntax with 2 numeric parameters.

  Returns: 1 on success, 0 on failure (piece does not exist).

  Replaces the active piece with the specified piece and updates the ghost piece.

### `setToSpawnPos`
- `setToSpawnPos()`<br>
  Returns: 1 (always succeeds).

  Resets the active piece to its default spawn position and updates the ghost piece.

### `moveToWall`
- `moveToWall(dir)`<br>
  Parameters:
  - dir: Direction, integer -1 (left) or 1 (right)

  Returns: 1 on success, 0 on failure (invalid direction).

  Moves the active piece horizontally until it hits a wall or obstacle stack (effectively a DAS activation).

### `hardDrop`
- `hardDrop()`<br>
  Returns: 1 (always succeeds).

  Immediately drops the active piece to the bottom of the playfield, locking it in place. Next piece in the queue becomes active.

### `rotate`
- `rotate(dir)`<br>
  Parameters:
  - dir: Rotation direction, integer -1 (counter-clockwise), 1 (clockwise), or 2 (180 degrees)

  Returns: 1 on success, 0 on failure (invalid direction).

  Rotates the active piece in the specified direction.

### `holdBlock`
- `holdBlock()`<br>
  Returns: 1 (always succeeds).

  Swaps the active piece with the piece in hold. If hold is empty, the active piece is moved to hold and the next piece becomes active. Can be used only once until hard drop is used (otherwise the function does nothing).

### `moveX`
- `moveX(dir)`<br>
  Parameters:
  - dir: Horizontal movement distance, integer between -10 and 10 (negative moves left, positive moves right)

  Returns: The actual number of steps the piece moved (integer between 0 and the absolute value of dir).

  Moves the active piece horizontally by the specified number of steps. The piece will stop moving if it hits a wall or obstacle before completing all steps. Returns the number of steps actually moved.

## Ruleset specification
### `attackTable`
**Type**: Array of integers with 11 elements

Specifies the number of lines sent for a specified line clear.

| Index         |          0          |   1    |   2    |   3    |   4    |        5         |        6         |        7         |           8           |        9         |    10     |
| ------------- | :-----------------: | :----: | :----: | :----: | :----: | :--------------: | :--------------: | :--------------: | :-------------------: | :--------------: | :-------: |
| Line clear    | 0 lines<br>(unused) | Single | Double | Triple | Jstris | T-spin<br>Double | T-spin<br>Triple | T-spin<br>Single | Mini T-spin<br>Single | Perfect<br>Clear | B2B bonus |
| Default value |          0          |   0    |   1    |   2    |   4    |        4         |        6         |        2         |           0           |        10        |     1     |

Default: `[0,0,1,2,4,4,6,2,0,10,1]`

### `comboTable`
**Type**: Array of integers with 13 elements

Specifies the number of additional lines sent for a specified combo.
The last index applies for 12-combo and greater.

| Index (combo) |   0   |   1   |   2   |   3   |   4   |   5   |   6   |   7   |   8   |   9   |  10   |  11   |  12   |
| ------------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Default value |   0   |   0   |   1   |   1   |   1   |   2   |   2   |   3   |   3   |   4   |   4   |   4   |   5   |

Default: `[0,0,1,1,1,2,2,3,3,4,4,4,5]`

### `hasHold`
**Type**: Boolean

Controls, whether the player can use Hold.

Default: `true`

### `sgProfile`
**Type**: Array of Doubles

Specifies delays between solid garbage additions.
After all of the previous delays inserted their garbage, the last value in the array is repeated.

Default: `[0,3]`

### `clearDelay`
**Type**: Integer

Specifies the amount of time (in ms) after a line clear in which the game is paused. The player can buffer rotations and holds during that pause.

Default: `0`

### `gravityLvl`
**Type**: Integer between 0 and 28

Specifies how fast pieces fall on their own.

<details>
<summary>Gravity table - click here</summary>

| Level | Period<a href="#fn:1"><sup id="fnref:1">[1]</sup></a> | Rows<a href="#fn:2"><sup id="fnref:2">[2]</sup></a> | G<a href="#fn:3"><sup id="fnref:3">[3]</sup></a> |
| ----- | ----------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------ |
| 0     | ∞ ms                                                  | 1                                                   | 0                                                |
| 1     | 900 ms                                                | 1                                                   | 0.018                                            |
| 2     | 850 ms                                                | 1                                                   | 0.02                                             |
| 3     | 800 ms                                                | 1                                                   | 0.021                                            |
| 4     | 750 ms                                                | 1                                                   | 0.022                                            |
| 5     | 700 ms                                                | 1                                                   | 0.024                                            |
| 6     | 650 ms                                                | 1                                                   | 0.026                                            |
| 7     | 600 ms                                                | 1                                                   | 0.028                                            |
| 8     | 550 ms                                                | 1                                                   | 0.03                                             |
| 9     | 500 ms                                                | 1                                                   | 0.033                                            |
| 10    | 450 ms                                                | 1                                                   | 0.037                                            |
| 11    | 400 ms                                                | 1                                                   | 0.042                                            |
| 12    | 350 ms                                                | 1                                                   | 0.048                                            |
| 13    | 300 ms                                                | 1                                                   | 0.056                                            |
| 14    | 250 ms                                                | 1                                                   | 0.067                                            |
| 15    | 200 ms                                                | 1                                                   | 0.083                                            |
| 16    | 150 ms                                                | 1                                                   | 0.111                                            |
| 17    | 100 ms                                                | 1                                                   | 0.167                                            |
| 18    | 50 ms                                                 | 1                                                   | 0.333                                            |
| 19    | 45 ms                                                 | 1                                                   | 0.37                                             |
| 20    | 40 ms                                                 | 1                                                   | 0.417                                            |
| 21    | 35 ms                                                 | 1                                                   | 0.476                                            |
| 22    | 30 ms                                                 | 1                                                   | 0.556                                            |
| 23    | 25 ms                                                 | 1                                                   | 0.667                                            |
| 24    | 20 ms                                                 | 1                                                   | 0.833                                            |
| 25    | 30 ms                                                 | 2                                                   | 1.111                                            |
| 26    | 20 ms                                                 | 2                                                   | 1.667                                            |
| 27    | 33 ms                                                 | 3                                                   | 1.515                                            |
| 28    | 0 ms                                                  | 21                                                  | 20                                               |

<p id="fn:1">[1]: The period after which the piece falls the specified amount of rows. <a href="#fnref:1">↑</a></p>
<p id="fn:2">[2]: The amount of rows the piece falls per period. <a href="#fnref:2">↑</a></p>
<p id="fn:3">[3]: The approximate amount of rows a piece falls every 1/60 s. <a href="#fnref:3">↑</a></p>

</details>

Default: `1`

### `garbageDelay`

**Type**: Integer between 0 and 60000

Specifies after how long (in ms) since receiving a garbage segment that segment can be added to the board.

Default: `500`

### `lockDelay`

**Type**: Array of integers between 0 and 20,000,000 with 3 elements

Specifies different levels of lock delay.

| Index         |                             0                              |                                         1                                          |                   2                   |
| ------------- | :--------------------------------------------------------: | :--------------------------------------------------------------------------------: | :-----------------------------------: |
| Lock delay    |                             L1                             |                                         L2                                         |                  L3                   |
| Info          | For how long the piece can stay on the ground without locking. | For how long the piece can stay on the ground while moving left/right without locking. | For how long the piece can be active. |
| Default value |                           500 ms                           |                                      5000 ms                                       |               20000 ms                |

Default: `[500,5000,20000]`

### `mess`

**Type**: Integer between -100 and 100

Specifies the chance for garbage to change columns both between segments and in segment.

- `-100` is 0% messiness between segments and 0% messiness in segment,
- Negative values are `100+mess`% messiness between segments and 0% messiness in segment,
- `0` is 100% messiness between segments and 0% messiness in segment,
- Positive values are 100% messiness between segments and `mess`% messiness in segment,
- `100` is 100% messiness between segments and 100% messiness in segment.

Default: `0`

### `gapW`

**Type**: Integer between 1 and 8

Specifies the width of the garbage hole.

Default: `1`

### `allSpin`

**Type**: Integer between 0 and 2

Specifies allowed spins:

- `0`: T-spins,
- `1`: Immobile all-spin,
- `2`: 4-point all-spin.

Default: `0`

### `asEx`

**Type**: String specifying up to 6 tetrominoes separated by commas

All-spin exclusion list - applicable only when `allSpin` is not 0. Specifies which pieces can't perform spins when all-spin is enabled.

For example, `"T,J"` will prevent T and J pieces from performing spins.

Default: `""`

### `gInv`

**Type**: Boolean

If true, garbage lines will be inverted - where there would be blocks, there will be empty spaces, and vice versa.

Default: `false`

### `solidAtk`

**Type**: Boolean

If true, garbage lines will consist of solid hurry-up garbage lines.

Default: `false`

### `blocksSel`

**Type**: Integer between 0 and 8

Specifies the block set used in the game.

If changed mid-game, pieces from the new set will appear at the end of the queue,
since Jstris always keeps 5 pieces in queue, regardless of the number of previews shown to the player. 

Available block sets:

0. Standard
1. Big (moves 2 spaces left/right at a time)
2. Big (moves 1 space left/right at a time)
3. ARS
4. Penta
5. M123
6. All-29
7. C2RS
8. O-spin

Default: `0`

### `rndSel`

**Type**: Integer between 0 and 10

Specifies the randomizer.

Available randomizers:

| Index | Randomizer  | Explanation                                                              |
| :---- | :---------- | :----------------------------------------------------------------------- |
| 0     | 7-bag       | One of each tetromino in a bag                                           |
| 1     | 14-bag      | Two of each tetromino in a bag                                           |
| 2     | Classic     | Actually a memoryless randomizer.                                        |
| 3     | One Block   | One piece is randomized and given throughout the entire game             |
| 4     | Two Block   | Two different pieces are randomized and given throughout the entire game |
| 5     | One 7-bag   | The same 7-bag looped forever                                            |
| 6     | One 14-bag  | The same 14-bag looped forever                                           |
| 7     | C2Sim       | Simulation of the Cultris II randomizer                                  |
| 8     | Repeat+7b   | 7-bag but repeats one piece at random                                    |
| 9     | BSblock+7b  | 7-bag but inserts a non-tetromino or a big block into the bag at random  |
| 10    | BigBlock+7b | 7-bag but inserts a big block into the bag at random                     |

Default: `0`

### `gblockSel`

**Type**: Integer between 0 and 3

Specifies the garbage blocking method.

Available garbage blocking methods:

0. Full (can offset garbage, garbage isn't inserted while in combo)
1. Limited (can offset garbage, garbage can be inserted while in combo)
2. None (can't offset garbage, garbage can be inserted while in combo)
3. Instant (garbage is inserted the moment it's received)

Default: `0`

### `prSel`

**Type**: Integer between 0 and 5

Specifies the number of previews available to the player.

Default: `5`

### `clearLines`

**Usermode exclusive!**

**Type**: Boolean

Specifies whether full lines are cleared or not.

Default: `true`

### `DAS`

**Type**: Integer between -1 and 5000

Enforces specified DAS value. If DAS is `-1`, the user setting is used.

Default: `-1`

### `ARR`

**Type**: Integer between -1 and 5000

Enforces specified ARR value. If ARR is `-1`, the user setting is used.

Default: `-1`

### `ghost`

**Type**: Integer between -1 and 1

Enforces the presence (or lack) of the ghost piece.

Available settings:

<ol start="-1">
  <li>User setting is used.</li>
  <li>Ghost is disabled.</li>
  <li>Ghost is enabled.</li>
</ol>

Default: `-1`

### `scoreMult`

**Usermode exclusive!**

**Type**: Double between 0 and 1000

Specifies the score multiplier.

If the score change would end up being decimal, the score change gets rounded to the nearest integer.

Default: `1`

### `disableAllUserControls`

**Usermode exclusive!**

**Type**: Boolean

Specifies whether all user controls are disabled so that the player can only use the usermode's controls (key-triggers).
This includes all movement controls and user-defined reset key. The user must reset the game using default reset key F4 (we do not prevent the function keys F2 to F12).

Default: `false`

## Block name reference list

### Set 0: Standard

| Piece ID   |   0   |   1   |   2   |   3   |   4   |   5   |   6   |
| ---------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Image      | ![I]  | ![O]  | ![T]  | ![L]  | ![J]  | ![S]  | ![Z]  |
| Piece name |   I   |   O   |   T   |   L   |   J   |   S   |   Z   |

### Set 1: Big, moves 2 spaces left/right at a time

| Piece ID   |    0     |    1     |    2     |    3     |    4     |    5     |    6     |
| ---------- | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| Image      | ![big_I] | ![big_O] | ![big_T] | ![big_L] | ![big_J] | ![big_S] | ![big_Z] |
| Piece name |    -     |    -     |    -     |    -     |    -     |    -     |    -     |

### Set 2: Big, moves 1 space left/right at a time

| Piece ID   |    0     |    1     |    2     |    3     |    4     |    5     |    6     |
| ---------- | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| Image      | ![big_I] | ![big_O] | ![big_T] | ![big_L] | ![big_J] | ![big_S] | ![big_Z] |
| Piece name |    BI    |    BO    |    BT    |    BL    |    BJ    |    BS    |    BZ    |

### Set 3: Arika Rotation System

| Piece ID   |    0     |    1     |    2     |    3     |    4     |    5     |    6     |
| ---------- | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| Image      | ![ars_I] | ![ars_O] | ![ars_T] | ![ars_L] | ![ars_J] | ![ars_S] | ![ars_Z] |
| Piece name |    -     |    -     |    -     |    -     |    -     |    -     |    -     |


### Set 4: Pentominoes

| Piece ID      |   0   |   1   |   2   |   3   |   4   |   5   |
| ------------- | :---: | :---: | :---: | :---: | :---: | :---: |
| Image         | ![I5] | ![V5] | ![T5] | ![U]  | ![W]  | ![X]  |
| Piece name    |  I5   |  V5   |  T5   |  U5   |  W5   |  X5   |
| Also known as |   -   |   -   |   -   |   U   |   W   |   X   |

| Piece ID      |   6   |   7   |      8      |   9   |  10   |     11      |
| ------------- | :---: | :---: | :---------: | :---: | :---: | :---------: |
| Image         | ![J5] | ![L5] | ![N_mirror] | ![N]  | ![Y]  | ![Y_mirror] |
| Piece name    |  J5   |  L5   |     S5      |  Z5   |  TL   |     TJ      |
| Also known as |   -   |   -   |     N'      |   N   |   Y   |     Y'      |

| Piece ID      |  12   |  13   |  14   |     15      |  16   |  17   |
| ------------- | :---: | :---: | :---: | :---------: | :---: | :---: |
| Image         | ![P]  | ![Q]  | ![F]  | ![F_mirror] | ![Z5] | ![S5] |
| Piece name    |  OZ   |  OS   |  TS   |     TZ      |  LL   |  JJ   |
| Also known as |   P   |   Q   |   F   |     F'      |  Z5   |  S5   |

### Set 5: M123

| Piece ID      |   0   |   1   |   2   |   3   |
| ------------- | :---: | :---: | :---: | :---: |
| Image         | ![O1] | ![I2] | ![I3] | ![V3] |
| Piece name    |  I1   |  I2   |  I3   |  L3   |
| Also known as |  O1   |   -   |   -   |  V3   |

### Set 6: All-29
All-29 does not contain any pieces.

### Set 7: Cultris II Rotation System

| Piece ID   |   0   |   1   |   2   |   3   |   4   |   5   |   6   |
| ---------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Image      | ![I]  | ![O]  | ![T]  | ![L]  | ![J]  | ![S]  | ![Z]  |
| Piece name |   -   |   -   |   -   |   -   |   -   |   -   |   -   |

### Set 8: O-spin Rotation System

| Piece ID   |   0   |   1   |   2   |   3   |   4   |   5   |   6   |
| ---------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Image      | ![I]  | ![O]  | ![T]  | ![L]  | ![J]  | ![S]  | ![Z]  |
| Piece name |   -   |  O+   |   -   |   -   |   -   |   -   |   -   |

### Set 9: NONE

Handle this set with care, as those pieces are made out of hurry-up garbage.<br>
These pieces are invisible in queue and in hold.

| Piece ID   |    0    |    1    |
| ---------- | :-----: | :-----: |
| Image      | ![NONE] | ![NONE] |
| Piece name |   INV   |  NONE   |

[access_usermodes]: ./images/access_usermodes.png "How to access usermodes"
[usermodes_tab]: ./images/usermodes_tab.png "The usermode tab"
[editor]: ./images/editor.png "The usermode editor"
[mode_example]: ./images/mode_example.png "An example of a usermode"
[comp_trigger]: ./images/comp_trigger.png "The Trigger component"
[comp_queue]: ./images/comp_queue.png "The Queue component"
[comp_queue_plus]: ./images/comp_queue_plus.png "The Queue component with advanced queue input capabilities"
[comp_cond]: ./images/comp_cond.png "The Condition component"
[comp_variable]: ./images/comp_variable.png "The Variable component"
[comp_map]: ./images/comp_map.png "The Map component"
[comp_stats]: ./images/comp_stats.png "The Stats component"
[comp_text]: ./images/comp_text.png "The Text component"
[comp_pause]: ./images/comp_pause.png "The Pause component"
[comp_audio]: ./images/comp_audio.png "The Audio component"
[comp_attack]: ./images/comp_attack.png "The Attack component"
[comp_ruleset]: ./images/comp_ruleset.png "The Ruleset component"
[comp_skin]: ./images/comp_skin.png "The Block Skin component"
[comp_run]: ./images/comp_run.png "The Run component"
[comp_relative]: ./images/comp_relative.png "The Relative Trigger component"
[comp_switch]: ./images/comp_switch.png "The On/Off (Component Switch) component"
[comp_random]: ./images/comp_random.png "The Random component"

[I]: ./images/pieces/I.png "I tetromino"
[O]: ./images/pieces/O.png "O tetromino"
[T]: ./images/pieces/T.png "T tetromino"
[L]: ./images/pieces/L.png "L tetromino"
[J]: ./images/pieces/J.png "J tetromino"
[S]: ./images/pieces/S.png "S tetromino"
[Z]: ./images/pieces/Z.png "Z tetromino"
[big_I]: ./images/pieces/big_I.png "Big I tetromino"
[big_O]: ./images/pieces/big_O.png "Big O tetromino"
[big_T]: ./images/pieces/big_T.png "Big T tetromino"
[big_L]: ./images/pieces/big_L.png "Big L tetromino"
[big_J]: ./images/pieces/big_J.png "Big J tetromino"
[big_S]: ./images/pieces/big_S.png "Big S tetromino"
[big_Z]: ./images/pieces/big_Z.png "Big Z tetromino"
[ars_I]: ./images/pieces/ars_I.png "I tetromino with Arika Rotation System"
[ars_O]: ./images/pieces/O.png "O tetromino with Arika Rotation System"
[ars_T]: ./images/pieces/ars_T.png "T tetromino with Arika Rotation System"
[ars_L]: ./images/pieces/ars_L.png "L tetromino with Arika Rotation System"
[ars_J]: ./images/pieces/ars_J.png "J tetromino with Arika Rotation System"
[ars_S]: ./images/pieces/ars_S.png "S tetromino with Arika Rotation System"
[ars_Z]: ./images/pieces/ars_Z.png "Z tetromino with Arika Rotation System"
[I5]: ./images/pieces/I5.png "I pentomino"
[V5]: ./images/pieces/V5.png "V pentomino"
[T5]: ./images/pieces/T5.png "T pentomino"
[U]: ./images/pieces/U.png "U pentomino"
[W]: ./images/pieces/W.png "W pentomino"
[X]: ./images/pieces/X.png "X pentomino"
[J5]: ./images/pieces/J5.png "J pentomino"
[L5]: ./images/pieces/L5.png "L pentomino"
[N_mirror]: ./images/pieces/N_mirror.png "Mirror of the N pentomino"
[N]: ./images/pieces/N.png "N pentomino"
[Y]: ./images/pieces/Y.png "Y pentomino"
[Y_mirror]: ./images/pieces/Y_mirror.png "Mirror of the Y pentomino"
[P]: ./images/pieces/P.png "P pentomino"
[Q]: ./images/pieces/Q.png "Q pentomino"
[F]: ./images/pieces/F.png "F pentomino"
[F_mirror]: ./images/pieces/F_mirror.png "Mirror of the F pentomino"
[Z5]: ./images/pieces/Z5.png "Z pentomino"
[S5]: ./images/pieces/S5.png "S pentomino"
[O1]: ./images/pieces/O1.png "Monomino"
[I2]: ./images/pieces/I2.png "Domino"
[I3]: ./images/pieces/I3.png "I tromino"
[V3]: ./images/pieces/V3.png "V tromino"
[NONE]: ./images/pieces/NONE.png "Blank piece"
[stats]: ./images/stats.png "Stats settings with an arrow pointing at a number 129"
[task]: ./images/text/task.png "During Ready-Go (Task spec.)"
[value]: ./images/text/value.png "Value next to the board (lines remaining position)"
[description]: ./images/text/description.png "Description text of the value next to the board"
[over]: ./images/text/over.png "Over the board (lower part)"
[getBoard]: ./images/getBoard.png "The matrix obtained after using the getBoard function"
[board]: ./images/board.png "Jstris board with X and Y values written outside of the board"
[publish]: ./images/publish.png "The publish screen"
