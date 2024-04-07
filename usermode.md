# Jstris Usermode Guide

**Table of Contents**
- [Jstris Usermode Guide](#jstris-usermode-guide)
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
  - [Block name reference list](#block-name-reference-list)

- - - 
## Getting started

Usermodes allow players to create their own custom gamemodes and share them with other players.

To get started, go to your Account Settings, then in the "Other tab" check the Experiments toggle.

Please note that you need to have at least 10 hours of playtime on your account or be a Supporter to be able to access Usermodes.

![access_usermodes]

After enabling experimental features, a new tab called "Usermodes" should be available.

![usermodes_tab]

Choose "Create" to create your first usermode, or "Browse" to explore usermodes created by other players.

## Editor

After choosing "Create", you will be presented with the Usermode Editor.

![editor]

Drag and drop components from the sidebar to the component area, or click on components to put them on the bottom of your usermode.

## Components

Usermodes are constructed by putting components together, starting with a "Trigger" component, that triggers the components put below it, from top to bottom.

If you put your component in wrong place, you can always drag it somewhere else by dragging the component's title bar.

![mode_example]

While hovering over a component with a mouse cursor, extra options are available:
- An ON/OFF switch,
- Green (+) - duplicates a component and puts it below the current component when pressed,
- Red (-) - removes the component.

Each component gets an ID assigned to it when added (unless it's duplicated) - these IDs are used for the [On/Off](#on-off) component and the [Random](#random) component.

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
- **At specific time** - triggers when a certain amount of time passes from the start of the game.
- **On each block** - triggers after placing a block, when next block appears, after line clears were processed.
- **On each lineclear** - triggers after any line clear.
- **On specific block #** - triggers once after a certain amount of blocks was placed.
- **On specific # line cleared** - triggers once after you cleared more than # lines.
- **Key down** - triggers when a key is pressed.
- **Key up** - triggers when a key is released.<br>
  Key up and Key down triggers react to a specified key code. You can use [this keycode utility](https://www.toptal.com/developers/keycode) to determine the key code of your desired key.<br>
  Key up and Key down triggers also accept an option to prevent the default action when a player has that key bound.
- **Variable changes** - triggers when a [variable](#variable) changes. Does not support [built-in variables](#built-in-variables).
- **Never** - does not trigger.
- **External/Conditional** - you can set your own external trigger name for [Condition](#condition), [Run](#run), [Relative Trigger](#relative-trigger), [On/Off](#on-off) or a [Random](#random) component to trigger.<br>
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

You can also check for a **Custom expression**. Custom expressions require a variable on the left hand side of the expression.
Custom expressions accept [built-in variables](#built-in-variables), [local counters](#local-counters) and [custom](#variable) variables.

For example: To check if a level (custom variable) is higher or equal to 20, a custom expression would look like this:
```
level>=20
```

Fulfilling a condition (or not) can trigger one of the actions:
- Game over - the player loses with an explanation, what condition was not fulfilled.<br>
  **Works only for "If false" conditions - setting this with "If true" condition will cause an error!**
- Successful game end - the player wins, and the usermode is considered completed.
- Run trigger actions - An [External/Conditional Trigger](#trigger) is triggered.

### Variable
![comp_variable]

**Variable** components are very powerful. Variable components allow you to specify a custom variable, and assign an expression to it.

The custom variable name must not be a name of a [built-in variable](#built-in-variables) and must be **at most 20 characters long**.
Variable names are case-sensitive.

Variables can be used in custom expressions for the [Condition](#condition) components and as placeholders for [Text](#text) components.

The right hand side of the component accepts [MathJS](https://mathjs.org/) expressions - try out its expression parser to play around.

Expressions can operate on [built-in variables](#built-in-variables).

Besides [MathJS](https://mathjs.org/) functions, expressions can also contain [special functions](#special-functions) that affect the board and the queue.

Expressions must fit within a **100-character limit**.

### Map
![comp_map]

**Map** allows you to manipulate the contents of the board using a specified map.

Click the *Edit map* button to enter the map editor. It functions identically to the Map Designer.

Maps can manipulate the board in various ways:
- **Replace board** - the whole board is replaced by a map,
- **Subtract from current board** - If blocks are present on the board in the same position as in the map, the blocks will be removed.
- **Add to current board (on top)** - The map will be overlaid on top of the board (like a layer in an image editing program).
- **Add to current board (under)** The map will be underlain under the board (like a layer in an image editing program).
- **Intersect with current board (keep stack color)** - All blocks on the map are removed, except in positions where there were blocks in the map. Block colors on the board are retained.
- **Intersect with current board (force map color)** - Same as above, but block colors are replaced with those from the map.
- **Replace & end if collision found**

### Stats

![comp_stats]

**Stats** component allows you to change the statistics displayed below the board.

In order to find out, what number to insert into the textbox, open Settings, then navigate to Stats, then check your desired stats.
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

## Text

**Text** components allow you to insert text into your usermode.
Text components can accept text and **placeholders**.

Placeholders are specified in curly brackets, and can hold [built-in variables](#built-in-variables), [local counters](#local-counters) and [custom variables](#variable), 

For example: `{PC}` will insert a number of Perfect Clears performed.

There are four different ways of showing Text (and fifth one which is not yet implemented):

| Option  |             During Ready-Go (Task spec.)             | Value next to the board (lines remaining position) |                Description text of the value next to the board                 |                              Over the board (lower part)                              |
| ------- | :--------------------------------------------------: | :------------------------------------------------: | :----------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------: |
| Example |                       ![task]                        |                      ![value]                      |                                 ![description]                                 |                                        ![over]                                        |
| Notes   | Always shows "TASK".<br>Does not accept line breaks. |                Accepts line breaks                 | Does not accept line breaks.<br>Defaults to "lines remaining" if not provided. | Actually, the text box is in the center of the board.<br>Does not accept line breaks. |

## Pause

**Pause** components pause the game for a specified period of time in seconds. Useful for quizzes.

There are two options available:
- **Allow skip by pressing any key** - The game unpauses immediately when the player presses any key.
- **Allow some controls** - The player can buffer holds and rotations during the pause.

## Audio

**Audio** components play a specified audio clip when executed. Audio components only accept audio clips from https://audio.jezevec10.com (Dallicious voice lines)
and https://s.jezevec10.com (in-game sounds).

<details>
<summary>Available sounds from audio.jezevec10.com</summary>

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
| https://audio.jezevec10.com/dal/internet.ogg                  | The Internet. I'm quite popular there.                                              | (only Bonetrousle's SFX)  |
| https://audio.jezevec10.com/dal/looking.ogg                   | What are you looking at?                                                            | Nyeh heh heh! (Undertale) |
| https://audio.jezevec10.com/dal/love.ogg                      | Well, I'm sure you'll love the next puzzle then.                                    | Snowy (Undertale)         |
| https://audio.jezevec10.com/dal/meme/180.ogg                  | One eighty.                                                                         | -                         |
| https://audio.jezevec10.com/dal/meme/aydosmio.ogg             | Aydosmio!                                                                           | -                         |
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
| https://audio.jezevec10.com/dal/meme/izkierda.ogg             | Izkierda.                                                                           | -                         |
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
| https://audio.jezevec10.com/dal/meme/teretcha.ogg             | Teretcha.                                                                           | -                         |
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

## Block name reference list

**Set 0: Standard**

| Piece ID   |   0   |   1   |   2   |   3   |   4   |   5   |   6   |
| ---------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Image      | ![I]  | ![O]  | ![T]  | ![L]  | ![J]  | ![S]  | ![Z]  |
| Piece name |   I   |   O   |   T   |   L   |   J   |   S   |   Z   |

**Set 1: Big, moves 2 spaces left/right at a time**

| Piece ID   |    0     |    1     |    2     |    3     |    4     |    5     |    6     |
| ---------- | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| Image      | ![big_I] | ![big_O] | ![big_T] | ![big_L] | ![big_J] | ![big_S] | ![big_Z] |
| Piece name |    -     |    -     |    -     |    -     |    -     |    -     |    -     |

**Set 2: Big, moves 1 space left/right at a time**

| Piece ID   |    0     |    1     |    2     |    3     |    4     |    5     |    6     |
| ---------- | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| Image      | ![big_I] | ![big_O] | ![big_T] | ![big_L] | ![big_J] | ![big_S] | ![big_Z] |
| Piece name |    BI    |    BO    |    BT    |    BL    |    BJ    |    BS    |    BZ    |

**Set 3: Arika Rotation System**

| Piece ID   |    0     |    1     |    2     |    3     |    4     |    5     |    6     |
| ---------- | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| Image      | ![ars_I] | ![ars_O] | ![ars_T] | ![ars_L] | ![ars_J] | ![ars_S] | ![ars_Z] |
| Piece name |    -     |    -     |    -     |    -     |    -     |    -     |    -     |


**Set 4: Pentominoes**
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

**Set 5: M123**
| Piece ID      |   0   |   1   |   2   |   3   |
| ------------- | :---: | :---: | :---: | :---: |
| Image         | ![O1] | ![I2] | ![I3] | ![V3] |
| Piece name    |  I1   |  I2   |  I3   |  L3   |
| Also known as |  O1   |   -   |   -   |  V3   |

**Set 6: All-29** does not contain any pieces.

**Set 7: Cultris II Rotation System**

| Piece ID   |   0   |   1   |   2   |   3   |   4   |   5   |   6   |
| ---------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Image      | ![I]  | ![O]  | ![T]  | ![L]  | ![J]  | ![S]  | ![Z]  |
| Piece name |   -   |   -   |   -   |   -   |   -   |   -   |   -   |

**Set 8: O-spin Rotation System**

| Piece ID   |   0   |   1   |   2   |   3   |   4   |   5   |   6   |
| ---------- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Image      | ![I]  | ![O]  | ![T]  | ![L]  | ![J]  | ![S]  | ![Z]  |
| Piece name |   -   |  O+   |   -   |   -   |   -   |   -   |   -   |

[access_usermodes]: ./images/access_usermodes.png "How to access usermodes"
[usermodes_tab]: ./images/usermodes_tab.png "The usermode tab"
[editor]: ./images/editor.png "The usermode editor"
[mode_example]: ./images/mode_example.png "An example of a usermode"
[comp_trigger]: ./images/comp_trigger.png "The Trigger component"
[comp_queue]: ./images/comp_queue.png "The Queue component"
[comp_queue_plus]: ./images/comp_queue_plus.png "The Queue component with advanced queue input capabilities"
[comp_cond]: ./images/comp_cond.png "The Condtion component"
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
[comp_relative]: ./images/comp_replative.png "The Relative Trigger component"
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
[stats]: ./images/stats.png "Stats settings with an arrow pointing at a number 129"
[task]: ./images/text/task.png "During Ready-Go (Task spec.)"
[value]: ./images/text/value.png "Value next to the board (lines remaining postion)"
[description]: ./images/text/description.png "Description text of the value next to the board"
[over]: ./images/text/over.png "Over the board (lower part)"
