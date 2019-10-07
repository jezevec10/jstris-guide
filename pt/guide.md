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
  - [Pré-visualizações](#pré-vizualizações)
  - [Garbage Sólido](#garbage-sólido)
  - [Atraso de Limpeza](#atraso-de-limpeza)
  - [Atraso de Garbage](#atraso-de-garbage)
  - [Messiness](#messiness)
  - [Configurações predefinidas](#configurações-predefinidas)
  - [Modo](#modo)
- [Perguntas Frequentes](#perguntas-frequentes)
  - [Posso adicionar um bot à minha sala privada ou customizada?](#q-can-i-add-a-bot-to-my-private-or-custom-room)
  - [O que aquelas abreviações nos resultados do jogo significam?](#q-what-do-those-abbreviations-in-the-game-results-table-mean)
  - [O que é DAS?](#q-what-is-das)
  - [O que é ARR?](#q-what-is-arr)
  - [O que é finesse?](#q-what-is-finesse)
  - [Posso criar uma sala privada?](#q-can-i-create-a-private-room)
  - [Posso jogar Jstris offiline?](#q-can-i-play-jstris-offline)
- [Informação Adicional](#informação-adicional)

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
<<<<<<< HEAD
- ~~jez_Block: `/changeBot jez`~~ (removed on 2018.09.21)
- ~~Fool bot: `/changeBot fool`~~ (removed on 2018.09.21)
=======
- ~~jez_Block: `/changeBot jez`~~ (Removido em 21.09.2018)
- ~~Fool bot: `/changeBot fool`~~ (Removido em 21.09.2018)
>>>>>>> 340c6a8f9ccf4c0e28be270c3d4defdb6acaaa38

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

### Pré-visualizações

Jstris possui um padrão de 5 pré-visualizações. Em salas customizadas, você pode escolher de 0 a 5 pré-visualizações.

### Garbage Sólido

Garbage sólido são linhas não limpáveis que sobem para apressar o jogo para que ele não se estenda infinitamente. Eles são ligeiramente mais escuro que as linhas de garbage normais. Na Bot Room, o garbage sólido, por padrão, começam a surgir depois de 2 minutos. O garbage sólido é customizável nas Custom Rooms.

![Solid Garbage][image7]

### Atraso de Limpeza

O atraso de limpeza é um valor fixo de tempo que passa depois que você limpa qualquer linha. Durante este tempo, você não pode fazer nada. Muitos jogos clásicos de bloqueio e PPT usam o Atraso de Limpeza, mas o Jstris, por padrão, não possuí atraso, e na maioria das vezes nunca é usado aqui. De qualquer forma, o Atraso de Limpeza é customizável se você quiser liga-lo. Seu tempo vai de 0 à 6000 milisegundos.

### Atraso de Garbage

Atraso de Garbage é um valor fixo de tempo entre o garbage que está para vir, indicado pela barra vermelha, e a inserção deste garbage no campo de jogo. Por padrão, este atraso é de 500 milisegundos. Isto é customizável, podendo ser configurado de 0 à 6000 milisegundos. Um grande Atraso de Garbage permite o posicionamento de uma maior quantidade de peças antes do garbage ser inserido. Ou, em outras palavras, quanto maior o Atraso de Garbage, maior a oportunidade para bloquear de forma mais efetiva. Outra maneira de definir o Atraso de Garbage é "a quantidade mínima de tempo que um ataque deve ser visível na barra vermelha antes que um bloco posicionado ative a inserção daquele garbage ao campo de jogo". 

### Messiness

Messines de garbage é o nível de dificuldade para limpar certos tipos de garbage. Para alterar a Messines de garbage em uma sala, use o comando `/set messiness ?`, onde  ? deve ser substituido por qualquer número de -100 a 100. -100 é a configuração de garbage menos bagunçada, e o buraco do garbage aparecerá somente em uma coluna ao longo de todo jogo (imagem à esquerda). 100 é o garbage mais bagunçado, e o buraco do garbage aparecerá em qualquer uma das 10 colunas, tornando o downstack mais difícil (imagem à direita).

![Unmessy (-100)][image10] 
![Messy (100)][image1]

### Configurações predefinidas

Se há configurações que você particularmente gosta e quer salva-las, você pode guarda-las como predefinidas. 

Para isto, vá até *Lobby*, então *Criar Sala*, então selecione *Simples* ou *Todos*. Uma vez que você tenha customizado as configurações ao seu gosto, clique no botão *Salvar* no canto inferior direito para gerar os seus dados predefinidos. Copie isto e então cole na caixa de texto próxima ao Preset data na página [Submit a preset](/presets/submit).

Uma vez que você tenha enviado a configuração, você pode vê-la, assim como todas as outras configurações predefinadas pelos usuários na [List of presets](/presets). Agora você pode facilmente recriar a mesma sala sem precisar alterar as configurações novamente. Só vá até *Criar Sala*, então *Usar predefinição*, e então insira o título ou número de ID da sua predefinição. 

### Mode

Existem 7 diferentes maneiras de criar uma nova sala:

- Padrão
- Time
- Queijo
- Live Sprint
- Live Cheese
- Live Sobrevivência
- Live Maps v0.1

**Padrão** é um multijogador todos-contra-todos normal. 

**Time** cria uma Sala de Time customizada. Para configurar o nomde o seu time, use o comando `/set teamName ?`, onde o ? é substituido pelo nome do seu time.

**Queijo** cria uma Cheese Room. Cheese (queijo), também conhecido por garbage, é o jeito mais simples de nocautear os inimigos no modo multijogador. É uma habilidade importante para fazer o downstack no queijo. Pratique o quão rápido você consegue fazer o downstack neste modo que inicia o jogo com 10 linhas de garbage. O primeiro a chegar embaixo ganha. 10 linhas é fácil demais para você? Ajuste a quantidade de linhas iniciais com o comando `/set height ?`, com o ponto de interrogação representando um número de 1 a 20.

**Live Sprint** permite você jogar Maratona contra um oponente. O mais rápido à terminar a Maratona, ganha. A sala, por padrão, é maratona 40L, mas você pode mudar para qualquer tipo de Maratona com estes comandos:

- 20L:     `/set gamemode sprint20`
- 40L:     `/set gamemode sprint40`
- 100L:    `/set gamemode sprint100`
- 1000L:   `/set gamemode sprint1000`

Se você bater seu recorde de Maratona em uma Live Sprint, infelizmente, você não pode adicionar à sua conta, porque a Maratona será contida em pré-visualização live, não em uma pré-visualização normal. Mas você ainda pode salvar o replay ao seus favoritos se você quiser guarda-lo.

**Live Cheese** permite você jogar Queijo contra um oponente. O modo Live Cheese é virtualmente idêntico ao Queijo, porém, você não pode customizar as linhas iniciais além de 10L, 18L e 100L. A sala, por padrão, é 10L, mas você pode mudar para qualquer um desses outros tipos com estes comandos:

- 10L:     `/set gamemode cheese10`
- 18L:     `/set gamemode cheese18`
- 100L:    `/set gamemode cheese100`

**Live Survival** permite você jogar Sobrevivência contra um oponente. Quem sobreviver por mais tempo ganha.


**Live Mapas v0.1** cria um Map Room customizado. Tudo nesta sala funciona igual ao Map Room.

## Perguntas Frequentes

### P: Posso adicionar um bot à minha sala privada ou customizada? 

R: Não. Atualmente, nós temos somente um bot no Jstris, que reside permanentemente na Bot Room. De qualquer forma, bots privados podem virar realidade no futuro.

### P: O que aquelas abreviações nos resultados do jogo significam?

R: B2B = back-to-back. B2Bpm = back-to-back per minute. APM = attack per minute. SPM = sent per minute. PPS = pieces per second. Rep = replay.

![game results table][image9]

### P: O que é DAS?

R: DAS é uma forma de sensibilidade horizontal de peça. DAS significa Delayeed Auto Shift. Ele controla o tempo que você tem que segurar as teclas da esquerda ou direita antes do bloco mover para adireção que você quer. Com um DAS muito baixo, mesmo o toque mais leve em uma tecla irá colocar o bloco em movimento. Com um DAS muito alto, você terá de pressionar a tecla durante mais tempo para que o bloco se mova. Profissionais, em geral, tendem a usar um DAS lento, porque o aumento de sensibilidade os permite jogar mais rápido. O DAS padrão no Jstris é 133. Se você sente que está muito sensível, aumente o número até que fique confortável. Se sentir que está muito lento, diminua o número. Ajuste e descubra o que se encaixa melhor em você.

### P: O que é ARR?

R: ARR é outra forma de sensibilidade horizontal de peça. ARR significa Auto Repeat Rate. Ela controla o quão rápido um bloco move para esqueda ou direita. Isto é um pouco mais facil de entender do que o DAS. Ligeiramente simples: com uma ARR baixa, os blocos se moverão quase que imediatamente para a direção que você quer quando pressionar uma tecla; com uma ARR alta, os blocos se moverão mais devagar na direção que você quer quando pressionar uma tecla. A ARR padrão no Jstris é 10.

### P: O que é finesse?

R: Finesse é definida como a maneira mais eficiente de mover um bloco. Boa finesse é importante para jogar mais suave a rapidamente. O número próximo à finesse denota quantos erros de finesse foram cometidos. Então, 0 de pontuação em finesse significa que você não comete erros de finesse. Idealmente, quanto mais perto você chega do 0, melhor. Finesse é algo que precisa ser aprendido ao invés de saber como fazer. Existem diversos recursos online explicando isso.  Este vídeo é um bom começo: [Tutorial: How to Play Fast!](https://youtu.be/_QBs703nOnk?t=502)

### P: Posso criar uma sala privada?

R: Sim. Clique em *Lobby*, então *Criar sala*, então na caixa de seleção que diz *Privado*. Copie e dê o link da sala à qualquer um que vocẽ quer que entre. Aqui vai uma dica: arraste o link de qualquer sala, publica ou privada, usando o  comando `/link`.

### P: Posso jogar Jstris offline?

R: Sim. Para jogar offline, você tem que baixar o Jstris enquanto estiver online. Para isto, clique com o botão direito na página inicial, clique em "Salvar como", e baixe o arquivo html. Note que somente modos singleplayer podem ser jogados offiline, e as pontuações não serão salvas.

- - -

## Informação adicional


Jstris sobrivive inteiramente através de doações. Não há nenhum tipo de propagandas no site. Devido a considerável quantidade de replays e dados de jogos, é necessário um poderoso servidor para rodar o Jstris. Todas as doações são bem-vindas e irão ajudar a manter o Jstris vivo. veja a sessão [Sobre](/sobre) nos site e saiba mais. 

[image2]: ./images/guide-intro.png "introduction"
[image4]: ./images/image4.png "MisaMino bot in opponents view"
[image8]: ./images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ./images/image5.png "the lobby, where you can join and create rooms"
[image11]: ./images/image11.png "team game in progress"
[image7]: ./images/image7.png "Solid Garbage"
[image10]: ./images/image10.png "Unmessy (-100)"
[image1]: ./images/image1.png "Messy (100)"
[image9]: ./images/image9.png "game results table"
