# Guide Jstris

Bienvenue sur Jstris, un jeu de bloc multijoueur en ligne simple. Jstris est stimulé par un gameplay rapide et sans lag et attire des joueurs talentueux du monde entier. Ce guide vous présentera les fonctionnalités de base du jeu.

- - -

**Table des matières**

- [Vue d'ensemble](#vue-d-ensemble)
- [Multijoueur](#multijoueur)
  - [Bot Room](#bot-room)
  - [1v1 Room](#1v1-room)
  - [Cheese Room](#cheese-room)
  - [Speed Limit Room](#speed-limit-room)
  - [Team Room](#team-room)
- [Jeu solo](#jeu-solo)
  - [Sprint](#sprint)
  - [Sprint fromage](#sprint-fromage)
  - [Ultra](#ultra)
  - [Survival](#survival)
  - [Maps](#maps)
- [Paramètres](#parametres)
  - [Attaques et combos](#attaques-et-combos)
  - [Distribution du handicap](#distribution-du-handicap)
  - [Bloquage du handicap](#bloquage du handicap)
  - [Randomiseur](#randomiseur)
  - [Prochains blocs](#prochains-blocs)
  - [Handicap solide](#handicap-solide)
  - [Délai d'effacement](#delai-d-effacement)
  - [Délai de handicap](#delai-de-handicap)
  - [Taux de désordre](#taux-de-desordre)
- [Foire Aux Questions](#faq)
  - [Q: Que signifient ces abréviations dans le tableau des résultats ?](#que-signifient-ces-abreviations-dans-le-tableau-des-resultats)
  - [Q: Qu'est-ce que le DAS?](#q-qu-est-ce-que-le-das)
  - [Q: Qu'est-ce que l'ARR?](#q-qu-est-ce-que-l-arr)
  - [Q: Qu'est-ce que la finesse?](#q-qu-est-ce-que-la-finesse)
  - [Q: Est-ce que je peux créer une partie privée?](#q-est-ce-que-je-peux-creer-une-partie-privee)
  - [Q: Est-ce qu'il existe une version hors-ligne de Jstris?](#q-est-ce-qu-il-existe-une-version-hors-ligne-de-Jstris)
- [Informations supplémentaires](#informations-supplementaires)

- - -

## Vue d'ensemble

Jstris utilise les mêmes mécaniques de base que la plupart des autres jeux similaires. Il suit des règles dites "Guidelines". L'une de ses caractéristiques notables est l'utilisation extensive des enregistrements. Dans chaque mode de jeu dans lequel vous jouez, pour chaque partie terminée, un enregistrement sera généré pour vous. Se regarder et s'analyser soi-même fait partie intégrante de l'amélioration de soi, et les parties enregistrées sur Jstris rendent tout cela très (trop ?) facile.

Contrairement à d'autres sites, vous pouvez être sûr que les classements de Jstris sont complètement exempts de toute triche. Les modérateurs travaillent 24 heures sur 24 pour supprimer les enregistrements suspects afin de vous garantir une liste fiable de records mondiaux. 

Il est recommandé de créer un compte sur Jstris. Pour ce faire, cliquez sur *S'inscrire* dans le coin supérieur droit. Seuls un courriel, un nom d'utilisateur et un mot de passe sont requis. Avec un compte, vous pouvez voir une multitude de statistiques, y compris vos meilleurs temps en mode solo, vos statistiques multijoueurs, vos statistiques d'amélioration, vos parties enregistrées, et bien plus encore. Vous pouvez aussi vous voir dans le classement (les scores des utilisateurs non enregistrés sont exclus). 

![introduction][image2]
- - -

## Multijoueur

### Bot Room

En arrivant sur le site, tous les joueurs sont immédiatement affectés à la **Bot Room**, une salle par défaut qui est ainsi nommée à cause du robot qui est toujours présent. Il est toujours situé dans le coin supérieur gauche de tous vos adversaires, facilement reconnaissable par sa couleur rouge uniforme.
![MisaMino bot in opponents view][image4]

Il y a 4 robots différents dans Jstris. Les voici, listés par force, avec les commandes pour sélectionner un robot spécifique, à entrer dans le tchat.
- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (supprimé le 21/09/2018)
- ~~Fool bot: `/changeBot fool`~~ (supprimé le 21/09/2018)

*\*Notez que toutes les commandes doivent être entrées entre la fin d'une partie et le début de la suivante. Toute commande entrée au cours d'une partie ne sera pas prise en compte.*

Misamino est de loin le robot le plus fort, peut-être le robot de placement de blocs le plus fort jamais créé. Réglé à 5 PPS (pièces par seconde), il devient un adversaire redoutable qui peut facilement terrasser les joueurs humains les plus forts dans un 1v1. Cependant, ses performances souffrent lorsqu'il y a plus de 5 humains dans la Bot Room, et il est probable qu'il se fasse éliminer rapidement. Ceci nous amène à notre prochain commande :  /botPPS.

La vitesse du robot peut être modifiée. Pour ce faire, tapez `/bot ?` et remplacez le ? par un nombre compris entre 0.3 et 5. Par exemple, si vous voulez que le robot joue à 2 PPS, tapez `/bot 2`. Si vous voulez que le bot joue à 1.73 PPS, tapez `/bot 1.73`. 

Jouer dans la Bot Room peut être difficile ! Ce qui est unique chez Jstris, c'est qu'il réunit d'humbles débutants et des adversaires de classe mondiale, ainsi que toute la palette de joueurs intermédiaires entre les deux. Si vous êtes fatigué et que vous voulez simplement regarder, utilisez la commande `/spectate` ou `/spec`. Pour revenir dans l'action, utilisez la commande `/play`. 

### 1v1 Room

La Bot Room n'est pas la seule partie disponible. Pour voir la liste complète des parties en cours, cliquez sur *Lobby* en bas à gauche de votre grille de jeu. La 2ème pièce la plus populaire sur Jstris est généralement la **1v1 Room**. Cette salle a un maximum de 2 utilisateurs jouant, bien que n'importe qui soit libre de venir et de regarder même si elle est pleine. Utilisez cette pièce pour régler des différends avec vos amis ou pour vous battre avec un joueur digne de ce nom. Si vous tenez compte du score, et que vous voulez le remettre à zéro, tapez `/resetCounter` et tous les scores seront réinitialisés.

### Cheese Room

Les lignes de handicap, aussi connues sous le nom de "fromage", sont le principal moyen d'éliminer les adversaires dans les modes multijoueurs. C'est une aptitude importante de savoir descendre dans le fromage. Entraînez-vous à descendre dans votre grille le plus vite possible dans la **Cheese Room**, une salle qui commence à jouer avec 10 lignes de handicap. Le premier à atteindre le bas de sa grille gagne. 10 lignes, c'est trop peu pour vous ? Ajustez le nombre de lignes de départ avec la commande `/set height ?`, le point d'interrogation représentant un nombre de 1 à 20. 

### Speed Limit Room

Vous voulez jouer avec un ami mais la différence de niveau entre vous est trop élevée ? Ou vous commencez à peine et vous en avez assez de perdre instantanément dans la Bot Room pleine de pros ? Il y a une salle "Speed Limit" disponible pour ça. La salle "Speed Limit" est réglée à 1,5 PPS par défaut, ce qui signifie qu'un joueur ne peut pas dépasser 1,5 PPS. Tout dépassement de cette limite entraînera le verrouillage temporaire de l'écran du joueur fautif. Toutes les salles "Speed Limit" sont indiquées par la petite icône de compteur de vitesse -[SPEEDOMETER_ICON]. Les parties personnalisées peuvent avoir n'importe quelle limite de vitesse de 0 PPS à 20 PPS. 

![the lobby, where you can join and create rooms][image5]

### Team Room

La dernière partie disponible par défaut est la **Team Room**. Choisissez un côté, rouge ou bleu, combattez et apportez la gloire à votre équipe. 

![team game in progress][image11]

- - -

## Jeu solo

### Sprint

Le mode de base, avec l'objectif le plus simple: **Sprint** est le mode solo le plus populaire sur Jstris. Effacez un nombre X de lignes aussi vite que possible. Jstris propose les modes Sprint 20, 40, 100 et 1000 lignes. 

### Sprint Fromage

Moins fonceur et plus analytique que Sprint, **Sprint fromage** exige plus de réflexion lorsque vous descendez dans les lignes de handicap de la façon la plus efficace. En Sprint fromage, Jstris propose les modes 10, 18, 100 et infini.

### Ultra

Axé sur le score et récompensant des techniques avancées, comme les T-spins et les Back-to-Backs, **Ultra** est un excellent moyen d'améliorer vos prouesses en attaque pour une utilisation en mode multijoueur. 

### Survival

Sans doute le plus difficile des modes solo, **Survival** ressemble beaucoup au Sprint fromage : seule différence, les lignes de handicap apparaissent à un rythme constant d'une ligne par seconde. Survivez le plus longtemps possible contre ces lignes montantes. 

### Maps

Récemment, le mode **Maps** a été introduit dans Jstris. Maps apporte un élément de créativité tout en préparant les joueurs à descendre efficacement dans leur grille, dans des contextes difficiles et inhabituels. Créez votre propre carte dans le *Map Designer*. Une fois publiée, n'importe qui dans le monde peut y jouer et concourir pour le temps le plus rapide. Il y a une limite de 5 cartes publiées par jour et 10 cartes non publiées en attente. Maps dispose également d'un classement global. Sur chaque carte, trois médailles sont décernées, Or pour la 1ère place, Argent pour la 2ème place et Bronze pour la 3ème place. Assurez votre place dans les trois premiers de n'importe quelle carte pour gagner des médailles et intégrer le haut du classement ! 

*\*Notez que le classement global est mis à jour 30 minutes après le début de chaque heure, donc les changements ne se répercutent pas immédiatement.*

- - -

## Paramètres

Pour voir les paramètres d'une partie sur Jstris, utilisez la commande `/config`. Nous allons maintenant passer en revue chacun des réglages. 

### Attaques et Combos

Les règles d'attaque et de combo par défaut dans Jstris (qui peuvent être personnalisées dans les parties privées) sont les suivantes :

| Type d'attaque     | Handicap   |   | Combo # | Handicap   |
| :----------------- | ---------: | - | ------: | ---------: |
| 0 ligne            |      **0** |   |       0 |      **0** |
| 1 ligne (single)   |      **0** |   |       1 |      **0** |
| 2 lignes (double)  |      **1** |   |       2 |      **1** |
| 3 lignes (triple)  |      **2** |   |       3 |      **1** |
| 4 lignes           |      **4** |   |       4 |      **1** |
| T-spin Double      |      **4** |   |       5 |      **2** |
| T-spin Triple      |      **6** |   |       6 |      **2** |
| T-spin Single      |      **2** |   |       7 |      **3** |
| T-spin Mini Single |      **0** |   |       8 |      **3** |
| Perfect Clear      |     **10** |   |       9 |      **4** |
| Back-to-Back       |     **+1** |   |      10 |      **4** |
|                    |            |   |      11 |      **4** |
|                    |            |   |     12+ |      **5** |

### Distribution du handicap

Il y a 4 systèmes différents concernant la façon dont les lignes de handicap sont envoyées pendant les parties multijoueurs :
- Targets `/set garbage targets`
- Divide `/set garbage divide`
- To all `/set garbage toAll`
- To least `/set garbage toLeast`

**Targets** est toujours la système par défaut (sauf dans la Team Room) et de loin la plus populaire. Dans Targets, une cible est tournée autour de chaque adversaire dans la partie, par incréments égaux et fixes, et la personne sur laquelle la cible a atterri au moment où vous envoyez les lignes de handicap est celle qui reçoit les lignes que vous avez envoyées. 

Dans le système **Divide**, les lignes que vous envoyez sont réparties également entre tous les joueurs. Par exemple, dans une salle avec 2 autres adversaires, si vous envoyez un T-spin Double (4 lignes), chacun de vos adversaires recevra alors 2 lignes. 

Dans le système **To all**, toutes les lignes que vous envoyez sont envoyées à chaque joueur dans la salle. Par exemple, dans une salle avec 4 adversaires, si vous envoyez un Perfect Clear (10 lignes), les 4 adversaires recevront chacun 10 lignes, soit un total de 40 lignes. Comme vous pouvez le supposer à partir de l'exemple, les parties avec un système "To all" ont tendance à être agitées, avec un nombre de lignes de handicap à croissance rapide et des parties généralement courtes. 

Dans le système **To least**, les lignes que vous envoyez sont envoyées au joueur qui dans la partie a reçu le moins de lignes jusqu'ici. Par exemple, dans une salle avec 3 autres adversaires, vous envoyez 4 lignes. L'adversaire A a déjà reçu 50 lignes dans le jeu au moment où vous avez envoyé l'attaque. L'adversaire B en a reçu 53. L'adversaire C en a reçu 58. Parce que l'adversaire A a reçu le moins de lignes jusqu'à présent, les 4 lignes lui seront envoyées.

### Bloquage du handicap

Il existe 4 systèmes de blocage du handicap sur Jstris :

- Plein
- Limité
- Aucun
- Instantané

**Plein** est le système de blocage par défaut sur Jstris. Les autres jeux similaires qui utilisent Full sont *Tetris Friends* (en mode e+) et *Tetris Online Poland*. Dans ce système, le handicap entrant apparait sous la forme d'une barre rouge à la droite de la grille de jeu. Le handicap n'apparaît pas dans la grille, cependant, jusqu'à ce qu'une pièce soit placée. Le handicap entrant peut être annulé avec des lignes envoyées (voir section précédente) et, en particulier, si vous avez déjà commencé un combo le handicap n'apparaîtra pas tant qu'il n'est pas terminé.

Le système de blocage **Limité** est très similaire au système Full mais comporte une différence. Le handicap entrant est inséré dès que vous déposez une pièce, qu'un combo ait déjà été lancé ou non. En d'autres termes, le handicap entrant n'est pas retardé par les combos comme dans le système Full. Comme dans le système Full, le handicap entrant peut être annulé avec les lignes envoyées. Les jeux similaires qui utilisent ce système sont entre autres *Puyo Puyo Tetris*, *Tetris Battle* et *Tetris Friends* (en mode non e+).

Dans le système de blocage **Aucun**, le handicap ne peut jamais être réduit ou annulé. Le handicap entrant apparaîtra d'abord sous la forme d'une barre rouge (comme dans Full et Limited) et seront ensuite insérés dans votre grille de jeu dès que vous aurez posé une pièce. Si un adversaire vous envoie 10 lignes, même si vous effacez 4 lignes avec votre prochaine pièce, le nombre de lignes de handicap ne sera pas réduit à 6. Au lieu de cela, vous recevrez toujours 10 lignes tout en en envoyant 4 à votre adversaire. 

Dans le système de blocage **Instantané**, il n'y a pas de barre rouge du tout. Dès qu'un adversaire envoie des lignes de handicap, elles apparaissent dans votre grille de jeu: il n'y a pas de blocage. 

|            | Barre rouge | Blocage |
| ---------- | :---------: | :-----: |
| Plein      |     Oui     |   Oui   |
| Limité     |     Oui     |   Oui   |
| Aucun      |     Oui     |   Non   |
| Instantané |     Non     |   Non   |

### Randomiseur

Les randomiseurs sont fondamentalement ce qui détermine l'ordre dans lequel vous obtenez les blocs. Jstris a 4 randomiseurs différents :
- 7-bag
- 14-bag
- Classic
- One Block

**7-bag** est le randomiseur standard et par défaut. Imaginez un petit sac avec 1 exemplaire de chacun des 7 blocs différents. Vous sortez maintenant, un par un, une pièce jusqu'à ce que le sac soit vide. Ensuite, vous obtenez un nouveau sac avec à nouveau 1 de chacun des 7 blocs différents. Vous les sortez un par un encore une fois. Répétez l'opération. Voici comment fonctionne le randomiseur à 7-bag. 

**14-bag** ressemble beaucoup à 7-sacs, seul le sac est doublé en taille, avec 2 exemplaire de chaque bloc. Une fois de plus, vous sortez chaque pièce du sac, une par une, jusqu'à ce que le sac soit vide. Rincez et répétez. 

Le randomizer **Classic** vous donne des pièces complètement aléatoires. Ce randomiseur rend l'empilement très difficile.

**One Block** est sans doute le randomiseur le plus bizarre de tous. Un bloc choisi au hasard est choisi pour vous au départ et vous n'obtiendrez que ce bloc spécifique pour l'ensemble de la partie. 

### Prochains blocks

Jstris affiche par défaut les 5 prochains blocs. Dans les parties personnalisées, vous pouvez paramétrer ce nombre entre 0 et 5. 

### Handicap solide

Le handicap solide consiste en des lignes qui s'élèvent du bas vers le haut pour "forcer le destin" d'une partie afin qu'elle ne dure pas indéfiniment. Elles sont un peu plus foncées que les lignes de handicap normales. Dans la Bot Room, le handicap solide commence à apparaître au bout de 2 minutes. Le handicap solide est également personnalisable dans les parties privées.
![Solid Garbage][image7]

### Délai d'effacement

Le délai d'effacement est un délai fixe qui s'écoule après que vous ayez effacé une ou plusieurs lignes. Pendant ce temps, vous ne pouvez rien faire. De nombreux jeux de blocs classiques ainsi que Puyo Puyo Tetris utilisent un délai d'effacement, mais Jstris par défaut a un délai de 0, et en général il n'est pas utilisé. Cependant, il est personnalisable si vous souhaitez l'activer. Sa plage d'utilisation va de 0 milliseconde à 6000 millisecondes.

### Délai de handicap

Le délai de handicap est un délai fixe entre l'arrivée des lignes de handicap indiquées par la barre rouge et l'insertion de ces ordures dans la grille de jeu. Par défaut, il est réglé à 500 millisecondes. Il est personnalisable sur une plage allant de 0 milliseconde à 1000 millisecondes. Un délai de handicap plus élevé permet de poser plus de pièces avant l'insertion des lignes en question, tandis qu'un délai plus faible permet de jouer moins de pièces avant leur insertion. En d'autres termes, plus le délai de handicap est élevé, plus les chances de bloquer plus efficacement sont grandes. Une autre façon de définir le délai de handicap est "le temps minimum pendant lequel une attaque entrante doit être visible dans la barre rouge avant qu'un bloc placé puisse déclencher l'insertion de ces lignes de handicap dans la grille de jeu".

### Taux de désordre

La taux de désordre fait référence au niveau de difficulté à nettoyer les lignes de handicap. Pour changer le taux de désordre des lignes de handicap dans une partie, utilisez la commande `/set messiness ?`, où le ? est remplacé par un nombre quelconque allant de -100 à 100. -100 est la configuration la moins "désordonnée", et le trou dans les lignes de handicap n'apparaîtra que dans une seule colonne pendant toute la durée du jeu (image de gauche). 100 est la configuration la plus désordonnée et le trou dans les lignes de handicap apparaîtra dans n'importe laquelle des 10 colonnes, ce qui rendra l'effacement des ces lignes beaucoup plus difficile (image de droite).

![Unmessy (-100)][image10] 
![Messy (100)][image1]

- - -

## FAQ

### Q: Que signifient ces abréviations dans le tableau des résultats ?

R: B2B = back-to-back. B2Bpm = back-to-back par minute. APM = attaques par minute. SPM = lignes envoyées par minute. PPS = pièces par seconde. Rep = replay.

![game results table][image9]

### Q: Qu'est-ce que le DAS?

R : Le DAS est une forme de sensibilité horizontale des pièces. DAS est l'abréviation de "Delayed Auto Shift". Il contrôle la durée pendant laquelle vous devez maintenir les touches gauche ou droite enfoncées avant que le bloc ne se déplace dans la direction souhaitée. Avec un DAS très bas, même la plus petite pression sur une touche enverra immédiatement le bloc en mouvement. Avec un DAS très élevé, vous devrez maintenir la touche enfoncée plus longtemps avant que le bloc ne commence à bouger. En moyenne, les professionnels ont tendance à utiliser un DAS plus faible parce que la sensibilité accrue leur permet de jouer plus rapidement. Le DAS par défaut sur Jstris est 133. S'il est encore trop sensible, augmentez ce nombre jusqu'à ce que vous vous sentiez à l'aise. S'il semble trop lent, optez pour un réglage plus bas. Ajustez et trouvez ce qui vous convient.

### Q: Qu'est-ce que l'ARR?

R : L'ARR est une autre forme de sensibilité horizontale des pièces. ARR signifie "Auto Repeat Rate" (taux de répétition automatique). Il contrôle la vitesse à laquelle le bloc se déplace vers la gauche ou vers la droite. C'est un peu plus facile à comprendre que DAS. Tout simplement, avec un ARR très bas, les blocs se déplaceront presque immédiatement dans la direction souhaitée en maintenant les touches gauche ou droite enfoncées. Avec un ARR très élevé, les blocs se déplaceront très lentement dans la direction souhaitée en maintenant les touches gauche ou droite enfoncées. L'ARR par défaut sur Jstris est 0, ce qui signifie qu'il est très rapide, presque instantané (souvenez-vous que Jstris est un des clients les plus rapides en moyenne). S'il vous semble trop rapide, augmentez le nombre jusqu'à ce que vous vous sentiez à l'aise.

### Q: Qu'est-ce que la finesse?

R : La finesse est définie comme le moyen le plus efficace de déplacer un bloc. Une bonne finesse est importante pour un jeu plus fluide et plus rapide. Le nombre à côté de la finesse indique combien d'erreurs de finesse ont été commises. Donc un score de finesse 0 signifie que vous n'avez commis aucune erreur de finesse.  Idéalement, plus vous vous rapprochez de 0, mieux c'est. La finesse est quelque chose qu'il faut apprendre pour savoir comment faire. Il existe de nombreuses ressources en ligne pour l'expliquer. Cette vidéo est un bon point de départ : [Tutoriel : Comment jouer vite !](https://youtu.be/_QBs703nOnk?t=502).

### Q: Est-ce que je peux créer une partie privée?

R : Oui. Cliquez sur *Parties*, puis sur *Créer unepartie*, puis cochez la case *Privé*. Copiez et donnez le lien de la salle à quiconque vous voulez inviter dans votre salle privée. Astuce : vous pouvez obtenir le lien de n'importe quelle partie, publique ou privée, en utilisant la commande `/link'.

### Q: Est-ce qu'il existe une version hors-ligne de Jstris?

R : Oui. Pour jouer hors ligne, vous devez d'abord télécharger Jstris pendant que vous êtes en ligne. Pour ce faire, faites un clic droit sur la page d'accueil, cliquez sur "Enregistrer sous", et téléchargez le fichier html. Notez que seuls les modes solo peuvent être joués hors ligne, et que les scores ne seront pas sauvegardés.
- - -

## Informations supplémentaires

Jstris fonctionne uniquement grâce aux dons. Il n'y a aucune publicité sur le site. En raison du nombre considérable d'enregistrements et de données de jeu stockées, un serveur puissant est nécessaire pour exécuter Jstris. Tous les dons sont très appréciés et permettront à Jstris de continuer à fonctionner - voir la section [À propos](/about) pour en savoir plus.

[image2]: ../images/guide-intro.png "introduction"
[image4]: ../images/image4.png "le robot MisaMino vus par les adversaires"
[image8]: ../images/image8.png "l'icône de compteur de vitesse pour les parties Speed Limit"
[image5]: ../images/image5.png "la liste des parties, où vous pouvez rejoindre et créer des parties"
[image11]: ../images/image11.png "partie en cours dans la Team Room"
[image7]: ../images/image7.png "Handicap Solide"
[image10]: ../images/image10.png "pas désordonné (-100)"
[image1]: ../images/image1.png "désordonné (100)"
[image9]: ../images/image9.png "tableau des résultats d'une partie"
