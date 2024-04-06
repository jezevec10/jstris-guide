# Jstris Usermode Guide

**Table of Contents**
- [Jstris Usermode Guide](#jstris-usermode-guide)
  - [Getting started](#getting-started)
  - [Editor](#editor)
  - [Components](#components)
    - [Trigger](#trigger)

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



[access_usermodes]: ./images/access_usermodes.png "How to access usermodes"
[usermodes_tab]: ./images/usermodes_tab.png "The usermode tab"
[editor]: ./images/editor.png "The usermode editor"
[mode_example]: ./images/mode_example.png "An example of a usermode"
[comp_trigger]: ./images/comp_trigger.png "The Trigger component"
[comp_queue]: ./images/comp_queue.png "The Queue component"
[comp_queue_plus]: ./images/comp_queue_plus.png "The Queue component with extended input capabilities"
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
