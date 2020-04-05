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
  - [Demora de Bloqueo](#demora-de-bloqueo)
  - [Demora de Limpieza](#demora-de-limpieza)
  - [Gravedad lvl](#gravedad-lvl)
  - [Demora de Basura](#demora-de-basura)
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

### Sala Lenta

Quiéres jugar con un amigo pero la diferencia de habilidades entre ustedes es muy grande? O solo vas empezando y te estás cansando de perder inmediatamente en la Sala del Bot llena de jugadores pro? O quieres mejorar tu eficiencia al quitar la velocidad de la ecuación? Hay una Sala Lenta para todas esas ocaciones. La velocidad predeterminada de la sala está puesta a 2.0 PPS, lo que significa que un jugador no puede ir a más de 2.0 PPS. Cualquier intentro de ir más rápido, resultará en el bloqueo temporal de la pantalla del jugador. Adicionalmente al limite de velocidad, la Sala Lenta tiene un retrazo de limpieza de linea de 500 milisegundos. Eso significa que por cada linea que limpies, tendrás que esperar 500ms antes de poder jugar otra vez. Todos las Salas Lentas están indicadas con un icono de un velocímetro. - [SPEEDOMETER_ICON]. Salas Lentas personalizadas pueden tener cualquier limite de velocidad, desde 0 PPS a 20PPS.

![the lobby, where you can join and create rooms][image5]

### Sala de Mapa

El **Map Room** es un lugar para hacer downstack lo más rápido posible en mapas elegidos aleatoreamente, creados por usuarios. El (D=?%) que aparece a un lado de cada mapa es la dificultad promedio del mapa, con 0% siendo el más fácil y 100% el más difícil. Mapas que requieren un final con Perfect Clear no son incluidos en la sala.

---

## Un Jugador

### Carrera

La fundación, y con el objetivo más simple, **Carrera** es el modo de un solo jugador más popular en Jstris. Limpia X cantidad de lineas lo más rápido que puedas. Jstris ofrece modos de 20, 40, 100, y 1000 lineas.

### Queso

Menos agresivo y más analítico que Carrera, **Queso** requiere pensar más mientras haces downstack a través de lineas de basura de la manera más eficiente possible. Jstris ofrece modos de 10, 18, 100, e Infinitas lineas.
### Ultra

Centrado en el puntaje y recompensando técnicas avanzadas como los t-spins y los back-to-back, **Ultra** es una gran manera de mejorar tu poder de ataque para uso en Multijugador.

### Supervivencia

Posiblemente el modo de un jugador más complicado que hay, **Supervivencia** es similar a Queso pero la basura sigue subiendo a una velocidad constante de una linea por segundo. Sobrevive por el mayor tiempo posible las lineas que continuan subiendo.

### Mapas

A finales del 2018 el modo **Mapas** fue introducido en Jstris. Mapas atrae un elemento de creatividad a la vez que prepara a los jugadores para hacer downstack eficientemente en situaciones dificiles e inusuales. Crea tu propio mapa en el _Diseñador de Mapas_. Una vez publicado, cualquiera en el mundo puede jugarlo y competir por el tiempo más rápido. Hay un limite por usuario de 5 mapas publicados al día y 10 mapas en espera de publicación. Mapas también tiene una tabla de clasificación. En cada mapa,tres medallas son otorgadas, Oro para el 1er lugar, Plata para el 2do y Bronze para el 3ro. Consigue un lugar en el top 3 de cualquier mapa para ganar medallas y conseguir tu lugar en la tabla de clasificación!

_\*Notése que la tabla de clasificación de Mapas solo es actualizada unas pocas veces al día, así que cambios no son visibles inmediatamente._

### 20TSD

La meta en este modo es conseguir la mayor cantidad de TSDs (T-spin Dobles) posible. Si limpeas cualquier linea que no sea un TSD, el juego termina. Es llamado 20TSD porque el concepto original era hacer una carrera de 40 lineas usando solamente 20 TSDs (20 x 2 = 40). Sin embargo, algunas personas han ido más allá de eso y ahora regularmente exceden 20.

---

## Configuración

Para ver la configuración de cualquier sala de Jstris, usa el comando `/config`. Ahora veremos todas las configuraciones.

### Tablas de Combo y Ataque

La tabla de Combo y Ataque predeterminada en Jstris (que puede ser modificada en salas personalizadas) es la siguiente:

| Tipo de Ataque      | Lineas Enviadas |     | Combo # | Lineas Enviadas |
| :------------------ | --------------: | --- | ------: | --------------: |
| 0 lineas            |      **0**      |     |       0 |      **0**      |
| 1 lineas (single)   |      **0**      |     |       1 |      **0**      |
| 2 lineas (double)   |      **1**      |     |       2 |      **1**      |
| 3 lineas (triple)   |      **2**      |     |       3 |      **1**      |
| 4 lineas            |      **4**      |     |       4 |      **1**      |
| T-spin Doble        |      **4**      |     |       5 |      **2**      |
| T-spin Triple       |      **6**      |     |       6 |      **2**      |
| T-spin Single       |      **2**      |     |       7 |      **3**      |
| T-spin Mini Single  |      **0**      |     |       8 |      **3**      |
| Perfect Clear       |     **10**      |     |       9 |      **4**      |
| Back-to-Back        |     **+1**      |     |      10 |      **4**      |
|                     |                 |     |      11 |      **4**      |
|                     |                 |     |     12+ |      **5**      |

### Distribución de Basura

Existen 8 maneras distintas en la que la basura es enviada en partidas multijugador. Son las siguientes:

- Targets `/set garbage targets`
- Divide `/set garbage divide`
- To all `/set garbage toAll`
- To least `/set garbage toLeast`
- To most `/set garbage toMost`
- To self `/set garbage toSelf`
- Random `/set garbage random`
- Roulette `/set garbage roulette`

**Targets** siempre es el predeterminado (excepto en la Sala de Equipos) y el más popular. En Targets, Se rota un objetivo alrededor de cada oponente en la sala, en incrementos iguales y fijos, y quien sea que haya tenido el objetivo en el momento en que se envía basura es el que recibe esa basura enviada.

En el sistema de distribución **Divide**, cualquier basura enviada se divide por igual entre todos los jugadores. Por ejemplo, en una sala con otros 2 oponentes, si envías un T-spin doble (4 líneas), cada uno de tus oponentes recibirá 2 líneas.

En el sistema **To all**, cualquier basura enviada se envía a todos los jugadores en la sala. Por ejemplo, en una sala con 4 oponentes, si se envía un Perfect Clear (10 líneas), los 4 oponentes recibirán 10 líneas cada uno, o un total de 40 líneas. Como se puede deducir del ejemplo, las salas con basura para todos tienden a ser agitadas, con basura que crece rápidamente y juegos característicamente cortos.

En el sistema **To least**, La basura que envíes se envía al jugador que haya _recibido_ la menor cantidad de basura hasta el momento. Por ejemplo, en una habitación con otros 3 oponentes, envías 4 líneas. El oponente A recibió 50 líneas en el juego en el momento en que enviaste el ataque. El oponente B recibió 53. El oponente C recibió 58. Debido a que el oponente A recibió la menor cantidad de líneas hasta el momento, se le enviarán las 4 líneas a él.

En el sistem **To most**, la basura que envíes se envía al jugador que ha _enviado_ la mayor cantidad de basura hasta el momento. En esencia, estás atacando al jugador más fuerte de la sala.

En el sistema **To self**, la basura que envías se te envía a ti mismo. No es práctico en Multijugador, pero uno puede encontrar útil practicar con él.

En el sistema **Random**,la basura que envías se envía a cualquier jugador aleatorio. Posiblemente el sistema más justo.

En el sistema **Roulette**, la basura que envías se envía a cualquier jugador aleatorio, _incluido tu mismo_.

### Bloqueo de Basura

Hay 4 tipos de sistemas de bloqueo de basura en Jstris. Son:

- Full
- Limited
- None
- Instant

**Full** es el sistema de bloqueo predeterminado en Jstris. Otros clientes que usan Full son _TF_ (e + rooms) y _TOP_. Bajo el sistema de bloqueo de basura Full, la basura entrante aparece como una barra roja a su derecha. Sin embargo, no se añade a tu campo de juego hasta que colocas una pieza. La basura entrante se puede reducir con líneas enviadas (como 4 líneas) y, si ya ha comenzado un combo, se detendrá por completo hasta que termine el combo.

El sistema de bloqueo **Limited**  es muy similar a Full pero con una diferencia. La basura entrante se añade tan pronto como suelta una pieza, independientemente de si un combo ya se inició o no. En otras palabras, la basura entrante no se detiene durante los combos como lo hace Full. Al igual que en Full, la basura entrante se puede reducir con líneas enviadas. Los clientes que usan Limited incluyen _PPT_ y _TB_ y _TF_ (salas que no son e +).

En el sistema de bloqueo **None**, la basura nunca se puede reducir o cancelar. La basura entrante aparecerá primero como una barra roja (como en Full y Limited) y luego se insertará en su campo de juego tan pronto como suelte una pieza. Si un oponente te envía 10 líneas, incluso si eliminas 4 líneas con tu próxima pieza, la basura no se reducirá a 6. En cambio, recibirás 10 líneas mientras envías 4 a tu oponente.

En el sistema de bloqueo **Instant**, no hay barra roja en absoluto. En el momento en que un oponente envía un ataque, su basura se añadira a su campo. No hay forma de bloquearlo.

|         | Barra Roja(queue) | Bloqueo?  |
| ------- | :---------------: | :-------: |
| Full    |       Sí          |    Sí     |
| Limited |       Sí          |    Sí     |
| None    |       Sí          |    No     |
| Instant |       No          |    No     |

### Bloques

Hay 8 tipos diferentes de bloques.

- Standard
- Big
- ARS
- Penta
- M123
- All-29
- C2RS
- O-spin

**Standard** Estos son los tetrominos más utilizados y básicos con los que probablemente estés más familiarizado. Estos son los bloques predeterminados.

**Big** Cuatro veces más grande que tus bloques estándar, estos bloques causarán un daño masivo cuando juegues con ellos.

**ARS** Bloques estándar con ARS (sistema de rotación Arika), incluido CC-check. Implementación por NueSB.

**Penta** Estos bloques son pentominos. Hay 18 pentominos únicos.

**M123** Minos de tamaño 1,2,3. Hay 4 bloques M123 únicos.

**All-29** Todos los minos de tamaños 1,2,3,4,5, con un total de 29 minos únicos. Una combinación de 7 bloques Standard, 4 M123 y 18 Penta.

**C2RS** Bloques estándar con el sistema de rotación de Cultris 2

**O-spin** Un sistema de rotación de meme donde O-spin triple (2xCW) y O-spin quadruple (1xCCW) son posibles. Además, se permiten otros giros no convencionales (debido a la kick tbale que tiene 15 niveles de patada en lugar de SRS que tiene 4).

### Aleatorizador

Los aleatorizadores son básicamente la fórmula de qué bloques y en qué orden obtienes. Jstris tiene 11 aleatorizadores diferentes. Son:

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

**7-bag** es el aleatorizador estándar y predeterminado. Imagine una bolsa pequeña con 1 de cada uno de los 7 bloques diferentes. Ahora extrae, una por una, una pieza hasta que la bolsa esté vacía. Luego obtienes una nueva bolsa con nuevamente 1 de cada uno de los 7 bloques diferentes. Ahora sacas uno por uno una vez más. Repites. Así es como funciona el aleatorizador de 7-bag.

**14-bag** es muy similar a 7-bag, solo que la bolsa tiene el doble de tamaño, con 2 de cada uno de los 7 bloques. Una vez más, extrae cada pieza de la bolsa, una por una, hasta que la bolsa esté vacía. Enjuague y repita.

**Classic** te da piezas completamente al azar. Este aleatorizador hace que stackear sea muy desafiante.

**C2Sim** Una simulación del aleatorizador Cultris 2, descrita en este [post](http://harddrop.com/forums/index.php?showtopic=5080&st=0&p=71443&#entry71443)

**One block** Este aleatorizador te da un bloque seleccionado al azar que se elige para ti al principio y obtendrás solo ese bloque específico por el resto de el juego.

**Two block** Este aleatorizador es como el One Block, solo que alterna entre dos bloques específicos.  

**One 7-bag**La misma bolsa de 7 piezas se repite indefinidamente. Usando este aleatorizador, obtendrás la misma secuencia de 7 piezas una y otra vez.

**One 14-bag** La misma bolsa de 14 piezas se repite indefinidamente. Usando este aleatorizador, obtendrás la misma secuencia de 14 piezas una y otra vez.

**Repeat+7b** Funciona como 7-bag, solo que cualquier pieza de la bolsa tiene la posibilidad de repetirse entre 1 y 7 veces.

**BSblock+7b** 7-bag normal, con la excepción de que pueden aparecer piezas de diferentes conjuntos de bloques (de ahí la BS block set en el nombre), como pentominos o bloques grandes.

**BigBlock+7b** 7-bag normal, con la excepción de que pueden aparecer bloques grandes.

### Vistas Previas

Jstris tiene un valor predeterminado de 5 vistas previas. En salas personalizadas, puede establecer entre 0 y 5 vistas previas.

### Basura Solida

La basura sólida son líneas que no puedes limpear y que se elevan desde la parte inferior para "apurar" el juego, para que no se extienda indefinidamente. Son ligeramente más oscuros que las líneas de basura normales. En la sala de bot, la basura sólida por defecto comienza a llegar después de 2 minutos. La basura sólida también se puede personalizar en habitaciones personalizadas.

![Solid Garbage][image7]

### Demora de Bloqueo

La Demora de Bloqueo se refiere a cuánto tiempo puede esperar una pieza en el suelo antes de bloquearse en su lugar. En Jstris, hay tres tipos de demoras de bloqueo que puede personalizar. El primero, L1, controla los milisegundos que pueden pasar después de que una pieza se deja caer suavemente al suelo hasta que se bloquea. La demora predeterminada de L1 es de 500 milisegundos. El segundo, L2, controla cuántos milisegundos después de que una pieza se deja caer suavemente al suelo y se mantiene en movimiento moviéndose hacia la izquierda o hacia la derecha hasta que se bloquea. La demora predeterminada de L2 es de 5000 milisegundos. Tenga en cuenta que si una pieza se gira, la L2 se reinicia y la pieza puede permanecer más de 5000 milisegundos, lo que nos lleva a L3. El tercero, L3, es la cantidad máxima de tiempo que una pieza que ingresa a la matriz puede permanecer activa antes de que se bloquee automáticamente, pase lo que pase. La demora predeterminada de L3 es de 20000 milisegundos.

### Demora de Limpieza

La Demora de Limpeza es una cantidad fija de tiempo que transcurre después de que limpia cualquier línea. Durante este tiempo, no puedes hacer nada. Muchos juegos de bloques clásicos y PPT usan un retraso, pero Jstris por defecto tiene un retraso de 0, y en su mayor parte nunca se usa aquí. Sin embargo, es personalizable si desea activarlo. Su rango es de 0 milisegundos a 6000 milisegundos.

### Gravedad lvl

El nivel de gravedad se refiere a la velocidad a la que las piezas caen por la matriz automáticamente. La gravedad se puede ajustar desde los niveles 0-28. La gravedad predeterminada es 1. Si la gravedad es 0, la pieza no se caerá hasta que se bloquee automáticamente después de la demora de bloqueo L3 de 20 segundos (consulte la sección Demora de bloqueo). Un nivel de gravedad de 28 es igual a 20G, lo que significa que las piezas caerán instantáneamente de arriba a abajo.

### Demora de Basura

La demora de la basura es un tiempo fijo entre la basura entrante indicada por la barra roja y la inserción de esa basura en el campo de juego. Por defecto, se establece en 500 milisegundos. Es personalizable desde un rango de 0 milisegundos a 60000 milisegundos. Una demora de basura más alto permite que se jueguen más piezas antes de insertar la basura, mientras que una demora de basura más bajo permite que se jueguen menos piezas antes de la inserción de basura. O, en otras palabras, cuanto mayor sea la demora de la basura, más oportunidades da para bloquear de manera más efectiva. Otra forma de definir la demora de la basura es "la cantidad mínima de tiempo que un ataque entrante tiene que ser visible en la barra roja antes de que un bloque colocado pueda desencadenar la inserción de esa basura en el campo de juego".

### Desorden

El desorden de basura se refiere al nivel de dificultad para limpiar ciertos tipos de basura. Para cambiar el desorden de la basura en una habitación, use el comando `/ set messiness?`, Donde el ? se reemplaza con cualquier número de -100 a 100. -100 es la configuración de basura menos desordenada, y el agujero de basura solo aparecerá en una columna a lo largo de todo el juego (imagen izquierda). 100 es la configuración de basura más desordenada y el agujero de basura aparecerá en cualquiera de las 10 columnas, lo que hace que sea mucho más difícil de apilar (imagen derecha).

![Unmessy (-100)][image10]
![Messy (100)][image1]

### Configuración de Presets

Si hay una configuración de sala que le guste especialmente y deseas volver a consultar fácilmente, puede guardar la configuración como un preset.

Para hacer esto, vaya a _Salas_, luego _Crear Sala_, luego a la pestaña _Simple_ o _Todo_. Una vez que haya personalizado la configuración a su gusto, presione el botón _Guardar_ en la esquina inferior derecha para generar sus datos preestablecidos. Cópielo, luego péguelo en el cuadro junto a Datos preestablecidos en la página [Subir una nueva plantilla](/presets/submit).

Una vez que haya enviado el ajuste preestablecido, puede verlo, junto con todos los demás ajustes preestablecidos enviados por otros usuarios en la [Lista de ajustes preestablecidos](/presets). Ahora puede recrear fácilmente la misma habitación sin tener que volver a personalizar todos los ajustes. Simplemente vaya a _Crear Sala_, luego _Usar Plantilla Personalizada_ e ingrese el título o el número de ID de su preset.

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
