# Jstris Guide

Bienvenido a Jstris, un sencillo juego de bloques en linea. Jstris es conocido por su rápida jugabilidad y está atrayendo jugadores talentosos alrededor de todo el mundo. Esta guía te introducirá a las características basicas del juego.

---

**Tabla de Contenidos**

- [Prólogo](#prólogo)
- [Controles](#controles)
- [Multijugador](#multijugador)
  - [Sala Default](#sala-default)
  - [Sala del Bot](#sala-del-bot)
  - [Sala 1v1](#sala-1v1)
  - [Sala Lenta](#sala-lenta)
  - [Sala de Mapa](#sala-de-mapa)
- [Un Jugador](#un-jugador)
  - [Carrera](#carrera)
  - [Queso](#queso)
  - [Ultra](#ultra)
  - [Supervivencia](#supervivencia)
  - [Mapas](#mapas)
  - [20TSD](#20tsd)
- [Configuración](#configuración)
  - [Tablas de Combo y Ataque](#tablas-de-combo-y-ataque)
  - [Distribución de Basura](#distribución-de-basura)
  - [Bloqueo de Basura](#bloqueo-de-basura)
  - [Bloques](#Bloques)
  - [Aleatorizador](#aleatorizador)
  - [Vistas Previas](#vistas-previas)
  - [Basura Solida](#basura-solida)
  - [Retraso de Bloqueo](#retraso-de-bloqueo)
  - [Retraso de Limpieza](#retraso-de-limpieza)
  - [Gravedad lvl](#gravedad-lvl)
  - [Retraso de Basura](#retraso-de-basura)
  - [Desorden](#desorden)
  - [Configuración de Preajustes](#Configuración-de-preajustes)
  - [Modo](#modo)
- [Preguntas Frecuentes](#faq)
  - [Q: Puedo agregar un bot a mi sala personalizada o privada?](#q-puedo-agregar-un-bot-a-mi-sala-personalizada-o-privada)
  - [Q: Qué significan las abreviaciones en la tabla de resultados?](#q-qué-signigican-las-abreviaciones-en-la-tabla-de-resultados?)
  - [Q:Qué es DAS?](#q-que-es-das)
  - [Q:Qué es ARR?](#q-que-es-arr)
  - [Q:Qué es finesse?](#q-que-es-finesse)
  - [Q: Puedo crear una sala privada?](#q-puedo-crear-una-sala-privada)
  - [Q: Puedo jugar jstris desconectado?](#q-puedo-jugar-jstris-desconectado)
- [Información Adicional](#información-adicional)

---

## Prólogo

Jstris usa las mismas mecánicas basicas que la mayoría de los otros juegos de bloques. Sigue las reglas de guideline.Una característica notable es el uso extensivo de repeticiones. En cada modo de juego que juegues y completes, una repetición será generada para ti. Ver y analizarte a ti mismo es una parte integral para mejorar, y las repeticiones de Jstris hacen de esto, una tarea muy sencilla.

A diferencia de otros sitios, puedes estar seguro que las tablas de clasificación de Jstris no tienen gente haciendo trampa. Los moderadores eliminan records sospechosos para asegurar una lista de logros mundial digna de confianza.

Es posible jugar sin registrarse, pero para usar todas las características de la página, se recomienda que cree una cuenta. Para eso, de click en _Registrarse_ en la esquina derecha superior. Solo se requiere un correo electrónico, un nombre de usuario y una contraseña. Con una cuenta, puedes ver una gran cantidad de estadísticas incluyendo tus mejores tiempos en modos de un solo jugador, estadísticas de multijugador, mejoras, repeticiones, y mucho más. También te puedes ver a ti mismo en las tablas de clasificación (las puntuaciones de usuarios no registrados son excluidas).

![introduction][image2]

---

## Controles

Jstris permite que los jugadores modifiquen sus controles en cualquier momento en el menú de **Ajustes** localizado debajo del tablero del jugador. Los controles predeterminados son:

| Comando         | Tecla Predeterm. |
| --------------- | ---------------- |
| Mover Izquierda | Izquierda        |
| Mover Derecha   | Derecha          |
| Caida Lenta     | Abajo            |
| Caida Rápida    | Espacio          |
| Rotar Izquierda | z                |
| Rotar Derecha   | Arriba           |
| Rotar 180       | a                |
| Hold            | c                |

## Multijugador

### Sala Default

Al entrar al sitio, todos los jugadores son inmediatamente arrojados al **Default Room**, un todos contra todos done encontrarás jugadores de todo nivel de habilidad.

Jugar en la Sala Default puede ser difícil! Algo único de Jstris es que arroja humildes principiantes y oponentes de talla mundial juntos, así como todos los demás de por medio. Si te cansas de jugar y únicamente quieres ver, entonces usa el comando `/spectate` o `/spec`. Para jugar otra vez, usa el comando `/play`.

### Sala del Bot

La Sala Default no es la única sala que hay. Para ver la lista completa de salas, da click en _Lobby_ en la parte inferior izquierda de tu tablero. La 2da sale más popular en Jstris usualmente es la Sala del Bot **Bot Room**, llamada de esta manera por el bot que siempre está presente. Siempre estará en la parte superior izquerda de todos tus oponentes, distinguible fácilmente por su color rojo uniforme.

![MisaMino bot in opponents view][image4]

Hay cuatro tipos de bots en Jstris. Aquí están listados por dificultad, y los comandos para cambiar a alguno específico, introducidos en el chat.

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (removido en 2018.09.21)
- ~~Fool bot: `/changeBot fool`~~ (removido en 2018.09.21)

_\*Todos los comandos deben ser ingresados entre juegos, Cualquier comando ingresando durante un juego será ignorado._

Misamino es por mucho el bot más difícil, quizás el bot más difícil alguna vez creado. Cuando está a la velocidad máxima de 5pps(piezas por segundo), se convierte en un oponente formidable que facilmente puede ganar en contra de los mejores jugadores humanos en un 1v1. Sin embargo, El desempeño del bot sufre cuando hay >5 humanos en la Sala del Bot, y es probable que pierda inmediatamente. Esto nos lleva a nuestro siguiente comando: /botPPS.

La velocidad del bot puede ser cambiada. para hacer esto, escribe `/bot ?` y remplaza el ? con cualquier numero entre .3 y 5. Por ejemplo, si quisiera que el bot jugara a 2 PPS, Escribiría `/bot 2`. Si quisiera que el bot jugara a 1.73 PPS, Escribiría `/bot 1.73`.

### Sala 1v1

La sala **1v1 Room** tiene un máximo de 2 jugadores, aunque eres libre de venir a observar aunque la sala esté llena. Usa esta sala para arreglar diferencias con tus amigos o para jugar en contra de algun jugador digno. Si están contando el puntaje, y quieres restablecerlo, escribe `/resetCounter` y todos los puntos volverán a 0.

### Slow Room

Want to play with a friend but the skill level between yourselves is too great? Or you’re just getting started and tired of losing instantly in the pro-dominated Bot Room? Or you want to improve efficiency in your game by taking speed out of the equation? There’s a Slow Room in place for all those occasions. The default Slow Room's speed limit is set at 2.0 PPS, which means a player cannot go over 2.0 PPS. Any attempts to go faster will result in the player’s screen being temporarily locked. In addition to the speed limit, the Slow Room has a line clear delay of 500 milliseconds. That means for each line(s) you clear, you will have to wait 500 ms before you can play again. All Slow Rooms are indicated by the little speedometer icon - [SPEEDOMETER_ICON]. Custom Slow rooms can have any speed limit from 0 PPS to 20 PPS.

![the lobby, where you can join and create rooms][image5]

### Map Room

The **Map Room** is a place to downstack the fastest through randomly-chosen, user-created Mapas. The (D=?%) displayed next to each map is the difficulty percentile of the map, with 0% being the easiest and 100% being the hardest. Mapas with Perfect Clear Finish requirement are not included among the Mapas.

---

## Singleplayer

### Sprint

The foundation, and with the most simple objective, **Sprint** is the most popular singleplayer mode on Jstris. Clear X amount of lines as fast as you can. Jstris offers 20, 40, 100, and 1000 line Sprint modes.

### Cheese Race

Less brash and more analytical than Sprint, **Cheese Race** requires more thinking as you downstack through garbage lines in the most efficient way. Jstris offers 10, 18, 100, and infinity line Cheese Race modes.

### Ultra

Score-focused and rewarding advanced techniques such as t-spins and back-to-backs, **Ultra** is a great way to improve your attacking prowess for use in Multijugador.

### Supervivencia

Quite possibly the most challenging of the singleplayer modes, **Supervivencia** is much like Cheese Race only the garbage rises at a constant rate of one line per second. Survive against the rising lines for as long as you can.

### Mapas

In late 2018, the **Mapas** mode was introduced to Jstris. Mapas brings an element of creativity while also preparing players to downstack effectively in difficult and unusual positions. Create your own map in the _Map Designer_. Once published, anyone in the world can play it and compete for the fastest time. There is a limit of 5 published Mapas per day and 10 unpublished Mapas in queue. Mapas also has a leaderboard. On every map, three medals are given, Gold for 1st place, Silver for 2nd place, and Bronze for 3rd place. Score in the top three of any map to win some medals and secure your place on the leaderboard!

_\*Note that the Mapas leaderboards updates only a few times each day, so new changes are not immediate._

### 20TSD

The goal in this mode is to try to get as many consecutive TSDs (T-spin Double) as you can. If you clear any line that isn't a TSD, the game ends. It is named 20TSD because the original concept was to do a 40 line sprint using nothing but 20 TSDs (20 x 2 = 40). However, some people have gone beyond that and now regularly exceed 20.

---

## Configuración

To see the Configuración of any room on Jstris, use the command `/config`. Now we will go over each of the settings.

### Attack and Combo table

The default attack and combo table in Jstris (which can be customized in private rooms) is as follows:

| Attack Type        | Lines Sent |     | Combo # | Lines Sent |
| :----------------- | ---------: | --- | ------: | ---------: |
| 0 lines            |      **0** |     |       0 |      **0** |
| 1 lines (single)   |      **0** |     |       1 |      **0** |
| 2 lines (double)   |      **1** |     |       2 |      **1** |
| 3 lines (triple)   |      **2** |     |       3 |      **1** |
| 4 lines            |      **4** |     |       4 |      **1** |
| T-spin Double      |      **4** |     |       5 |      **2** |
| T-spin Triple      |      **6** |     |       6 |      **2** |
| T-spin Single      |      **2** |     |       7 |      **3** |
| T-spin Mini Single |      **0** |     |       8 |      **3** |
| Perfect Clear      |     **10** |     |       9 |      **4** |
| Back-to-Back       |     **+1** |     |      10 |      **4** |
|                    |            |     |      11 |      **4** |
|                    |            |     |     12+ |      **5** |

### Distribución de Basura

There are 8 different systems in how garbage is sent around during Multijugador matches. They are as follows:

- Targets `/set garbage targets`
- Divide `/set garbage divide`
- To all `/set garbage toAll`
- To least `/set garbage toLeast`
- To most `/set garbage toMost`
- To self `/set garbage toSelf`
- Random `/set garbage random`
- Roulette `/set garbage roulette`

**Targets** is always the default (except in the Team Room) and by far the most popular. In Targets, a target is rotated around every opponent in the room, in equal and fixed increments, and whoever the target was landed on at the moment you send garbage is the one who gets that garbage you sent.

In the **Divide** garbage distribution system (GDS), any garbage you send is equally divided among all players. For example, in a room with 2 other opponents, if you send a T-spin Double (4 lines), each of your opponents will get 2 lines.

In the **To all** GDS, any garbage you send is sent to every player in the room. For example, in a room with 4 opponents, if you send a Perfect Clear (10 lines), all 4 opponents will recieve 10 lines each, or a total of 40 lines. As you can surmise from the example, rooms with To all garbage tend to be hectic, with fast rising garbage and characteristically short games.

In the **To least** GDS, garbage you send is sent to the player who had _recieved_ the least garbage so far. For example, in a room with 3 other opponents, you send 4 lines. Opponent A received 50 lines in the game already at the moment you sent the attack. Opponent B received 53. Opponent C received 58. Because Opponent A received the least lines so far, the 4 lines from your line clear will be sent to him.

In the **To most** GDS, garbage you send is sent to the player who had _sent_ the most garbage so far. In essence, you are attacking the strongest player in the room.

In the **To self** GDS, garbage you send is sent to yourself. Impractical in Multijugador, but one might find it helpful to practice with it alone.

In the **Random** GDS, garbage you send is sent to any random player. Arguably the most fair GDS.

In the **Roulette** GDS, garbage you send is sent to any random player, _including yourself_.

### Bloqueo de Basura

There are 4 types of garbage blocking systems on Jstris. They are:

- Full
- Limited
- None
- Instant

**Full** is the default blocking system on Jstris. Other clients that use Full are _TF_ (e+ rooms) and _TOP_. Under the Full garbage blocking system, incoming garbage appears as a red bar to your right. It doesn’t rise up on your playfield, however, until you place a piece down. The incoming garbage can be reduced with sent lines (such as a 4 lines) and, if you have already started a combo, will pause completely until you finish the combo.

**Limited** blocking system is very similar to Full but with one difference. Incoming garbage is inserted as soon as you drop a piece, regardless of whether a combo was started already or not. In other words, incoming garbage does not pause during combos the way Full does. Like in Full, incoming garbage can be reduced with sent lines. Clients that use Limited include _PPT_ and _TB_ and _TF_ (non e+ rooms).

In the **None** blocking system, garbage can never be reduced or cancelled. Incoming garbage will first appear as a red bar (like in Full and Limited) and then be inserted into your playfield as soon as you drop a piece. If an opponent sends you 10 lines, even if you clear 4 lines as your next piece, the garbage will not reduce to 6. Instead, you will still recieve 10 lines while sending 4 to your opponent.

In the **Instant** blocking system, there is no red bar at all. The moment an opponent sends an attack, its garbage will rise up on your field. There is no blocking it.

|         | Red bar (queue) | Blocking? |
| ------- | :-------------: | :-------: |
| Full    |       Yes       |    Yes    |
| Limited |       Yes       |    Yes    |
| None    |       Yes       |    No     |
| Instant |       No        |    No     |

### Bloques

There are 8 different types of blocks.

- Standard
- Big
- ARS
- Penta
- M123
- All-29
- C2RS
- O-spin

**Standard** These are the most widely used and basic tetrominoes you are probably most familiar with. These are the default blocks.

**Big** Four times bigger than your standard blocks, these blocks will deal out massive damage when played with.

**ARS** Standard blocks with ARS (Arika rotation system), including CC-check. Implementation by NueSB

**Penta** These blocks are pentominoes. There are 18 unique pentominoes.

**M123** Minos of sizes 1,2,3. There are 4 unique M123 blocks.

**All-29** All minos of sizes 1,2,3,4,5, totaling 29 unique minos. A combination of 7 Standard, 4 M123, and 18 Penta blocks.

**C2RS** Standard blocks with the Cultris 2 rotation system

**O-spin** A meme rotation system where O-spin triple (2xCW) and O-spin quadruple (1xCCW) are possible. Also, other unconventional spins are allowed (due to the kick table which has 15 kick levels as opposed to SRS which has 4).

### Aleatorizador

Randomizers are basically the formula for what and what order blocks you get. Jstris has 11 different randomizers. They are:

- 7-bag
- 14-bag
- Classic
- C2Sim
- One block
- Two block
- One 7-bag
- One 14-bag
- Repeat+7b
- BSblock+7b
- BigBlock+7b

**7-bag** is the standard and default randomizer. Imagine a small bag with 1 each of the 7 different blocks. Now you draw out, one by one, a piece until the bag is empty. Then you get a new bag with again 1 each of the 7 different blocks. Now you draw out one by one once more. Repeat. This is how the 7-bag randomizer works.

**14-bag** is much like 7-bag only the bag is doubled in size, with 2 of each of the 7 blocks. Once again, you draw out each piece from the bag, one by one, until the bag is empty. Rinse and repeat.

**Classic** randomizer gives you completely random pieces. This randomizer makes stacking very challenging.

**C2Sim** A simulation of the Cultris 2 randomizer, described in this [post by Integration](http://harddrop.com/forums/index.php?showtopic=5080&st=0&p=71443&#entry71443)

**One block** This randomizer gives you a randomly selected block is chosen for you at the start and you will get only that specific block for the whole game.

**Two block** This randomizer is like the One Block one, only it alternates between two specific blocks instead.

**One 7-bag** The same bag of 7 pieces is repeated indefinitely. Using this randomizer, you will get the same sequence of 7 pieces over and over.

**One 14-bag** The same bag of 14 pieces is repeated indefinitely. Using this randomizer, you will get the same sequence of 14 pieces over and over.

**Repeat+7b** Works like 7-bag, only any piece in the bag has a chance of being repeated anywhere from 1-7 times.

**BSblock+7b** Normal 7-bag, with the exception that pieces from different Block Sets (hence the BS in the name), like pentominoes or Big Blocks, may appear.

**BigBlock+7b** Normal 7-bag, with the exception that Big Blocks may appear.

### Previews

Jstris has a default of 5 previews. In custom rooms, you can set anywhere from 0 to 5 previews.

### Solid Garbage

Solid garbage are unclearable lines that rise up from the bottom to “hurry up” the game so it doesn’t extend indefinitely. They are slightly darker than normal garbage lines. In the Bot Room, solid garbage by default starts to come after 2 minutes. Solid garbage is also customizable in custom rooms.

![Solid Garbage][image7]

### Lock Delay

Lock delay refers to how much time a piece can wait on the ground before locking into place. In Jstris, there are three types of lock delays you can customize. The first one, L1, controls how many milliseconds after a piece is softdropped to the ground until it locks. The default L1 delay is 500 milliseconds. The second one, L2, controls how many milliseconds after a piece is softdropped to the ground and is kept in motion by moving left or right until it locks. The default L2 delay is 5000 milliseconds. Note that if a piece is rotated, the L2 is reset and the piece can stay on longer than 5000 milliseconds, which brings us to L3. The third one, L3, is the maximum amount of time a piece that enters the matrix can stay on before it autolocks, no matter what. The default L3 delay is 20000 milliseconds.

### Clear Delay

Clear delay is a fixed amount of time that passes after you clear any line(s). During this time, you can’t do anything. Many classic block games and PPT use clear delay, but Jstris by default has 0 delay, and for the most part it is never used here. However, it is customizable if you want to turn it on. Its range is 0 milliseconds to 6000 milliseconds.

### Gravity lvl

Gravity level refers to the rate at which the pieces fall down the matrix automatically. The Gravity can be adjusted from levels 0-28. The default Gravity is 1. If gravity is 0, the piece will not fall down at all until it is autolocked after the 20 second L3 lock delay (see section Lock Delay). A Gravity level of 28 is equal to 20G, which means pieces will instantly fall from the top to bottom.

### Garbage Delay

Garbage delay is a fixed amount of time between the incoming garbage indicated by the red bar and the insertion of that garbage into the playfield. By default, it is set at 500 milliseconds. It is customizable from a range of 0 milliseconds to 60000 milliseconds. A higher garbage delay allows for more pieces to be played before garbage is inserted, while a lower garbage delay allows for less pieces to be played before garbage insertion. Or in other words, the higher the garbage delay, the more opportunity it gives to block more effectively. Another way to define garbage delay is “the minimumum amount of time an incoming attack has to be visible in the red bar before a placed block can trigger the insertion of that garbage to the playfield.”

### Messiness

Garbage messiness refers to the difficulty level to clear certain types of garbage. To change the messiness of garbage in a room, use the command `/set messiness ?`, where the ? is replaced with any number from -100 to 100. -100 is the least messy garbage Configuración, and the garbage hole will only appear in one column throughout the entirety of the game (left picture). 100 is the most messy garbage Configuración and the garbage hole will appear in any of the 10 columns, making it much more difficult to downstack (right picture).

![Unmessy (-100)][image10]
![Messy (100)][image1]

### Configuración presets

If there is a room settings Configuración you particularly like and want to easily refer back to, you can save the settings as a preset.

To do this, go to _Lobby_, then _Create Room_, then either the _Simple_ or _All_ tab. Once you have customized the settings to your liking, hit the _Save_ button at the bottom right corner to generate your preset data. Copy it, then paste it in the box next to Preset data on the [Submit a preset](/presets/submit) page.

Once you’ve submitted the preset, you can view it, along with all other user-submitted presets on the [List of presets](/presets). Now you can easily recreate the same room without customizing all the settings again. Just go to _Create Room_, then _Use Custom Preset_, and enter either the title or ID number of your preset.

### Mode

There are currently 7 different modes to choose from when creating a new room. They are:

- Standard
- Team
- Cheese
- Live Sprint
- Live Cheese
- Live Supervivencia
- Live Mapas v0.1

**Standard** mode is normal Multijugador free-for-all.

**Team** mode creates a custom Team Room. Pick a side, red or blue, and battle and bring glory for your team. To set your own team name, use the command `/set teamName ?` where the ? is replaced with your team name.

![team game in progress][image11]

**Cheese** mode creates a Cheese Room. Cheese, also known as garbage, is the primary way to knock out opponents in Multijugador modes. It is an important skill to downstack through cheese. Practice how fast you can downstack in this mode that starts games with 10 lines of garbage. First to reach the bottom wins. 10 lines too easy for you? Adjust the amount of starting lines with the command `/set height ?` , with the question mark representing a number from 1 to 20.

**Live Sprint** mode allows you to play Sprint against an opponent(s). The fastest one to finish the Sprint wins. The room defaults to a 40L Sprint, but you can change to any other type of Sprint with these commands:

- 20L: `/set gamemode sprint20`
- 40L: `/set gamemode sprint40`
- 100L: `/set gamemode sprint100`
- 1000L: `/set gamemode sprint1000`

If you break your Sprint record in Live Sprint, unfortunately you cannot add it to your account because the Sprint will be contained in a Live Replay, not a standard Replay. But you can still save the replay to your favorites if you want to preserve it.

**Live Cheese** mode allows you to play Cheese against an opponent(s). Live Cheese mode is virtually identical to Cheese mode except that you can't customize starting lines beyond the 10L, 18L, and 100L. The room defaults to a 10L Cheese, but you can change to any other type of Cheese with these commands:

- 10L: `/set gamemode cheese10`
- 18L: `/set gamemode cheese18`
- 100L: `/set gamemode cheese100`

**Live Survial** mode allows you to play Supervivencia against an opponent(s). Whoever survives the longest wins.

**Live Mapas v0.1** mode creates a custom Map Room. Everything in this room works the same as the Map Room.

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

A: Finesse is defined as the most efficient way to move a block. Good finesse is important for playing smoother and faster. The number next to finesse denotes how many finesse errors were committed. So a 0 finesse score means you made no finesse errors. Ideally, the closer you get to 0, the better. Finesse is something that needs to be learned in order to know how to do. There are many resources online explaining it. This video is a good starting point: [Tutorial: How to Play Fast!](https://youtu.be/_QBs703nOnk?t=502).

### Q: Can I create a private room?

A: Yes. Click _Lobby_, then _Create Room_, then check the box that says _Private_. Copy and give the room link to anyone you want to join your private room. Here’s a tip: grab the link of any room, public or private, by using the command `/link`.

### Q: Can I play Jstris offline?

A: Yes. In order to play offline, you have to first download Jstris while you are online. To do this, right click on the home page, press "Save as", and download the html file. Note that only single player modes can be played offline, and the scores will not be saved.

---

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
