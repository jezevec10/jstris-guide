# Jstris Guide

Willkommen zu Jstris, einem simplen online Multiplayer Blockspiel. Jstris ist für schnelles Gameplay bekannt und spricht talentierte Spieler aus der ganzen Welt an. Dieser Guide wird dich mit den grundlegenden Features des Spiels vertraut machen.

- - -

**Inhaltsverzeichnis**

- [Jstris Guide](#jstris-guide)
  - [Überblick](#überblick)
  - [Steuerung](#steuerung)
  - [Mehrspieler](#mehrspieler)
    - [Standardraum](#standardraum)
    - [Botraum](#botraum)
    - [1v1 Raum](#1v1-raum)
    - [Langsamer Raum](#langsamer-raum)
    - [Map Raum](#map-raum)
  - [Einzelspieler](#einzelspieler)
    - [Sprint](#sprint)
    - [Cheese Race](#cheese-race)
    - [Ultra](#ultra)
    - [Survival](#survival)
    - [Maps](#maps)
    - [20TSD](#20tsd)
  - [Konfiguration](#konfiguration)
    - [Angriffs- und Combotabelle](#angriffs--und-combotabelle)
    - [Müllverteilung](#müllverteilung)
    - [Müllblockierung](#müllblockierung)
    - [Blöcke](#blöcke)
    - [Zufallsgenerator](#zufallsgenerator)
    - [Vorschau](#vorschau)
    - [Fester Müll](#fester-müll)
    - [Sperrverzögerung](#sperrverzögerung)
    - [Löschverzögerung](#löschverzögerung)
    - [Schwerkraftslevel](#schwerkraftslevel)
    - [Müllverzögerung](#müllverzögerung)
    - [Müllunordnung](#müllunordnung)
    - [Voreinstellungen](#voreinstellungen)
    - [Mode](#mode)
  - [FAQ](#faq)
    - [Q: Kann ich einen Bot zu meinem privaten oder angepassten Raum hinzufügen?](#q-kann-ich-einen-bot-zu-meinem-privaten-oder-angepassten-raum-hinzufügen)
    - [Q: Was bedeuten diese Abkürzungen in der Spielergebnistabelle?](#q-was-bedeuten-diese-abkürzungen-in-der-spielergebnistabelle)
    - [Q: Was ist DAS?](#q-was-ist-das)
    - [Q: Was ist ARR?](#q-was-ist-arr)
    - [Q: Was ist Finesse?](#q-was-ist-finesse)
    - [Q: Can I create a private room?](#q-can-i-create-a-private-room)
    - [Q: Kann ich Jstris offline spielen?](#q-kann-ich-jstris-offline-spielen)
  - [Zusätzliche Informationen](#zusätzliche-informationen)

- - -

## Überblick

Jstris benutzt die selben Mechaniken wie die meisten anderen Blockspiele. Es folgt den Guideline Regeln. Ein wichtiges Feature sind Replays der Spiele. In jedem Spielmodus in dem du spielst wird ein Replay für dich erstellt. Das Anschauen und Analysieren von Replays ist ein wichtiger Teil der Selbstverbesserung, und die Jstris Replays machen das sehr leicht.

Anders als andere Seiten, kannst du dir sicher sein, dass die Jstris Bestenlisten komplett sauber und frei von Cheatern sind. Moderatoren werden verdächtige Rekorde entfernen um eine vertrauenswürdige Liste aufrecht zu halten.

Es ist möglich ohne Registration zu spielen, aber um alle Features der Webseite nutzen zu können, ist es empfehlenswert einen Account zu erstellen. Klicke dafür in der oberen rechten Ecke auf *Registrieren*. Es werden nur Email, Benutzername und Passwort benötigt. Mit einem Account kannst du verschiedene Statistiken einsehen, inklusive deiner Bestzeiten in Singleplayermodi, Multiplayerstatistiken, Verbesserungsstatistiken, Replays und mehr. Du wirst außerdem noch auf den Bestenlisten zu sehen sein (die Spiele unregistrierter Spieler werden nicht angezeigt).

![Einführung][image2]
- - -

## Steuerung

Spieler können auf Jstris ihre Steuerung zu jeder Zeit im **Optionen** Menü einstellen, welches sich unter dem Hauptspielfeld befindet. Die

| Aktion          | Standardtaste |
| --------------- | ------------- |
| Bewegung Links  | Links         |
| Bewegung Rechts | Rechts        |
| Leichter Fall   | Unten         |
| Harter Fall     | Leertaste     |
| Rotiere Links   | z*            |
| Rotiere Rechts  | Oben          |
| Rotiere 180     | a             |
| Hold            | c             |

*\*Es ist empfehlenswert diese Taste auf Y umzustellen, damit dies auf der deutschen QWERTZ Tastatur die eigentlich bedachte Steuerung wiederspiegelt.*

## Mehrspieler

### Standardraum

Sobald man die Seite betritt, tritt man automatisch dem **Standardraum** bei, einem "Free-for-all" wo du auf Spieler jeden Skilllevels triffst.

Im Standardraum zu spielen kann schwer sein! Was einzigartig an Jstris ist, dass es Anfänger sowie Topspieler in einen Topf wirft, zusammen mit jedem zwischendrin. Sobald du eine Pause einlegen möchtest, benutze den Befehl `/spectate` oder `/spec`. Benutze den Befehl `/play`, sobald du wieder spielen möchtest.

### Botraum

Der Standardraum ist nicht der einzige Raum. Klicke auf *Lobby* unten links von deinem Spielfeld, um die vollständige Raumliste einzusehen. Der zweitpopulärste Raum ist üblicherweise der **Botraum**, wessen Namensgebung von einem Bot kommt, welcher zu jeder Zeit anwesend ist. Er ist immer oben links in der Gegnerliste und durch die rote Farbe leicht zu unterscheiden.

![MisaMino Bot aus der Sicht der Gegner][image4]

Es gibt 4 verschiedene Bots in Jstris. Hier werden sie nach Stärke gelistet, zusammen mit den Befehlen um sie zu ändern, welche in die Chatbox eingegeben werden.

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (entfernt am 21.09.2018)
- ~~Fool bot: `/changeBot fool`~~ (entfernt am 21.09.2018)

*\*Beachte, dass alle Befehle zwischen Spielen eingegeben werden müssen. Alle Befehle während eines Spiels werden ignoriert.*

Misamino ist bei weitem der stärkste Bot, möglicherweise sogar der stärkste Blockspiel-Bot welcher jemals gemacht wurde. Wenn dieser auf die maximale Geschwindigkeit von 5 PPS (pieces per second) eingestellt wird, stellt es einen starken Gegner dar, welcher selbst die stärksten menschlichen Spieler in einem 1v1 besiegen kann. Die Stärke des Bots sinkt aber, sobald sich mehr als 5 Spieler im Botraum befinden, und es wird schnell den oberen Bildschirmrand erreichen. Dies bringt uns schon zu unserem nächsten Befehl: `/botPPS`

Die Geschwindigkeit des Bots kann verändert werden. Benutze den Befehl `/bot ?` und ersetze das ? mit einer Zahl zwischen 0,3 und 5,0. Wenn ich zum Beispiel gegen den Bot mit 2 PPS spielen möchte, würde ich den Befehl `/bot 2` benutzen. Wenn ich gegen den Bot mit 1,73 PPS spielen möchte, benutze ich `/bot 1.73` (Dezimalzahlen mit Punkt statt Komma schreiben).

### 1v1 Raum

Der **1v1 Raum** hat eine maximale Spieleranzahl von 2 Spielern, aber es steht jedem frei zu kommen und zuzuschauen, auch wenn der Raum voll ist. Benutze diesen Raum um gegen deine Freunde anzutreten oder gegen einen würdigen Gegner anzutreten. Falls ihr Punkte zählt und den Zähler zurücksetzen möchtet, benutzt `/resetCounter` und alle Punktzahlen werden auf 0 zurückgesetzt.

### Langsamer Raum

Falls du mit einem Freund spielen willst und euer Skillunterschied zu groß ist, falls du frisch anfängst und es satt bist immer direkt im Botraum mit den ganzen Topspielern zu verlieren, oder wenn du deine Effizienz verbessern willst, indem du Geschwindigkeit erstmal außen vor lässt, gibt es den langsamen Raum. Der Standard langsame Raum ist auf 2,0 PPS begrenzt, was bedeutet, dass ein Spieler die Geschwindigkeit 2,0 PPS nicht überschreiten kann. Sobald man zu schnell ist, wird eine Warnung angezeigt und das Spielfeld ist für kurze Zeit gesperrt. Dazu kommt noch, dass der langsame Raum eine Zeilenauflöseverzögerung von 500 Millisekunden hat. Das bedeutet, dass du für jede Zeile die du clearst 500ms warten musst. Alle langsamen Räume werden mit dem kleinen Tachometer Icon angezeigt - [SPEEDOMETER_ICON]. Angepasste langsame Räume können eine beliebige Geschwindigkeitsbegrenzung von 0 PPS bis zu 20 PPS haben.

![Die Lobby, wo du Räumen beitreten kannst und auch selber Räume erstellen kannst][image5]

### Map Raum

Der **Map Raum** ist ein Ort um sich zu schnell wie möglich durch die zufällig ausgewählten, nutzer-erstellten Maps durchzuarbeiten. Das "(D=?%)" neben jeder Map stellt die Schwierigkeit jeder Map da, wobei 0% die einfachste und 100% die schwerste darstellt. Maps mit einer "Perfect Clear" Bedingung werden hier nicht in Betracht gezogen.

- - -

## Einzelspieler

### Sprint

Der Spielmodus mit dem einfachstem Ziel ist **Sprint**, welches der populärste Einzelspielermodus auf Jstris ist. Dazu muss man X Zeilen so schnell wie möglich auflösen. Jstris bietet 20, 40, 100 und 1000 Zeilen Sprintmodi an.

### Cheese Race

Der **Cheese Race** stellt einen nicht so hecktischen Modus dar. Während man sich durch die Müllzeilen so effizient wie möglich arbeitet, muss mehr nachgedacht werden als im Sprint. Jstris bietet 10, 18, 100 und Unendlich Zeilen Cheese Race Modi an.

### Ultra

Der **Ultra** Modus fokussiert sich auf Punktzahl und fortgeschrittenen Techniken, wie T-Spins oder Back-to-backs. Es ist ein toller Modus um deine Offensivkraft für den Mehrspieler Modus zu verbessern.

### Survival

Der wahrscheinlich schwerste Einzelspielermodus ist **Survival** (Überleben). Dieser ist ähnlich wie Cheese Race, nur dass der Müll mit einer konstanten Geschwindigkeit von einer Zeile pro Sekunde steigt. Überlebe so lange wie du kannst.

### Maps

Gegen Ende von 2018 wurde der **Maps** Modus eingeführt. Maps kombinieren ein Element von Kreativität und ein Element des effizienten Downstackens in schweren und ungewöhnlichen Situationen zusammen. Du kannst eingene Maps im *Map Designer* erstellen. Sobald du diese veröffentlicht hast, kann die ganze Welt sie spielen und auf die beste Zeit spielen. Es gibt ein Limit von 5 veröffentlichten und 10 unveröffentlichten Maps am Tag. Maps haben außerdem eine Bestenliste. Es werden auf jeder Map drei Medallien vergeben, Gold für den 1. Platz, Silber für den 2. Platz und Bronze für den 3. Platz. Hol dir einen Top-3 Platz auf einer Map um Medallien zu gewinnen und dir deinen Platz auf der Bestenliste zu sichern!

*\*Beachte, dass Mapbestenlisten nur ein paar Mal am Tag aktualisiert werden, also sind neue Rekorde nicht direkt zu sehen.*

### 20TSD

Das Ziel in diesem Modus ist so viele TSDs (T-Spin Doubles) hintereinander wie möglich zu bekommen. Wenn du eine Zeile auflöst, welche kein TSD war, endet das Spiel. Es heißt 20TSD, da das Originalkonzept aus einem 40-Zeilen Sprint aus 20 TSDs bestand (20 x 2 = 40). Manche Leute haben es aber geschafft darüber hinauszuwachsen und überschreiten jetzt regelmäßig die 20.

- - -

## Konfiguration

Benutze den Befehl `/config` um die Konfiguration eines Raumes in Jstris einzusehen. Jetzt werden wir jede Einstellung behandeln.

### Angriffs- und Combotabelle

Die Standard Angriffs- und Combotabelle in Jstris (welche in privaten Räumen verändert werden kann) sieht wie folgt aus:

| Angriffsart        | Gesendete Zeilen |     | Combo # | Gesendete Zeilen |
| :----------------- | ---------------: | --- | ------: | ---------------: |
| 0 Zeilen           |            **0** |     |       0 |            **0** |
| 1 Zeilen (Single)  |            **0** |     |       1 |            **0** |
| 2 Zeilen (Double)  |            **1** |     |       2 |            **1** |
| 3 Zeilen (Triple)  |            **2** |     |       3 |            **1** |
| 4 Zeilen           |            **4** |     |       4 |            **1** |
| T-Spin Double      |            **4** |     |       5 |            **2** |
| T-Spin Triple      |            **6** |     |       6 |            **2** |
| T-Spin Single      |            **2** |     |       7 |            **3** |
| T-Spin Mini Single |            **0** |     |       8 |            **3** |
| Perfect Clear      |           **10** |     |       9 |            **4** |
| Back-to-Back       |           **+1** |     |      10 |            **4** |
|                    |                  |     |      11 |            **4** |
|                    |                  |     |     12+ |            **5** |

### Müllverteilung

Es gibt 8 verschiedene Wege in denen Müll in Mehrspielerräumen verteilt werden kann.

- Ziele (Targets) `/set garbage targets`
- Aufgeteilt (Divide) `/set garbage divide`
- An alle (To all) `/set garbage toAll`
- Zum Wenigsten (To least) `/set garbage toLeast`
- Zum Meisten (To most) `/set garbage toMost`
- Zu sich selbst (To self) `/set garbage toSelf`
- Zufällig (Random) `/set garbage random`
- Roulette (Roulette) `/set garbage roulette`

**Ziele** (Targets) ist der Standard (außer in Teamräumen) und bei Weitem der populärste. Hier wird ein Ziel bewegt, welches in gleichen und regelmäßigen Abständen über jeden Gegner rotiert. Wer auch immer im Moment in dem du Müll sendest das Ziel ist, ist die die den Müll erhalten wird.

Im **Aufgeteilt** (Divide) Müllverteilungssystem (garbage distribution system, GDS) wird der Müll den du sendest gleich an alle Spieler verteilt. Wenn du zum Beispiel in einem Raum mit zwei anderen Gegnern bist und du einen T-Spin Double machst (4 Zeilen), wird jeder Gegner zwei Zeilen Müll bekommen.

Im **An alle** (To all) Müllverteilungssystem wird dein Müll an jeden Spieler gesendet. Wenn du zum Beispiel in einem Raum mit 4 Gegnern bist und du einen Perfect Clear machst (10 Zeilen), wird jeder Gegner 10 Zeilen bekommen. Wie sich leicht aus dem Beispiel erkennen lässt, sind Räume mit "An alle" sehr hecktisch, mit schnell steigendem Müll und sehr kurzen Runden.

Im **Zum Wenigsten** (To least) Müllverteilungssystem wird der Müll an den Spieler gesendet, welcher bisher den wenigsten Müll *erhalten* hat. Wenn du zum Beispiel in einem Raum mit 3 Gegnern bist und du 4 Zeilen sendest und Spieler A bisher 50, B 53 und C 58 Zeilen erhalten hat, bekommt A den Müll, da er bisher die wenigsten Zeilen erhalten hat.

Im **Zum Meisten** (To most) Müllverteilungssystem wird der Müll an den Spieler gesendet, welcher bisher den meinsten Müll *gesendet* hat. Damit wird der stärkste Spieler im Raum angegriffen.

Im **Zu sich selbst** (To self) Müllverteilungssystem wird der Müll an einen selbst gesendet. Zwar ist dieser Modus für den Mehrspielermodus ungeeignet, aber nützlich wenn man alleine damit üben möchte.

Im **Zufällig** (Random) Müllverteilungssystem wird der Müll an einen zufälligen Gegner gesendet.

Im **Roulette** Müllverteilungssystem wird der Müll an eine zufällige Person gesendet, *inklusive einem selbst*.

### Müllblockierung

Auf Jstris gibt es 4 unterschiedliche Müllblockierungsysteme.

- Vollständig (Full)
- Begrenzt (Limited)
- Kein (None)
- Sofort (Instant)

**Vollständig** ist das Standardmüllblockierungsystem auf Jstris. Andere Spiele, welche Vollständig benutzen, sind *TF* (e+ Räume) und *TOP*. Im Vollständig Müllblockierungsystem erscheint der ankommende Müll als roter Balken am rechten Spielfeldrand. Diese werden aber nicht direkt in dein Spielfeld eingesetzt, sondern erst, wenn du einen Stein platzierst. Der ankommende Müll kann mit gesendeten Zeilen verringert werden und, falls du eine Combo gestartet hast, wird warten, bis du diese abgeschlossen hast.

Das **Begrenzt** Müllblockierungsystem ist dem Vollständig System sehr ähnlich, aber mit einem entscheidenden Unterschied. Der ankommende Müll wird direkt eingesetzt sobald du einen Stein platzierst, egal ob du dich in einer Combo befindest oder nicht. Ähnlich wie in Full kann der ankommende Müll mit gesendeten Zeilen verringert werden. Spiele, welche Begrenzt benutzen, sind *PPT*, *TB* und *TF* (Nicht-e+ Räume).

Im **Kein** Müllblockierungsystem kann Müll nicht reduziert werden. Ankommender Müll wird, wie in Full oder Begrenzt, als roter Balken am rechten Spielfeldrand erscheinen und dann ins Spielfeld eingesetzt werden, sobald du einen Stein platzierst. Wenn dein Gegner dir 10 Zeilen sendet, dann wird, auch wenn du mit dem Stein danach 4 Zeilen sendest, der Müll nicht auf 6 reduziert werden. Stattdessen erhältst du 10 Zeilen und sendest gleichzeitig 4 Zeiten an deinen Gegner.

Im **Sofort** Müllblockierungsystem gibt es überhaupt keinen roten Balken. Sobald der Gegner dir Zeilen sendet, wird dieser direkt auf deinem Spielfeld erscheinen. Du kannst diesen nicht blocken.

|             | Roter Balken | Blockbar? |
| ----------- | :----------: | :-------: |
| Vollständig |      Ja      |    Ja     |
| Begrenzt    |      Ja      |    Ja     |
| Kein        |      Ja      |    No     |
| Sofort      |     Nein     |   Nein    |

### Blöcke

Es gibt 8 verschiedenen Blockarten.

- Standard
- Groß (Big)
- ARS
- Penta
- M123
- All-29
- C2RS
- O-spin

**Standard** Dies sind die am meist verbreiteten und grundlegendsten Tetrominos, mit welchen du wahrscheinlich am vertrautetesten bist.

**Groß** Diese sind 4-mal größer als die Standardblöcke und werden im Spielverlauf sehr viele Zeilen senden.

**ARS** Standard Blöcke mit dem ARS (Arika rotation system), inklusive CC-check. Implementiert von NueSB

**Penta** Diese Blöcke sind Pentominos. Es gibt 18 verschiedene Pentominos.

**M123** Minos der Größen 1,2,3. Es gibt 4 verschiedene M123 Blöcke.

**All-29** Alle minos der Größen 1,2,3,4,5, insgesamt 29 verschiedene Minos. Eine Kombination der 7 Standard, 4 M123 und 18 Penta Blöcke.

**C2RS** Standardblöcke mit dem Cultris 2 Rotationssystem

**O-spin** Ein Meme Rotationssystem, bei welchem O-Spin Triple (2xCW) und O-Spin Quadruple (1xCCW) möglich sind. Außerdem sind viele andere ungewöhnliche Spins möglich (da die Kicktabelle 15 Kicklevel hat, anders als SRS, welches nur 4 hat).

### Zufallsgenerator

Zufallsgenerator entscheiden welche und in welcher Reihenfolge du Blöcke bekommst. Jstris hat 11 verschiedenen Zufallsgeneratoren.

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

**7-bag** ist der Standard-Zufallsgenerator. Stell dir einen kleinen Beutel mit je 1 der 7 verschiedenen Blöcke vor. Nun ziehe einen Stein nach dem anderen heraus, bis der Beutel leer ist. Dann bekommst du einen neuen Beutel mit wiederum 1 Stück von jedem der 7 verschiedenen Blöcke. Nun ziehst du einen nach dem anderen noch einmal heraus. Dies wird wiederholt, bis das Spiel zu ende ist. So funktioniert der 7-bag-Zufallsgenerator.

**14-bag** ist ähnlich wie 7-bag, nur dass der Beutel doppelt so groß ist, mit 2 von jedem der 7 Blöcke. Du ziehst wieder jedes Stück einzeln aus dem Beutel, bis der Beutel leer ist.

Der **Classic** Zufallsgenerator gibt dir völlig zufällige Blöcke. Dieser Zufallsgenerator macht das Stacken sehr schwer.

**C2Sim** Eine Simulation des Zufallsgenerators von Cultris 2, beschrieben in diesem [Beitrag von Integration](http://harddrop.com/forums/index.php?showtopic=5080&st=0&p=71443&#entry71443)

**One Block** Dieser Zufallsgenerator gibt dir einen zufällig ausgewählten Block, der zu Beginn für dich ausgewählt wird, und du erhältst nur diesen einen Block für das gesamte Spiel.

**Two Block** Dieser Zufallsgenerator ist wie der Ein-Block-Zufallsgenerator, nur dass er stattdessen zwischen zwei bestimmten Blöcken wechselt.

**One 7-Bag** Der gleiche Beutel mit 7 Steinen wird unbegrenzt wiederholt. Wenn du diesen Zufallsgenerator verwendest, erhalten Sie immer wieder die gleiche Abfolge von 7 Blöcken.

**One 14-bag** Der gleiche Beutel mit 14 Steinen wird unbegrenzt wiederholt. Wenn du diesen Zufallsgenerator verwendest, erhalten Sie immer wieder die gleiche Abfolge von 14 Blöcken.

**Repeat+7b** Funktioniert wie 7-bag, nur dass jedes Stück im Beutel eine Chance hat, 1-7 Mal wiederholt zu werden.

**BSblock+7b** Normaler 7-Beutel, mit der Ausnahme, dass Stücke aus verschiedenen Blocksätzen (daher das BS im Namen), wie Pentomino oder Big Blocks, erscheinen können.

**BigBlock+7b** Normaler 7-Bag mit der Ausnahme, dass Big Blöcke vorkommen können.

### Vorschau

Jstris hat standardmäßig 5 Vorschaublöcke. In angepassten Räumen kann du zwischen 0 und 5 Vorschaublöcken wechseln.

### Fester Müll

Fester Müll sind unentfernbare Zeilen, die von unten aufsteigen, um das Spiel zu "beschleunigen", damit sich das Spiel nicht hinauszieht. Sie sind etwas dunkler als normale Müllzeilen. Im Bot-Raum erscheint der solide Müll standardmäßig nach 2 Minuten. Fester Müll ist auch in angepassten Räumen anpassbar.

![Fester Müll][image7]

### Sperrverzögerung

Die Sperrverzögerung gibt an, wie viel Zeit ein Block auf dem Boden verbleiben kann, bevor es einrastet. In Jstris gibt es drei Arten von Sperrverzögerungen, die angepasst werden können. Die erste, L1, steuert, wie viele Millisekunden ein Block braucht bis es einrastet, nachdem es auf den Boden fallen gelassen wurde. Die Standardverzögerung L1 beträgt 500 ms. Die zweite, L2, gibt an, wie viele Millisekunden ein Block braucht bis es einrastet, nachdem es gesoftdroppt wurde und durch Links- und Rechtsbewegung aktiv gehalten wird. Die Standardverzögerung L2 beträgt 5000 ms. Beachte, dass, wenn ein Block gedreht wird, L2 zurückgesetzt wird und das Stück länger als 5000 ms aktiv bleiben kann, was uns zu L3 bringt. Die dritte, L3, ist die maximale Zeitspanne, die ein Block hat bevor es sich automatisch sperrt, egal wie sehr es aktiv gehalten wird. Die Standardverzögerung L3 beträgt 20000 ms.

### Löschverzögerung

Die Löschverzögerung ist eine festgelegte Zeitspanne, die vergeht, nachdem eine oder mehrere Zeilen gelöscht wurden. Während dieser Zeit kann man nichts tun. Viele klassische Blockspiele und PPT verwenden Clear Delay, aber Jstris hat standardmäßig eine Verzögerung von 0, und in den meisten Fällen wird es hier nie verwendet. Es ist jedoch anpassbar, falls man es einschalten möchte. Sein Bereich reicht von 0 ms bis 6000 ms.

### Schwerkraftslevel

Das Schwerkraftslevel bezieht sich auf die Geschwindigkeit, mit der die Stücke automatisch in die Matrix fallen. Die Schwerkraft kann von 0-28 eingestellt werden. Die Standardeinstellung ist 1. Wenn die Schwerkraft 0 ist, fällt das Stück überhaupt nicht nach unten, bis es nach der 20 Sekunden lange L3-Sperrverzögerung automatisch eintritt (siehe Abschnitt [Sperrverzögerung](#sperrverzögerung)). Ein Schwerkraftslevel von 28 bedeutet 20G, was bedeutet, dass die Figuren sofort von oben nach unten "fallen".

### Müllverzögerung

Müllverzögerung ist eine feste Zeitspanne zwischen dem ankommenden Müll (angezeigt mit dem roten Balken an der rechten Seite) und dem Eintreten des Mülls ins Spielfeld. Standardmäßig beträgt diese 500ms. Diese ist von 0ms bis 60000ms veränderbar. Eine höhere Müllverzögerung ermöglicht das Platzieren von mehr Blöcken vor dem Eintreten des Mülls. Mit anderen Worten, je höher die Müllverzögerung, desto mehr Chancen bietet sie, es effektiver zu blocken. Eine andere Möglichkeit die Müllverzögerung zu definieren, ist "die minimale Zeitspanne, die ein eingehender Angriff im roten Balken sichtbar sein muss, bevor ein platzierter Block die Einfügung dieses Mülls in das Spielfeld auslösen kann".

### Müllunordnung

Müllunordnung beschreibt den Schwierigkeitsgrad um bestimmte Arten von Müll zu beseitigen. Um die Müllunordnung zu verändern, benutze den Befehl `/set messiness ?`, bei welchem das ? mit einer Zahl von -100 bis 100 ersetzt wird. -100 ist die ordentlichste Einstellung und die Mülllücke wird für das Spiel nur in einer Spalte auftauchen (Linkes Bild). 100 ist die unordentlichste Einstellung und die Mülllücke wird in jedem der 10 Spalten auftauchen, was das Downstacken viel schwerer macht (rechtes Bild).

![Ordentlich (-100)][image10]
![Unordentlich (100)][image1]

### Voreinstellungen

Wenn es eine Konfiguration der Raumeinstellungen gibt, die dir gefällt und auf die du einfach zurückgreifen möchtest, kannst du die Einstellungen als Voreinstellung speichern.

Gehen Sie dazu auf *Lobby*, dann *Raum erstellen*, dann entweder auf die Registerkarte *Einfach* oder *Alle*. Wenn du die Einstellungen nach deinen Wünschen angepasst hast, drücke auf die Schaltfläche *Speichern* in der unteren rechten Ecke, um deine Voreinstellungsdaten zu erzeugen. Kopiere diese und füge sie dann in das Kästchen neben den Voreinstellungsdaten auf der Seite [Voreinstellung senden](/presets/submit) ein.

Sobald du deine Voreinstellung eingereicht hast, kannst du diese zusammen mit den Voreinstellungen anderer diese auf der Seite [Liste der Voreinstellungen](/presets) einsehen. Jetzt kannst du den gleichen Raum erstellen, ohne alle Einstellungen wieder einstellen zu müssen. Dafür musst du nur auf *Raum erstellen*, dann *Angepasste Voreinstellungen verwenden* und dann entweder den Titel oder die ID der Voreinstellung eingeben.

### Mode

Es gibt momentan 7 verschiedene Modi, welcher ein neu erstellter Raum annehmen kann. Diese sind:

- Standard
- Team
- Käse (Cheese)
- Live Sprint
- Live Käse (Cheese)
- Live Überleben (Survival)
- Live Maps v0.1

**Standard** ist ein normaler Free-For-All Mehrspielermodus.

Im **Team**-Modus wird ein benutzerdefinierter Teamraum erstellt. Wähle eine Seite, rot oder blau, kämpfe und bring Ruhm und Ehre für dein Team. Benutze den Befehl `/set teamName ?` um einen eigenen Teamnamen festzulegen, wobei das ? durch den Teamnamen ersetzt wird.

![Teamspiel][image11]

**Käse** erstellt einen Käseraum. Müll, welcher oft als Käse bezeichnet wird, ist der Hauptweg um deine Gegner in Mehrspielermodi zu besiegen. Das Downstacken durch Käse ist ein wichtiger Bestandteil des Spiels. Hier wird ein Modus gespielt, bei dem man sich durch 10 Müllzeilen durchkämpft. Der erste, der alle Müllzeilen entfernt hat, gewinnt. 10 Zeilen sind zu wenig? Mit dem `/set height ?` Befehl kannst du die Anzahl der Zeilen von 1 bis 20 einstellen.

Der **Live Sprint** Modus erlaubt es dir gegen eine andere Person zu sprinten. Der schnellste gewinnt. Der Raum ist standardmäßig auf einen 40L (Zeilen, engl. line) Sprint eingestellt, aber du kannst es mit folgenden Befehlen zu einem anderen Sprintmodus wechseln:

- 20L:     `/set gamemode sprint20`
- 40L:     `/set gamemode sprint40`
- 100L:    `/set gamemode sprint100`
- 1000L:   `/set gamemode sprint1000`

Falls du deinen Sprintrekord in einem Live Sprint schlägst, kannst du es leider nicht zu deinem Account hinzufügen, da der Sprint in einem Live Replay und nicht einem Standardreplay abgespeichert ist. Aber du kannst ihn trotzdem zu deinen Favoriten hinzufügen, falls du ihn behalten möchtest.

**Live Käse** erlaubt es dir, den Käsemodus gegen andere Spieler zu spielen. Live Käse ist dem normalen Käsemodus nahezu identisch, mit der Ausnahme dass man die Zeilen nur auf 10L, 18L und 100L einstellen kann. Der Raum ist standardmäßig auf 10L eingestellt, aber du kannst diese mit folgenden Befehlen verändern.

- 10L:     `/set gamemode cheese10`
- 18L:     `/set gamemode cheese18`
- 100L:    `/set gamemode cheese100`

**Live Survial** erlaubt es dir, den Überlebensmodus gegen andere Spieler zu spielen. Wer am längsten überlebt gewinnt.

**Live Maps v0.1** erstellt einen Map Raum. Alles funktioniert so, wie in einem normalen Map Raum.

## FAQ

### Q: Kann ich einen Bot zu meinem privaten oder angepassten Raum hinzufügen?

A: Nein. Derzeit haben wir nur einen Bot auf Jstris, der sich ständig im Bot Room befindet. Private Bots könnten jedoch in Zukunft hinzugefügt werden.

### Q: Was bedeuten diese Abkürzungen in der Spielergebnistabelle?

A: B2B = back-to-back. B2Bpm = back-to-back pro Minute. APM = Angriff pro Minute. SPM = Sent (gesendet) pro Minute. PPS = Blöcke per second. Rep = Replay.

![Spielergebnistabelle][image9]

### Q: Was ist DAS?

A: DAS ist eine Form der horizontalen Eingabeempfindlichkeit. DAS steht für verzögerte automatische Verschiebung (delayed auto shift). Es gibt an, wie lange die linke oder rechte Taste gedrückt gehalten werden muss, bevor sich der Block in die gewünschte Richtung bewegt. Bei einem sehr niedrigen DAS führt selbst die leichteste Berührung einer Taste dazu, dass sich der Block sofort bewegt. Bei einer sehr hohen DAS müssen Sie die Taste länger gedrückt halten, bevor sich der Block bewegt. Profis neigen dazu, eine niedrigere DAS zu verwenden, weil die erhöhte Empfindlichkeit ihnen schnelleres Spielen ermöglicht. Die Standard-DAS auf Jstris ist 133 (ms). Wenn sie sich zu empfindlich anfühlt, kannst diese Zahl erhöhen, bis du dich wohl fühlst. Wenn sie sich zu langsam anfühlt, verringere die Zahl. Probier aus und schau was dir passt.

### Q: Was ist ARR?

A: ARR ist eine andere Form der horizontalen Eingabeempfindlichkeit. ARR steht für automatische Wiederholrate (auto repeat rate). Es gibt an, wie schnell sich der Block nach links oder rechts bewegt. Das ist etwas einfacher zu verstehen als DAS. Ganz einfach: Bei einer sehr niedrigen ARR schellen die Blöcke fast sofort in die gewünschte Richtung, wenn die linke oder rechte Taste gedrückt gehalten wird. Bei einer sehr hohen ARR bewegen sich die Blöcke sehr langsam in die gewünschte Richtung. Die Standard-ARR auf Jstris ist 10 (ms).

### Q: Was ist Finesse?

A: Finesse ist als die effizienteste Art und Weise definiert, einen Block zu verschieben. Eine gute Finesse ist wichtig, um flüssiger und schneller spielen zu können. Die Zahl neben der Finesse gibt an, wie viele Finesse-Fehler begangen wurden. Eine Finesse-Zahl von 0 bedeutet also, dass keine Finesse-Fehler begangen wurden.  Im Idealfall gilt: Je näher man der 0 kommt, desto besser. Finesse ist etwas, das erst gelernt werden muss, bevor man weiß wie man es umsetzt. Es gibt viele Onlineressourcen, die es erklären. Dieses Video ist ein guter Start: [Tutorial: Wie man schnell spielt! (Englisch)](https://youtu.be/_QBs703nOnk?t=502).

### Q: Can I create a private room?

A: Yes. Klicke auf *Lobby*, Dann *Raum erstellen*, und dann markiere das *Privat* Kästchen. Kopiere den Raumlink und sende ihn jedem, den du zu deinem Raum einladen möchtest. Tipp: Du kannst den `/link` Befehl nutzen um einen Link von einem beliebigen Raum zu erhalten, egal ob öffentlich oder privat.

### Q: Kann ich Jstris offline spielen?

A: Ja. Damit du offline spielen kannst, musst du zuerst Jstris herunterladen, während du online bist. Klicke dazu mit der rechten Maustaste auf der Homepage, klicke "Speichern als..." und lade die HTML datei herunter. Beachte, dass nur Einzelspieler-Modi offline gespielt werden können, und die Ergebnisse nicht gespeichert werden.

- - -

## Zusätzliche Informationen

Jstris läuft vollständig über Spenden. Es gibt keinerlei Werbung. Aufgrund der großen Menge an gespeicherten Replays und Spieldaten ist für den Betrieb von Jstris ein leistungsfähiger Server erforderlich. Alle Spenden sind sehr willkommen und helfen, Jstris am Leben zu erhalten - siehe den Abschnitt [Über](/about) auf der Website, um mehr zu erfahren.

[image2]: ./images/guide-intro.png "Einführung"
[image4]: ./images/image4.png "MisaMino Bot aus der Sicht der Gegner"
[image8]: ./images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ./images/image5.png "Die Lobby, wo du Räumen beitreten kannst und auch selber Räume erstellen kannst"
[image11]: ./images/image11.png "Teamspiel"
[image7]: ./images/image7.png "Fester Müll"
[image10]: ./images/image10.png "Unmessy (-100)"
[image1]: ./images/image1.png "Messy (100)"
[image9]: ./images/image9.png "Spielergebnistabelle"
