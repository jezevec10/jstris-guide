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
  - [Bloques](#bloques)
  - [Aleatorizador](#aleatorizador)
  - [Vistas Previas](#vistas-previas)
  - [Basura Solida](#basura-solida)
  - [Demora de Bloqueo](#demora-de-bloqueo)
  - [Demora de Limpieza](#demora-de-limpieza)
  - [Gravedad lvl](#gravedad-lvl)
  - [Demora de Basura](#demora-de-basura)
  - [Desorden](#desorden)
  - [Configuración de Preajustes](#configuración-de-preajustes)
  - [Modos](#modos)
- [Preguntas Frecuentes](#faq)
  - [Q: ¿Puedo agregar un bot a mi sala privada o personalizada?](#q-¿puedo-agregar-un-bot-a-mi-sala-privada-o-personalizada?)
  - [Q: ¿Qué significan esas abreviaturas en la tabla de resultados?](#q-¿qué-significan-esas-abreviaturas-en-la-tabla-de-resultados?)
  - [Q:¿Qué es el DAS?](#q-¿qué-es-el-das?)
  - [Q:¿Qué es el ARR?](#q-¿qué-es-el-arr?)
  - [Q:¿Qué es el Finesse?](#q-¿qué-es-el-finesse?)
  - [Q: ¿Puedo crear una sala privada?](#q-¿puedo-crear-una-sala-privada?)
  - [Q: ¿Puedo jugar jstris sin conexión?](#q-¿puedo-jugar-jstris-sin-conexión?)
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
PresetsPresetsPresets

### Tablas de Combo y Ataque

La tabla de Combo y Ataque predeterminada en Jstris (que puede ser modificada en salas personalizadas) es la siguiente:

| Tipo de Ataque     | Lineas Enviadas |     | Combo # | Lineas Enviadas |
| :----------------- | --------------: | --- | ------: | --------------: |
| 0 lineas           |           **0** |     |       0 |           **0** |
| 1 lineas (single)  |           **0** |     |       1 |           **0** |
| 2 lineas (double)  |           **1** |     |       2 |           **1** |
| 3 lineas (triple)  |           **2** |     |       3 |           **1** |
| 4 lineas           |           **4** |     |       4 |           **1** |
| T-spin Doble       |           **4** |     |       5 |           **2** |
| T-spin Triple      |           **6** |     |       6 |           **2** |
| T-spin Single      |           **2** |     |       7 |           **3** |
| T-spin Mini Single |           **0** |     |       8 |           **3** |
| Perfect Clear      |          **10** |     |       9 |           **4** |
| Back-to-Back       |          **+1** |     |      10 |           **4** |
|                    |                 |     |      11 |           **4** |
|                    |                 |     |     12+ |           **5** |

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

El sistema de bloqueo **Limited** es muy similar a Full pero con una diferencia. La basura entrante se añade tan pronto como suelta una pieza, independientemente de si un combo ya se inició o no. En otras palabras, la basura entrante no se detiene durante los combos como lo hace Full. Al igual que en Full, la basura entrante se puede reducir con líneas enviadas. Los clientes que usan Limited incluyen _PPT_ y _TB_ y _TF_ (salas que no son e +).

En el sistema de bloqueo **None**, la basura nunca se puede reducir o cancelar. La basura entrante aparecerá primero como una barra roja (como en Full y Limited) y luego se insertará en su campo de juego tan pronto como suelte una pieza. Si un oponente te envía 10 líneas, incluso si eliminas 4 líneas con tu próxima pieza, la basura no se reducirá a 6. En cambio, recibirás 10 líneas mientras envías 4 a tu oponente.

En el sistema de bloqueo **Instant**, no hay barra roja en absoluto. En el momento en que un oponente envía un ataque, su basura se añadira a su campo. No hay forma de bloquearlo.

|         | Barra Roja(queue) | Bloqueo? |
| ------- | :---------------: | :------: |
| Full    |        Sí         |    Sí    |
| Limited |        Sí         |    Sí    |
| None    |        Sí         |    No    |
| Instant |        No         |    No    |

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
Presets
**ARS** Bloques estándar con ARS (sistema de rotación Arika), incluido CC-check. Implementación por NueSB.

**Penta** Estos bloques son pentominos. Hay 18 pentominos únicos.

**M123** Minos de tamaño 1,2,3. Hay 4 bloques M123 únicos.

**All-29** Todos los minos de tamaños 1,2,3,4,5, con un total de 29 minos únicos. Una combinación de 7 bloques Standard, 4 M123 y 18 Penta.

**C2RS** Bloques estándar con el sistema de rotación de Cultris 2

**O-spin** Un sistema de rotación de meme donde O-spin triple (2xCW) y O-spin quadruple (1xCCW) son posibles. Además, se permiten otros giros no convencionales (debido a la kick tbale que tiene 15 niveles de patada en lugar de SRS que tiene 4).

### Aleatorizador

Presets
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

### Configuración de Preajustes

Si hay una configuración de sala que le guste especialmente y deseas volver a consultar fácilmente, puede guardar la configuración como un preajuste.

Para hacer esto, vaya a _Salas_, luego _Crear Sala_, luego a la pestaña _Simple_ o _Todo_. Una vez que haya personalizado la configuración a su gusto, presione el botón _Guardar_ en la esquina inferior derecha para generar sus datos preestablecidos. Cópielo, luego péguelo en el cuadro junto a Datos preestablecidos en la página [Subir una nueva plantilla](/presets/submit).

Una vez que haya enviado el ajuste preestablecido, puede verlo, junto con todos los demás ajustes preestablecidos enviados por otros usuarios en la [Lista de ajustes preestablecidos](/presets). Ahora puede recrear fácilmente la misma habitación sin tener que volver a personalizar todos los ajustes. Simplemente vaya a _Crear Sala_, luego _Usar Plantilla Personalizada_ e ingrese el título o el número de ID de su preajuste.

### Modos

Actualmente hay 7 modos diferentes a elegir al crear una nueva sala. Son:

- Standard
- Team
- Cheese
- Live Sprint
- Live Cheese
- Live Supervivencia
- Live Mapas v0.1

**Standard** es multijugador normal todos contra todos.

**Team** Este modo crea una sala de equipo personalizada. Elige un equipo, rojo o azul, y lucha y trae gloria a tu equipo. Para configurar el nombre de tu propio equipo, usa el comando `/set teamName ?` Donde el ? se reemplaza con el nombre de tu equipo.

![team game in progress][image11]

**Cheese** crea una sala de queso. El queso, también conocido como basura, es la forma principal de noquear a los oponentes en los modos Multijugador. Es una habilidad importante el abrirte paso a través de el queso. Practica qué tan rápido puedes limpiar lineas en este modo que inicia los juegos con 10 líneas de basura. Primero en llegar al fondo gana. ¿10 líneas es demasiado fácil para ti? Ajusta la cantidad de líneas con las que inicias con el comando `/set height ?`, Con el signo de interrogación representando un número del 1 al 20.

**Live Sprint** Este modo te permite jugar Sprint contra un oponente(s). El más rápido en terminar el Sprint gana. La sala tiene predeterminado un Sprint de 40L, pero puedes cambiar a cualquier otro tipo de Sprint con estos comandos:

- 20L: `/set gamemode sprint20`
- 40L: `/set gamemode sprint40`
- 100L: `/set gamemode sprint100`
- 1000L: `/set gamemode sprint1000`

Si rompes tu record de Sprint en Live Sprint, desafortunadamente no podrás agregarlo a tu cuenta porque el Sprint estará contenido en una Reproducción en vivo, no en una Reproducción estándar. Pero aún puedes guardar la repetición en tus favoritos si deseas conservarla.

**Live Cheese** Este modo te permite jugar Queso contra un oponente(s). El modo Live Cheese es prácticamente idéntico al modo Cheese, excepto que no puedes personalizar las líneas de inicio más allá de 10L, 18L y 100L. La sala tiene un valor predeterminado de 10L Cheese, pero puedes cambiar a cualquier otro tipo de Cheese con estos comandos:

- 10L: `/set gamemode cheese10`
- 18L: `/set gamemode cheese18`
- 100L: `/set gamemode cheese100`

**Live Survial** te permite jugar Supervivencia contra un oponente(s). Quien sobreviva más tiempo gana.

**Live Maps v0.1** crea una sala de mapas personalizada. Todo en esta sala funciona igual que la sala de mapas.

## FAQ

### Q: ¿Puedo agregar un bot a mi sala privada o personalizada?

A: No. Actualmente, solo tenemos un bot en Jstris, que reside permanentemente en la sala de bot. Sin embargo, los bots privados pueden ser una realidad en el futuro.

### Q: ¿Qué significan esas abreviaturas en la tabla de resultados?

A: B2B = back-to-back. B2Bpm = back-to-back por minuto. APM = ataque por minuto. SPM = sent per minute (enviado por minuto). PPS = piezas por segundo. Rep = repetición.

![game results table][image9]

### Q: ¿Qué es el DAS?

A: DAS es una forma de sensibilidad horizontal de la pieza. DAS significa cambio automático retrasado (Delayed Auto Shift). Controla durante cuánto tiempo debe mantener presionadas las teclas izquierda o derecha antes de que el bloque se mueva en la dirección que desee. Con un DAS muy bajo, incluso el toque más ligero de una tecla hará que el bloque se mueva inmediatamente. Con un DAS muy alto, deberá mantener presionada la tecla durante más tiempo antes de que el bloque comience a moverse. Los profesionales en promedio tienden a usar un DAS más bajo porque la mayor sensibilidad les permite jugar más rápido. El DAS predeterminado en Jstris es 133. Si todavía se siente demasiado sensible, aumenta este número hasta que se sienta cómodo. Si se siente demasiado lento, baja el número. Ajústalo y encuentra lo que más te convenga.

### Q: ¿Qué es el ARR?

A: ARR es otra forma de sensibilidad horizontal de la pieza. ARR significa tasa de repetición automática (Auto Repeat Rate). Controla qué tan rápido se mueve el bloque hacia la izquierda o hacia la derecha. Esto es un poco más fácil de entender que DAS. En pocas palabras, con un ARR muy bajo, los bloques se moverán casi de inmediato a la dirección que desee al mantener presionadas las teclas izquierda o derecha. Con un ARR muy alto, los bloques se moverán muy lentamente en la dirección que desee al mantener presionadas las teclas izquierda o derecha. El ARR predeterminado en Jstris es 10.

### Q: ¿Qué es el Finesse?

A: Finesse se define como la forma más eficiente de mover un bloque. Buen finesse es importante para jugar de manera más suave y rápida. El número al lado de finesse indica cuántos errores de finesse se cometieron. Entonces, un puntaje de finesse de 0 significa que no cometió errores de finesse. Idealmente, cuanto más se acerque a 0, mejor. El finesse es algo que debe aprenderse para saber cómo hacerlo. Hay muchos recursos en línea que lo explican. Este video es un buen punto de partida: [Tutorial: How to Play Fast!](https://youtu.be/_QBs703nOnk?t=502).

### Q: ¿Puedo crear una sala privada?

A: Si. Haga clic en _Salas_, luego _Crear Sala_, luego marque la casilla que dice _Privado_. Copie y proporcione el enlace de la sala a cualquier persona que desee unirse a su sala privada. Aquí hay un consejo: toma el enlace de cualquier habitación, pública o privada, usando el comando `/ link`.

### Q: ¿Puedo jugar Jstris sin conexión?

A: Si. Para jugar sin conexión, primero debes descargar Jstris mientras estás en línea. Para hacer esto, haga clic derecho en la página de inicio, presione "Guardar como" y descargue el archivo html. Tenga en cuenta que solo los modos para un jugador se pueden jugar sin conexión, y las puntuaciones no se guardarán.

---

## Información Adicional

Jstris funciona completamente con donaciones. No hay anuncios de ningún tipo. Debido a la considerable cantidad de repeticiones almacenadas y datos del juego, se requiere un servidor potente para ejecutar Jstris. Todas las donaciones son muy apreciadas y ayudarán a mantener Jstris en funcionamiento. Consulte la sección [Acerca de](/about) en el sitio web para obtener más información.

[image2]: ./images/guide-intro.png "introduction"
[image4]: ./images/image4.png "MisaMino bot in opponents view"
[image8]: ./images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ./images/image5.png "the lobby, where you can join and create rooms"
[image11]: ./images/image11.png "team game in progress"
[image7]: ./images/image7.png "Solid Garbage"
[image10]: ./images/image10.png "Unmessy (-100)"
[image1]: ./images/image1.png "Messy (100)"
[image9]: ./images/image9.png "game results table"
