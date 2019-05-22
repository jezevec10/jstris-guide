# Jstris Guide

Welcome to Jstris, a simple online multiplayer block game. Jstris is known for its fast gameplay and is attracting talented players from all around the world. This guide will introduce you to the basic features of the game.

- - -

**Table of Contents**

- [Overview](#overview)
- [Controls](#controls)
- [Multiplayer](#multiplayer)
  - [Default Room](#default-room)
  - [Bot Room](#bot-room)
  - [1v1 Room](#1v1-room)
  - [Bot 1v1 Room](#bot-1v1-room)
  - [Slow Room](#slow-room)
  - [Map Room](#map-room)
  - [Team Room](#team-room)
- [Singleplayer](#singleplayer)
  - [Sprint](#sprint)
  - [Cheese Race](#cheese-race)
  - [Ultra](#ultra)
  - [Survival](#survival)
  - [Maps](#maps)
- [Configuration](#configuration)
  - [Attack and Combo table](#attack-and-combo-table)
  - [Garbage Distribution](#garbage-distribution)
  - [Garbage Blocking](#garbage-blocking)
  - [Randomizer](#randomizer)
  - [Previews](#previews)
  - [Solid Garbage](#solid-garbage)
  - [Clear Delay](#clear-delay)
  - [Garbage Delay](#garbage-delay)
  - [Messiness](#messiness)
  - [Configuration presets](#configuration-presets)
  - [Mode](#mode)
- [Frequently Asked Questions](#faq)
  - [Q: Can I add a bot to my private or custom room?](#q-can-i-add-a-bot-to-my-private-or-custom-room)
  - [Q: What do those abbreviations in the Game Results table mean?](#q-what-do-those-abbreviations-in-the-game-results-table-mean)
  - [Q: What is DAS?](#q-what-is-das)
  - [Q: What is ARR?](#q-what-is-arr)
  - [Q: What is finesse?](#q-what-is-finesse)
  - [Q: Can I create a private room?](#q-can-i-create-a-private-room)
  - [Q: Can I play Jstris offline?](#q-can-i-play-jstris-offline)
- [Additional Information](#additional-information)

- - -

## Overview

Jstris uses the same basic mechanics as most other block games. It follows guideline rules. One notable feature is its extensive use of replays. In every single game mode you play in and complete, a replay will be generated for you. Watching and analyzing yourself is an integral part to self-improvement, and Jstris’s replays makes doing that all too easy.

Unlike other sites, you can be sure Jstris’s Leaderboards are completely clean and cheater-free. Moderators will remove suspicious records to ensure a trusworthy list of global achievements. 

It is possible to play without registering, but in order to use all features of the website, it is recommended to create an account. To do so, click on *Register* at the top right corner. Only an email, username, and password is required. With an account, you can see a multitude of statistics including your Best Times in singleplayer modes, multiplayer stats, improvement stats, replays, and much more. You can now also see yourself on the Leaderboard (unregistered users’ scores are excluded). 

![introduction][image2]
- - -

## Controls

Jstris allows for players to customize their controls at any time in the **Settings** menu that is located underneath the main play area. Default controls are as follows:

|   Command    | Default Key |
| ------------ | ----------- |
| Move Left    | left        |
| Move Right   | right       |
| Soft Drop    | down        |
| Hard Drop    | space       |
| Rotate Left  | z           |
| Rotate right | up          |
| Rotate 180   | a           |
| Hold         | c           |

## Multiplayer

### Default Room

Upon entering the site, all players are immediately thrown into the **Default Room**, a free-for-all where you'll find players of all skill levels.   

Playing in the Default Room can be tough! What’s unique about Jstris is that it throws humble beginners and world-class opponents together into the mix, along with everyone else between. If you get tired from playing and simply want to watch, then use the command `/spectate` or `/spec`. To play again, use the command `/play`. 

### Bot Room

The Default Room isn’t the only room there is. To view the full room list, click on *Lobby* in the bottom left of your playfield. The 2nd most popular room on Jstris is usually the **Bot Room**, so named because of the one Bot that is always present. It is always located in the top left corner of all your opponents, easily distinguishable by its uniform red color.

![MisaMino bot in opponents view][image4]

There are 4 different bots in Jstris. Here they are listed by strength, and the commands to change to that specific one, entered into the textbox.

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (removed on 2018.09.21)
- ~~Fool bot: `/changeBot fool`~~ (removed on 2018.09.21)

*\*Note that all commands must be entered in between games. Any command entered during a game will be nullified.*

Misamino is by far the strongest bot, perhaps the strongest block placing bot ever created yet. When paired with the maximum 5 PPS (pieces per second), it becomes a formidable opponent that can easily dismantle the strongest human players in a 1v1. However, bot performance suffers when there are >5 humans in the Bot Room, and it is likely to top out immediately. This brings us to our next command:  /botPPS.

The speed of the bot can be changed. To do this, type in `/bot ?` only replace the ? with any number between .3 and 5. For example, if I wanted the bot to play at 2 PPS, I would type in `/bot 2`. If I wanted the bot to play at 1.73 PPS, I would type in `/bot 1.73`. 

### 1v1 Room

The **1v1 Room** room has a maximum of 2 playing users, although anyone is free to come and watch even if it’s full. Use this room to settle differences with your friends or to battle it out with a worthy player. If you’re keeping score, and you want to reset it, type in `/resetCounter` and all scores will be reset to 0.

### Bot 1v1 Room

A room to 1v1 the Bot. 

### Slow Room

Want to play with a friend but the skill level between yourselves is too great? Or you’re just getting started and tired of losing instantly in the pro-dominated Bot Room? Or you want to improve efficiency in your game by taking speed out of the equation? There’s a Slow Room in place for all those occasions. The default Slow Room's speed limit is set at 2.0 PPS, which means a player cannot go over 2.0 PPS. Any attempts to go faster will result in the player’s screen being temporarily locked. In addition to the speed limit, the Slow Room has a line clear delay of 700 milliseconds. That means for each line(s) you clear, you will have to wait 700 ms before you can play again. All Slow Rooms are indicated by the little speedometer icon - [SPEEDOMETER_ICON]. Custom Slow rooms can have any speed limit from 0 PPS to 20 PPS. 

![the lobby, where you can join and create rooms][image5]

### Map Room

The **Map Room** is a place to downstack the fastest through randomly-chosen, user-created maps. The (D=?%) displayed next to each map is the difficulty percentile of the map, with 0% being the easiest and 100% being the hardest. Maps with Perfect Clear Finish requirement are not included among the Maps. 

### Team Room

The final default room is the **Team Room**. Pick a side, red or blue, and battle and bring glory for your team. 

![team game in progress][image11]

- - -

## Singleplayer

### Sprint

The foundation, and with the most simple objective, **Sprint** is the most popular singleplayer mode on Jstris. Clear X amount of lines as fast as you can. Jstris offers 20, 40, 100, and 1000 line Sprint modes. 

### Cheese Race

Less brash and more analytical than Sprint, **Cheese Race** requires more thinking as you downstack through garbage lines in the most efficient way. Jstris offers 10, 18, 100, and infinity line Cheese Race modes.

### Ultra

Score-focused and rewarding advanced techniques such as t-spins and back-to-backs, **Ultra** is a great way to improve your attacking prowess for use in multiplayer. 

### Survival

Quite possibly the most challenging of the singleplayer modes, **Survival** is much like Cheese Race only the garbage rises at a constant rate of one line per second. Survive against the rising lines for as long as you can. 

### Maps

In late 2018, the **Maps** mode was introduced to Jstris. Maps brings an element of creativity while also preparing players to downstack effectively in difficult and unusual positions. Create your own map in the *Map Designer*. Once published, anyone in the world can play it and compete for the fastest time. There is a limit of 5 published maps per day and 10 unpublished maps in queue. Maps also has a leaderboard. On every map, three medals are given, Gold for 1st place, Silver for 2nd place, and Bronze for 3rd place. Score in the top three of any map to win some medals and secure your place on the leaderboard! 

*\*Note that the Maps leaderboards updates only a few times each day, so new changes are not immediate.*

- - -

## Configuration

To see the configuration of any room on Jstris, use the command `/config`. Now we will go over each of the settings. 

### Attack and Combo table

The default attack and combo table in Jstris (which can be customized in private rooms) is as follows:

| Attack Type        | Lines Sent |   | Combo # | Lines Sent |
| :----------------- | ---------: | - | ------: | ---------: |
| 0 lines            |      **0** |   |       0 |      **0** |
| 1 lines (single)   |      **0** |   |       1 |      **0** |
| 2 lines (double)   |      **1** |   |       2 |      **1** |
| 3 lines (triple)   |      **2** |   |       3 |      **1** |
| 4 lines            |      **4** |   |       4 |      **1** |
| T-spin Double      |      **4** |   |       5 |      **2** |
| T-spin Triple      |      **6** |   |       6 |      **2** |
| T-spin Single      |      **2** |   |       7 |      **3** |
| T-spin Mini Single |      **0** |   |       8 |      **3** |
| Perfect Clear      |     **10** |   |       9 |      **4** |
| Back-to-Back       |     **+1** |   |      10 |      **4** |
|                    |            |   |      11 |      **4** |
|                    |            |   |     12+ |      **5** |

### Garbage Distribution

There are 4 different systems in how garbage is sent around during multiplayer matches. They are as follows:

- Targets `/set garbage targets`
- Divide `/set garbage divide`
- To all `/set garbage toAll`
- To least `/set garbage toLeast`

**Targets** is always the default (except in the Team Room) and by far the most popular. In Targets, a target is rotated around every opponent in the room, in equal and fixed increments, and whoever the target was landed on at the moment you send garbage is the one who gets that garbage you sent. 

In the **Divide** garbage distribution system (GDS), any garbage you send is equally divided among all players. For example, in a room with 2 other opponents, if you send a T-spin Double (4 lines), each of your opponents will get 2 lines. 

In the **To all** GDS, any garbage you send is sent to every player in the room. For example, in a room with 4 opponents, if you send a Perfect Clear (10 lines), all 4 opponents will recieve 10 lines each, or a total of 40 lines. As you can surmise from the example, rooms with To all garbage tend to be hectic, with fast rising garbage and characteristically short games. 

In the **To least** GDS, garbage you send is sent to the player who had *recieved* the least garbage so far. For example, in a room with 3 other opponents, you send 4 lines. Opponent A received 50 lines in the game already at the moment you sent the attack. Opponent B received 53. Opponent C received 58. Because Opponent A received the least lines so far, the 4 lines from your line clear will be sent to him.

In the **To most** GDS, garbage you send is sent to the player who had *sent* the most garbage so far. In essence, you are attacking the strongest player in the room.  

In the **To self** GDS, garbage you send is sent to yourself. Impractical in multiplayer, but one might find it helpful to practice with it alone. 

In the **Random** GDS, garbage you send is sent to any random player. Arguably the most fair GDS.

In the **Roulette** GDS, garbage you send is sent to any random player, *including yourself*.

### Garbage Blocking

There are 4 types of garbage blocking systems on Jstris. They are:

- Full
- Limited
- None
- Instant

**Full** is the default blocking system on Jstris. Other clients that use Full are *TF* (e+ rooms) and *TOP*. Under the Full garbage blocking system, incoming garbage appears as a red bar to your right. It doesn’t rise up on your playfield, however, until you place a piece down. The incoming garbage can be reduced with sent lines (such as a 4 lines) and, if you have already started a combo, will pause completely until you finish the combo.

**Limited** blocking system is very similar to Full but with one difference. Incoming garbage is inserted as soon as you drop a piece, regardless of whether a combo was started already or not. In other words, incoming garbage does not pause during combos the way Full does. Like in Full, incoming garbage can be reduced with sent lines. Clients that use Limited include *PPT* and *TB* and *TF* (non e+ rooms).

In the **None** blocking system, garbage can never be reduced or cancelled. Incoming garbage will first appear as a red bar (like in Full and Limited) and then be inserted into your playfield as soon as you drop a piece. If an opponent sends you 10 lines, even if you clear 4 lines as your next piece, the garbage will not reduce to 6. Instead, you will still recieve 10 lines while sending 4 to your opponent. 

In the **Instant** blocking system, there is no red bar at all. The moment an opponent sends an attack, its garbage will rise up on your field. There is no blocking it. 

|         | Red bar (queue) | Blocking? |
| ------- | :-------------: | :-------: |
| Full    |       Yes       |    Yes    |
| Limited |       Yes       |    Yes    |
| None    |       Yes       |    No     |
| Instant |       No        |    No     |

### Randomizer

Randomizers are basically the formula for what and what order blocks you get. Jstris has 4 different randomizers. They are:

- 7-bag
- 14-bag
- Classic
- One Block

**7-bag** is the standard and default randomizer. Imagine a small bag with 1 each of the 7 different blocks. Now you draw out, one by one, a piece until the bag is empty. Then you get a new bag with again 1 each of the 7 different blocks. Now you draw out one by one once more. Repeat. This is how the 7-bag randomizer works. 

**14-bag** is much like 7-bag only the bag is doubled in size, with 2 of each of the 7 blocks. Once again, you draw out each piece from the bag, one by one, until the bag is empty. Rinse and repeat. 

**Classic** randomizer gives you completely random pieces. This randomizer makes stacking very challenging.

**One Block** is perhaps the oddest randomizer of them all. A randomly selected block is chosen for you at the start and you will get only that specific block for the whole game. 

### Previews

Jstris has a default of 5 previews. In custom rooms, you can set anywhere from 0 to 5 previews. 

### Solid Garbage

Solid garbage are unclearable lines that rise up from the bottom to “hurry up” the game so it doesn’t extend indefinitely. They are slightly darker than normal garbage lines. In the Bot Room, solid garbage by default starts to come after 2 minutes. Solid garbage is also customizable in custom rooms.

![Solid Garbage][image7]

### Clear Delay

Clear delay is a fixed amount of time that passes after you clear any line(s). During this time, you can’t do anything. Many classic block games and PPT use clear delay, but Jstris by default has 0 delay, and for the most part it is never used here. However, it is customizable if you want to turn it on. Its range is 0 milliseconds to 6000 milliseconds.

### Garbage Delay

Garbage delay is a fixed amount of time between the incoming garbage indicated by the red bar and the insertion of that garbage into the playfield. By default, it is set at 500 milliseconds. It is customizable from a range of 0 milliseconds to 1000 milliseconds. A higher garbage delay allows for more pieces to be played before garbage is inserted, while a lower garbage delay allows for less pieces to be played before garbage insertion. Or in other words, the higher the garbage delay, the more opportunity it gives to block more effectively. Another way to define garbage delay is “the minimumum amount of time an incoming attack has to be visible in the red bar before a placed block can trigger the insertion of that garbage to the playfield.”

### Messiness

Garbage messiness refers to the difficulty level to clear certain types of garbage. To change the messiness of garbage in a room, use the command `/set messiness ?`, where the ? is replaced with any number from -100 to 100. -100 is the least messy garbage configuration, and the garbage hole will only appear in one column throughout the entirety of the game (left picture). 100 is the most messy garbage configuration and the garbage hole will appear in any of the 10 columns, making it much more difficult to downstack (right picture).

![Unmessy (-100)][image10] 
![Messy (100)][image1]

### Configuration presets

If there is a room settings configuration you particularly like and want to easily refer back to, you can save the settings as a preset.

To do this, go to *Lobby*, then *Create Room*, then either the *Simple* or *All* tab. Once you have customized the settings to your liking, hit the *Save* button at the bottom right corner to generate your preset data. Copy it, then paste it in the box next to Preset data on the [Submit a preset](/presets/submit) page.

Once you’ve submitted the preset, you can view it, along with all other user-submitted presets on the [List of presets](/presets). Now you can easily recreate the same room without customizing all the settings again. Just go to *Create Room*, then *Use Custom Preset*, and enter either the title or ID number of your preset. 

### Mode

There are currently 7 different modes to choose from when creating a new room. They are:

- Standard
- Team
- Cheese
- Live Sprint
- Live Cheese
- Live Survival
- Live Maps v0.1

**Standard** mode is normal multiplayer free-for-all. 

**Team** mode creates a custom Team Room. To set your own team name, use the command `/set teamName ?` where the ? is replaced with your team name. 

**Cheese** mode creates a Cheese Room. Cheese, also known as garbage, is the primary way to knock out opponents in multiplayer modes. It is an important skill to downstack through cheese. Practice how fast you can downstack in this mode that starts games with 10 lines of garbage. First to reach the bottom wins. 10 lines too easy for you? Adjust the amount of starting lines with the command `/set height ?` , with the question mark representing a number from 1 to 20.

**Live Sprint** mode allows you to play Sprint against an opponent(s). The fastest one to finish the Sprint wins. The room defaults to a 40L Sprint, but you can change to any other type of Sprint with these commands:

- 20L:     `/set gamemode sprint20`
- 40L:     `/set gamemode sprint40`
- 100L:    `/set gamemode sprint100`
- 1000L:   `/set gamemode sprint1000`

If you break your Sprint record in Live Sprint, unfortunately you cannot add it to your account because the Sprint will be contained in a Live Replay, not a standard Replay. But you can still save the replay to your favorites if you want to preserve it.

**Live Cheese** mode allows you to play Cheese against an opponent(s). Live Cheese mode is virtually identical to Cheese mode except that you can't customize starting lines beyond the 10L, 18L, and 100L. The room defaults to a 10L Cheese, but you can change to any other type of Cheese with these commands:

- 10L:     `/set gamemode cheese10`
- 18L:     `/set gamemode cheese18`
- 100L:    `/set gamemode cheese100`

**Live Survial** mode allows you to play Survival against an opponent(s). Whoever survives the longest wins.

**Live Maps v0.1** mode creates a custom Map Room. Everything in this room works the same as the Map Room. 

## FAQ

### Q: Can I add a bot to my private or custom room?

A: No. Currently, we only have one bot on Jstris, which permanently resides in the Bot Room. However, private bots may be a reality in the future.

### Q: What do those abbreviations in the Game Results table mean?

A: B2B = back-to-back. B2Bpm = back-to-back per minute. APM = attack per minute. SPM = sent per minute. PPS = pieces per second. Rep = replay.

![game results table][image9]

### Q: What is DAS?

A: DAS is a form of horizontal piece sensitivity. DAS stands for delayed auto shift. It controls for how long you have to hold down the left or right keys before the block moves to the direction you want. With a very low DAS, even the lightest touch on a key will immediately send the block moving. With a very high DAS, you will have to hold down the key for longer before the block starts moving. Professionals on average tend to use a lower DAS because the increased sensitivity allows them to play faster. The default DAS on Jstris is 133. If it still feels too sensitive, raise that number until you feel comfortable. If it feels too slow, lower the number. Adjust and find what suits you.

### Q: What is ARR?

A: ARR is another form of horizontal piece sensitivity. ARR stands for auto repeat rate. It controls for how fast the block moves left or right. This is a little easier to understand than DAS. Quite simply, with a very low ARR, blocks will zoom almost immediately to the direction you want when holding down the left or right keys. With a very high ARR, blocks will move very slowly in the direction you want when holding down the left or right keys. The default ARR on Jstris is 10. 

### Q: What is finesse?

A: Finesse is defined as the most efficient way to move a block. Good finesse is important for playing smoother and faster. The number next to finesse denotes how many finesse errors were committed. So a 0 finesse score means you made no finesse errors.  Ideally, the closer you get to 0, the better. Finesse is something that needs to be learned in order to know how to do. There are many resources online explaining it. This video is a good starting point: [Tutorial: How to Play Fast!](https://youtu.be/_QBs703nOnk?t=502).

### Q: Can I create a private room?

A: Yes. Click *Lobby*, then *Create Room*, then check the box that says *Private*. Copy and give the room link to anyone you want to join your private room. Here’s a tip: grab the link of any room, public or private, by using the command `/link`.

### Q: Can I play Jstris offline?

A: Yes. In order to play offline, you have to first download Jstris while you are online. To do this, right click on the home page, press "Save as", and download the html file. Note that only single player modes can be played offline, and the scores will not be saved.

- - -

## Additional Information

Jstris runs entirely on donations. There are no advertisements whatsoever. Due to the considerable amount of stored replays and game data, a powerful server is required to run Jstris. All donations are much appreciated and will help keep Jstris running - see the [About](/about) section on the website to learn more.

[image2]: ./images/guide-intro.png "introduction"
[image4]: ./images/image4.png "MisaMino bot in opponents view"
[image8]: ./images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ./images/image5.png "the lobby, where you can join and create rooms"
[image11]: ./images/image11.png "team game in progress"
[image7]: ./images/image7.png "Solid Garbage"
[image10]: ./images/image10.png "Unmessy (-100)"
[image1]: ./images/image1.png "Messy (100)"
[image9]: ./images/image9.png "game results table"
