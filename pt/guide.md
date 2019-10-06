# Guia Jstris

Bem-vindo ao Jstris, um jogo de blocos multijogador simples. Jstris é conhecido por sua jogabilidade rápida e vem atraindo jogadores talentosos de todo o mundo. Este guia irá te introduzir aos conceitos básicos do jogo.

- - -

**Índice**

- [Resumo](#resumo)
- [Controles](#controles)
- [Multijogador](#multijogador)
  - [Default Room](#default-room)
  - [Bot Room](#bot-room)
  - [1v1 Room](#1v1-room)
  - [Slow Room](#slow-room)
  - [Map Room](#map-room)
  - [Salas de Time](#salas-de-time)
- [Singleplayer](#singleplayer)
  - [Maratona](#sprint)
  - [Queijo](#cheese-race)
  - [Ultra](#ultra)
  - [Sobrevivência](#sobrevivência)
  - [Mapas](#mapas)
- [Configurações](#configurações)
  - [Tabela de Ataque e Combo](#tabela-de-ataque-e-combo)
  - [Distrubuição de Garbage](#distribuição-de-garbage)
  - [Bloqueio de Garbage](#bloqueio-de-garbage)
  - [Blocos](#blocos)
  - [Aleatorizador](#aleatorizador)
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

## Resumo

Jstris usa os mesmos conceitos básicos da maioria dos jogos de bloco. Ele segue algumas regras. Uma importante característica é o seu extensivo uso de replays. Em todo modo de jogo que você completa, um replay é gerado. Asstir e analizar suas jogadas é importante para melhorar suas habilidades, e os replays que o Jstri's cria fazem com que isso seja muito mais fácil.

Diferente de outros sites, você pode ter certeza que as classificações do Jstris são livres de trapaças. Moderadores vão remover as jogadas suspeitas para garantir uma lista de conquistas globais justa. 

Não é necessário se registrar para jogar mas, para usar todas as funcionalidades do site, é recomendado criar uma conta. Para isto, clique em *Registrar* no canto superior direito. Só um email, nome de usuário e senha são necessários. Com uma conta, você têm acesso à diversas estatísticas das suas melhores jogadas no modo singleplayer e multiplayer, estatísticas de melhoria, replays, e muito mais. Você pode também se ver na nas tabelas de classificações (usuários não registrados são excluidos das tabelas).

![introduction][image2]
- - -

## Controles

Jstris permite os jogadores customizarem seus controles a qualquer momento nas **Configurações** localizadas abaixo da área principal de jogo. Os controles padrões são:

|   Comando           | Tecla       |
| ------------------- | ----------- |
| Mover à esquerda    | esquerda    |
| Mover à direita     | direita     |
| Queda suave         | baixo       |
| Queda rápida        | espaço      |
| Girar à esquerda    | z           |
| Girar à direita     | cima        |
| Girar 180º          | a           |
| Segurar             | c           |

## Multijogador

### Default Room

Ao entrar no site, todos os jogadores são colocados na **Default Room**, uma sala todos-contra-todos onde você irá encontrar jogadores de todos os níveis de habilidade.

Jogar na Default Room pode ser complicado! O que é único no Jstris é que ele junta jogadores iniciantes e jogadores de nível profissional em uma mistura. Se você ficar cansado de jogar e quiser somente assistir, use o comando `/spectate` or `/spec`. Para jogar novamente, use o comando `/play`.

### Bot Room

A Default Room não é a única sala do Jstris. Para ver a lista completa de salas, clique em *Lobby* no canto inferior esquerdo da sua área de jogo. A segunda sala mais popular no Jstris é, normalmente, a **Bot Room**, que recebeu este nome por causa de um bot que está sempre por lá. Está sempre localizado no canto superior esquerdo de todos os seus oponentes, facilmente distinguível por sua cor uniformemente vermelha. 

![MisaMino bot in opponents view][image4]

Há 4 bots diferentes no Jstris. Aqui eles estão listados por força, e o comandos para mudar para um bot especifico, na caixa de texto.

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (removed on 2018.09.21)
- ~~Fool bot: `/changeBot fool`~~ (removed on 2018.09.21)

*\*Note que todos os comandos devem ser digitados entre as partidas. Qualquer comando digitado durante a partida será anulado.*

Misamino é de longe o bot mais forte, talvez o melhor em block placing já criado. Quando emparelhado com o máximo 5 PPS (peças por segundo), ele vira um oponente formidável que pode facilmente destruir os jogadores humanos mais habilidosos em um 1v1. De qualquer forma, a performance do bot sofre quando há mais que 5 humanos em uma Bot Room. Isto nos leva ao nosso próximo comando: `/botPPS`

A velocidade do bot pode ser alterada. Para isto, digite `/bot ?`, mudando apenas o ? para qualquer número entre .3 e 5. Por exemplo, se eu quiser um bot para jogar à 2PPS, eu digito `/bot 2`. Se eu quiser
um bot para jogar à 1.73 PPS, eu digito `/bot 1.73`.

### 1v1 Room

A **1v1 Room** tem no máximo 2 jogadores, porém, todos podem entrar para assistir. Use esta sala para batalhar contra seus amigos ou contra um oponente à altura. Se você está mantendo a pontuação, e quer apaga-la, digite `/resetCounter` e os pontos voltarão a ser 0.

### Slow Room

Quer jogar com um amigo, mas o nível de habilidade entre vocês é muito grande? Ou está cansado de perder instantâneamente nas Bot Room? Ou quer melhorar a eficiência em jogo tirando o fator velocidade? Para estas ocasiões, existem a Slow Rooms. As Slow Rooms padrões tem o limite de velocidade de 2.0 PPS, o que significa que um jogador não pode passar de 2.0 PPS. Qualquer tentativa de ir mais rápido irá resultar no bloqueio temporário da tela do jogador. Junto ao limite de velocidade, a Slow Room possui uma atraso da limpeza linear de 700 milisegundos. O que significa que para cada linha que você limpar, há um tempo de 700 ms antes que você possa jogar novamente. Todas as Slow Rooms são indicadas pelo pequeno ícone de velocímetro - [SPEEDOMETER_ICON]. Slow Rooms customizadas podem ter qualquer limite de velocidade entre 0 20 PPS. 

![the lobby, where you can join and create rooms][image5]

### Map Room

A **Map Room** é o lugar disputar a melhor classificação em aleatóriamente escolhidos criados pelos usuários. O (D=?%) mostrado próximo a cada mapa é a porcentagem dificuldade do mapa, sendo 0% o mais fácil e 100% o mais difícil. Mapas que exigem Perfect Clear Finish não são incluidos.

### Salas de Time

A última sala padrão é a **Salas de Time**. Escolha um lado, vermelho ou azul, e a batalha irá trazer a glória para o seu time.

![team game in progress][image11]

- - -

## Singleplayer

### Maratona

A base, e com o objetivo mais simples, **Maratona** é o modo um-jogador mais popular no Jstris. Limpe X quantidade de linhas o mais rápido que conseguir. Jstris oferece  modos **Maratona** de 20, 40, 100, e 1000 linhas.

### Queijo

Menos impetuosa e mais analítica que a Maratona, **Queijo** requer mais pensamento conforme você limpa os blocos da maneira mais eficiente. Jstris oferece o modo de jogo Queijo com 10, 18, 100 e infinitas linhas.

### Ultra

Focada em pontuação e recompensando técnicas avançadas como t-spins e back-to-backs, **Ultra** é um bom modo de melhorar sua destreza de ataque para jogar nos modos Multijogador.

### Sobrevivência

Possivelmente o modo singleplayer mais desafiador, **Sobrevivência** é parecido com Queijo, porém, o garbage sobe a uma taxa constante de uma linha por segundo. Sobreviva contra as linhas que sobem pelo maior tempo que você conseguir. 

### Mapas

No final de 2018, o modo **Mapas** foi introduzido ao Jstris. Os mapas trazem um elemento de criatividade e também prepara os jogadores para limpar as linhas mais efetivamente em posições difíceis e incomuns. Crie seu próprio mapa em **Criador de Mapas**. Uma vez publicado, qualquer um no mundo pode jogar e competir pelo melhor tempo. Há um limite de 5 mapas publicados por dia e 10 não públicados na fila. Mapas também possuem uma classificação. Em todo mapa, três medalhas são dadas: Ouro para o 1º colocado, Prata para o 2º e Bronze para o terceiro. Pontue entre os três melhores em qualquer mapa para ganhar algumas medalhas e assegurar sua colocação.

*\*Note que a classificação de Mapas atualiza somente algumas vezes por dia, logo, novas mudanças podem não ser instantâneas.*

- - -

## Configurações

To see the configuration of any room on Jstris, use the command `/config`. Now we will go over each of the settings. 

Para ver as configurações de qualquer sala no Jstris, use o comando `/config`. Agora nos vamos passar por cada uma dos ajustes.

### Tabela de Ataque e Combo

A tabela padrão de ataque e combo no Jstris (que pode ser customizada em salas privadas) é a seguinte:

| Tipo de ataque     | Linha enviada |   | Combo # | Linha enviada |
| :----------------- | ------------: | - | ------: | ------------: |
| 0 lines            |      **0**    |   |       0 |      **0**    |
| 1 lines (single)   |      **0**    |   |       1 |      **0**    |
| 2 lines (double)   |      **1**    |   |       2 |      **1**    |
| 3 lines (triple)   |      **2**    |   |       3 |      **1**    |
| 4 lines            |      **4**    |   |       4 |      **1**    |
| T-spin Double      |      **4**    |   |       5 |      **2**    |
| T-spin Triple      |      **6**    |   |       6 |      **2**    |
| T-spin Single      |      **2**    |   |       7 |      **3**    |
| T-spin Mini Single |      **0**    |   |       8 |      **3**    |
| Perfect Clear      |     **10**    |   |       9 |      **4**    |
| Back-to-Back       |     **+1**    |   |      10 |      **4**    |
|                    |               |   |      11 |      **4**    |
|                    |               |   |     12+ |      **5**    |

### Distribuição de Garbage

Há 8 formas diferentes de como o garbage é enviado durante as partidas multijogador. São as seguintes:

- Targets `/set garbage targets`
- Divide `/set garbage divide`
- To all `/set garbage toAll`
- To least `/set garbage toLeast`
- To most `/set garbage toMost`
- To self `/set garbage toSelf`
- Random `/set garbage random`
- Roulette `/set garbage roulette`

**Targets** é sempre o padrão (exceto em Salas de Times) e é, de longem o mais popular. Em Targets, um alvo é passado por todos os oponentes da sala, em incrementos iguais e fixos, e em quem o alvo parar no momento em que você enviou o garbage é o que irá receber. 

No sistema distribuição de garbage **Divide** (GDS), todo o garbage que você envia é igualmente dividido entre todos os jogadores. Por exemplo, em uma sala com 2 oponentes, se você envia um T-spin Double (4 lines), cada um dos seus oponentes receberá 2 linhas.

No GDS **To all**, todo garbage que você enviar vai para todos os jogadores da sala. Por exemplo, em uma sala com 4 oponentes, se você enviar um Perfect Clear (10 linhas), todos os 4 oponentes irão recebeer 10 linhas cada, ou um total de 40 linhas. Como você pode supor pelo exemplo, salas com To all garbage tendem a ser agitadas, com rápida subida de garbage e jogos característicamente curtos.

No GDS **To least**, o garbage que você envia vai para o jogador que *recebeu* menor garbage até então. Por exemplo, em uma sala com 3 oponentees, você envia 4 linhas. Oponete A recebe 50 linhas já no momento em que você enviou o ataque. Oponente B recebeu 53. Oponentee C recebeu 58. Já que o oponente A reecebeu a menor quantidade de linhas, as 4 linhas da sua line clear serão enviadas a ele.

No GDS **To most**, o garbage que você envia é mandado para o jogador que *enviou* o maior garbage. Em suma, você está atraindo o jogador mais forte da sala.

No GDS **To self**, o garbage que você envia vai para você mesmo. É imprático no multijogador, mas é útil para praticar sozinho.

No GDS **Random**, o garbage que você envia vai para um jogador aleatório. Discutivelmente o mais justo dos GDS.

No GDS **Roulette**, o garbage que você envia vai para um jogador aleatório, *incluindo você*.

### Bloqueio de Garbage

Existem 4 tipos de sistema de Bloqueio de Garbage no Jstris. Eles são:

- Full
- Limited
- None
- Instant

**Full** é o sistema de bloqueio padrão no Jstris. Outros usuários que usam Ful são *TF* (salas e+) e *TOP*. No sistema de bloqueio de garbage Full, o garbage que chega aparece como uma barra vermelha à sua direita. Ele não sobe no seu campo de jogo até que você posicione uma peça. O garbage que chega pode ser reduzido com as linhas enviadas e, se você já iniciou um combo, ele ficará completamente parado até que você finalize o combo.

Sistema de bloqueio **Limited** é muito similar ao Full, mas com uma diferença. O garbage que chega é inserido assim que você posiciona uma peça, independente se um combo foi ou não iniciado. Em outras palavras, o garbage que chega não pausa durante os combos da maneira que o Full faz. Como o Full, o garbage que chega pode ser reduzido com as linhas enviadas. Usuários que usam Limiteed incluem *PPT*, e *TB*, e *TF* (salas não e+).

No sistema de bloqueio **None**, um garbage não pode ser reduzido ou cancelado. O garbage que chega a você irá primeiro aparecer com uma barra vermelha (assim como no Full e no Limited) e então ser inserido no campo de jogo assim que você posicionar uma peça. Se um oponente envia 10 linhas para você, mesmo se você limpar 4 linhas com sua próxima peça, o garbage não irá reduzir à 6. Ao invés disso, você ainda receberá 10 linhas enquanto envia 4 ao oponente.

No sistema de bloqueio **Instant**, a barra vermelha não é mostrada. No momento que o oponente envia um ataque, o garbega irá subir em seu campo. Não há nenhum bloqueio.

|         | Barra vermelha (queue) | Bloqueio? |
| ------- | :--------------------: | :-------: |
| Full    |          Sim           |    Sim    |
| Limited |          Sim           |    Sim    |
| None    |          Sim           |    Não    |
| Instant |          Não           |    Não    |

### Blocos

Há 8 tipos diferentes de blocos

- Standard
- Big
- ARS
- Penta
- M123
- All-28
- C2RS
- O-spin

**Standard** Estes são os mais usados e básicos tetrominos que você provavelmente conhece. Estes são os blocos padrões

**Big** Quatro vezes maior que os blocos padrões, estes causarão um dano massivo utilizados.

**ARS** Blocos padrões com ARS (Arika rotation system), incluindo CC-check. Implementado por NueSB.

**Penta** Estes blocos são pentominós. Existem 18 pentominós únicos. 

**M123** Minos de tamanho 1, 2 e 3. Há 4 blocos M123 únicos.

**All-28** Todos os minos de tamanho 1, 2, 3, 4 e 5. Uma combinação de padrão, M123 e Penta.

**C2RS** Blocos padrões com o sistema de rotação Cultris 2

**O-spin** Um sistema de rotação meme onde 0-spin triplo (2xCW) e 0-spin quadruplo (1xCC2) são possíveis. Também, outros giros não convencionais são permitidos (devido à kick table que possui 15 kick levels em oposição ao SRS que tem 4).

### Aleatorizador

Aleatorizadores são basicamente a formula para a ordem de blocos você recebe. Jstris possui 11 aleatorizadores diferentes. Eles são:

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

**7-bag** É o aleatorizaodor padrão. Imagine uma pequena bolsa com 1 bloco de cada um dos 7. Agora você desenha a peça, um por um, até que a bolsa esteja vazia. Agora você desnha on por um mais uma vez. Repita. E é assim que o aleatorizador 7-bag funciona.

**14-bag** É parecido com o 7-bag, mas com o dobro de tamanho, com 2 de cada um dos 7 blocos. Mais uma vez, você desenha cada peça da bolsa, um por um, até que a bolsa esteja vazia. Repita.

**Classic** Te dá peças complentamente aleatórias. Este aleatorizador faz o empilhamento ser muito difícil.

**C2Sim** Uma simulação do aleatorizador Cultris 2, descrito neste [post](http://harddrop.com/forums/index.php?showtopic=5080&st=0&p=71443&#entry71443) feito pelo Integration.

**One block** Este aleatorizador te dá um bloco aleatório no começo do jogo e você só receberá este bloco no jogo inteiro.

**Two Block** Este aleatorizador é parecido com o One Block, mas ele alterna entre dois blocos específicos.

**One 7-bag** A mesma bolsa de 7 peças é repetida indefinidamente. Usando este aleatorizador, você receberá sempre a mesma sequência de 7 peças.

**One 14-bag** A mesma bolsa de 14 peças é repetida indefinidamente. Usando este aleatorizador, você recebe sempre a mesma sequência de 14 peças.

**Repeat+7b** Funciona como o 7-bag, mas cada peça da bolsa pode ser repetida em qualquer momento de 1 a 7 vezes.

**BSblock+7b** Um 7-bag normal, com exceção de que peças de diferentes Block Sets (por isso o BS no nome), como pentominós ou Big Blocks, podem aparecer.

**BigBlock+7b** Um 7-bag normal, com exceção de que Big Blocks podem aparecer.

### Previews

Jstris possui um padrão de 5 pré-visualizações. Em salas customizadas, você pode escolher de 0 a 5 pré-visualizações.

### Solid Garbage

Solid garbage are unclearable lines that rise up from the bottom to “hurry up” the game so it doesn’t extend indefinitely. They are slightly darker than normal garbage lines. In the Bot Room, solid garbage by default starts to come after 2 minutes. Solid garbage is also customizable in custom rooms.

![Solid Garbage][image7]

### Clear Delay

Clear delay is a fixed amount of time that passes after you clear any line(s). During this time, you can’t do anything. Many classic block games and PPT use clear delay, but Jstris by default has 0 delay, and for the most part it is never used here. However, it is customizable if you want to turn it on. Its range is 0 milliseconds to 6000 milliseconds.

### Garbage Delay

Garbage delay is a fixed amount of time between the incoming garbage indicated by the red bar and the insertion of that garbage into the playfield. By default, it is set at 500 milliseconds. It is customizable from a range of 0 milliseconds to 60000 milliseconds. A higher garbage delay allows for more pieces to be played before garbage is inserted, while a lower garbage delay allows for less pieces to be played before garbage insertion. Or in other words, the higher the garbage delay, the more opportunity it gives to block more effectively. Another way to define garbage delay is “the minimumum amount of time an incoming attack has to be visible in the red bar before a placed block can trigger the insertion of that garbage to the playfield.”

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
- Live Sobrevivência
- Live Maps v0.1

**Standard** mode is normal multiplayer free-for-all. 

**Team** mode creates a custom Salas de Time. To set your own team name, use the command `/set teamName ?` where the ? is replaced with your team name. 

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

**Live Survial** mode allows you to play Sobrevivência against an opponent(s). Whoever survives the longest wins.

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

[image2]: ../images/guide-intro.png "introduction"
[image4]: ../images/image4.png "MisaMino bot in opponents view"
[image8]: ../images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ../images/image5.png "the lobby, where you can join and create rooms"
[image11]: ../images/image11.png "team game in progress"
[image7]: ../images/image7.png "Solid Garbage"
[image10]: ../images/image10.png "Unmessy (-100)"
[image1]: ../images/image1.png "Messy (100)"
[image9]: ../images/image9.png "game results table"