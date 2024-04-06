# Jstris Usermode Guide

**Table of Contents**
- [Jstris Usermode Guide](#jstris-usermode-guide)
  - [Getting started](#getting-started)
  - [Editor](#editor)
  - [Components](#components)
    - [Trigger](#trigger)
    - [Queue](#queue)
  - [Block name reference list](#block-name-reference-list)

- - - 
## Getting started

Usermodes allow players to create their own custom gamemodes and share them with other players.

To get started, go to your Account Settings, then in the "Other tab" check the Experiments toggle.

Please note that you need to have at least 10 hours of playtime on your account or be a Supporter to be able to access Usermodes.

![][access_usermodes]

After enabling experimental features, a new tab called "Usermodes" should be available.

![][usermodes_tab]

Choose "Create" to create your first usermode, or "Browse" to explore usermodes created by other players.

## Editor

After choosing "Create", you will be presented with the Usermode Editor.

![][editor]

Drag and drop components from the sidebar to the component area, or click on components to put them on the bottom of your usermode.

## Components

Usermodes are constructed by putting components together, starting with a "Trigger" component, that triggers the components put below it, from top to bottom.

If you put your component in wrong place, you can always drag it somewhere else by dragging the component's title bar.

![][mode_example]

While hovering over a component with a mouse cursor, extra options are available:
- An ON/OFF switch,
- Green (+) - duplicates a component and puts it below the current component when pressed,
- Red (-) - removes the component.

Each component gets an ID assigned to it when added (unless it's duplicated) - these IDs are used for the [On/Off](#on-off) component and the [Random](#random) component.

### Trigger

![][comp_trigger]

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
![][comp_queue]

**Queue** components allow you to replace a queue with your own fixed queue.

Be aware that if the finite queue runs out of pieces, the game is over, no matter whether there's a piece in Hold or not.

Type the tetromino block names in the "Queue" field to set up the queue.

There are four options available:
  - **Allow refill if queue is used** - After all the pieces from the queue are used up, the game keeps dealing new pieces according to the [Ruleset](#ruleset) - 7-bag by default.
  - **Repeat this queue** - The specified queue is looped forever.
  - **Replace active block** - The active piece (the piece you are currently controlling) will be also replaced.
  - **Non-terminal last block** - Adds a NONE piece to the end of the queue, so that the game doesn't immediately end after placing all the pieces. Make sure to handle this option appropriately and refill the player's queue.

You can also enable the advanced queue input by clicking on "+ Switch to advanced queue input."

![][comp_queue_plus]

**Queue+** allows you to set a queue with pieces that aren't limited to just tetrominoes. In fact, it lets you set up a queue with any piece in the game.

Check the [Block name reference list](#block-name-reference-list) for more info about usable block names.

To set the queue to any piece available in the aforementioned list, use the format:
```
[<set_ID>:<piece_ID>]
```
So for example, `[3:0]` will produce an I piece with Arika Rotation System.

## Block name reference list

**Set 0: Standard**

| Piece ID   |   0    |   1    |   2    |   3    |   4    |   5    |   6    |
| ---------- | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| Image      | ![][I] | ![][O] | ![][T] | ![][L] | ![][J] | ![][S] | ![][Z] |
| Piece name |   I    |   O    |   T    |   L    |   J    |   S    |   Z    |

**Set 1: Big, moves 2 spaces left/right at a time**

| Piece ID   |     0      |     1      |     2      |     3      |     4      |     5      |     6      |
| ---------- | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
| Image      | ![][big_I] | ![][big_O] | ![][big_T] | ![][big_L] | ![][big_J] | ![][big_S] | ![][big_Z] |
| Piece name |     -      |     -      |     -      |     -      |     -      |     -      |     -      |

**Set 2: Big, moves 1 space left/right at a time**

| Piece ID   |     0      |     1      |     2      |     3      |     4      |     5      |     6      |
| ---------- | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
| Image      | ![][big_I] | ![][big_O] | ![][big_T] | ![][big_L] | ![][big_J] | ![][big_S] | ![][big_Z] |
| Piece name |     BI     |     BO     |     BT     |     BL     |     BJ     |     BS     |     BZ     |

**Set 3: Arika Rotation System**

| Piece ID   |     0      |     1      |     2      |     3      |     4      |     5      |     6      |
| ---------- | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
| Image      | ![][ars_I] | ![][ars_O] | ![][ars_T] | ![][ars_L] | ![][ars_J] | ![][ars_S] | ![][ars_Z] |
| Piece name |     -      |     -      |     -      |     -      |     -      |     -      |     -      |


**Set 4: Pentominoes**
| Piece ID      |    0    |    1    |    2    |   3    |   4    |   5    |
| ------------- | :-----: | :-----: | :-----: | :----: | :----: | :----: |
| Image         | ![][I5] | ![][V5] | ![][T5] | ![][U] | ![][W] | ![][X] |
| Piece name    |   I5    |   V5    |   T5    |   U5   |   W5   |   X5   |
| Also known as |    -    |    -    |    -    |   U    |   W    |   X    |

| Piece ID      |    6    |    7    |       8       |   9    |   10   |      11       |
| ------------- | :-----: | :-----: | :-----------: | :----: | :----: | :-----------: |
| Image         | ![][J5] | ![][L5] | ![][N_mirror] | ![][N] | ![][Y] | ![][Y_mirror] |
| Piece name    |   J5    |   L5    |      S5       |   Z5   |   TL   |      TJ       |
| Also known as |    -    |    -    |      N'       |   N    |   Y    |      Y'       |

| Piece ID      |   12   |   13   |   14   |      15       |   16    |   17    |
| ------------- | :----: | :----: | :----: | :-----------: | :-----: | :-----: |
| Image         | ![][P] | ![][Q] | ![][F] | ![][F_mirror] | ![][Z5] | ![][S5] |
| Piece name    |   OZ   |   OS   |   TS   |      TZ       |   LL    |   JJ    |
| Also known as |   P    |   Q    |   F    |      F'       |   Z5    |   S5    |

**Set 5: M123**
| Piece ID      |    0    |    1    |    2    |    3    |
| ------------- | :-----: | :-----: | :-----: | :-----: |
| Image         | ![][O1] | ![][I2] | ![][I3] | ![][V3] |
| Piece name    |   I1    |   I2    |   I3    |   L3    |
| Also known as |   O1    |    -    |    -    |   V3    |

**Set 6: All-29** does not contain any pieces.

**Set 7: Cultris II Rotation System**

| Piece ID   |   0    |   1    |   2    |   3    |   4    |   5    |   6    |
| ---------- | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| Image      | ![][I] | ![][O] | ![][T] | ![][L] | ![][J] | ![][S] | ![][Z] |
| Piece name |   -    |   -    |   -    |   -    |   -    |   -    |   -    |

**Set 8: O-spin Rotation System**

| Piece ID   |   0    |   1    |   2    |   3    |   4    |   5    |   6    |
| ---------- | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| Image      | ![][I] | ![][O] | ![][T] | ![][L] | ![][J] | ![][S] | ![][Z] |
| Piece name |   -    |   O+   |   -    |   -    |   -    |   -    |   -    |

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
