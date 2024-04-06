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

**Triggers** are the starting point

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
