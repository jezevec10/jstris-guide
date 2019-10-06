# Jstris 导航-游戏指南-Jstris Guide

欢迎来到Jstris，一个简单的在线多人方块游戏。Jstris向来以低延迟的游戏著称，并且吸引着世界上的各路神仙玩家前来。该指南将向你介绍本游戏的基本事项。

## 写在最前：
这篇文章不会完全翻译自Eddie的英文Guide，会以尽量适合中文玩家的说法以及信息进行说明。（意译和重写）

为了让各位与歪果仁进行英语交流时减少障碍，保留了部分常用英语词汇。

对这篇导航进行完善？[请进群](https://jq.qq.com/?_wv=1027&k=58mxfPJ)进行交流！

- - -


## **目录-Table of Contents**

- [总览-Overview](#总览-overview)
- [多人游戏-Multiplayer](#多人游戏-multiplayer)
  - [默认房-Default Room](#默认房-default-room)
  - [机器人房-Bot Room](#机器人房-bot-room)
  - [单挑房-1v1 Room](#单挑房-1v1-room)
  - [挖掘房-Cheese Room](#挖掘房-cheese-room)
  - [慢速房-Slow Room](#慢速房-slow-room)
  - [地图房-Map Room](#地图房-map-room)
  - [组队房-Team Room](#组队房-team-room)
- [单人游戏-Singleplayer](#单人游戏-singleplayer)
  - [竞速模式-Sprint](#竞速模式-sprint)
  - [挖掘竞速-Cheese Race](#挖掘竞速-cheese-race)
  - [限时极限-Ultra](#限时极限-ultra)
  - [生存模式-Survival](#生存模式-survival)
  - [地图-Maps](#地图-maps)
- [系统设置-Configuration](#系统设置-configuration)
  - [攻击连击表-Attack and Combo table](#攻击连击表-attack-and-combo-table)
  - [垃圾行分配方式-Garbage Distribution](#垃圾行分配方式-garbage-distribution)
  - [垃圾行抵消-Garbage Blocking](#垃圾行抵消-garbage-blocking)
  - [序列生成器-Randomizer](#序列生成器-randomizer)
  - [预览数-Previews](#预览数-previews)
  - [实心垃圾行-Solid Garbage](#实心垃圾行-solid-garbage)
  - [消行延迟-Clear Delay](#消行延迟-clear-delay)
  - [垃圾行生效延迟-Garbage Delay](#垃圾行生效延迟-garbage-delay)
  - [垃圾行混乱度-Messiness](#垃圾行混乱度-messiness)
  - [配置预设-Configuration presets](#配置预设-configuration-presets)
  - [模式-Mode](#模式-mode)
- [常见问题解答 FAQ-Frequently Asked Questions](#常见问题解答-faq)
  - [Q: 我能在私房或者自定义房间使用bot吗？](#q-我能在私房或者自定义房间使用bot吗)
  - [Q: 游戏结果当中的各种英文……都是啥？](#q-游戏结果当中的各种英文都是啥)
  - [Q: 加速（器）怎么弄?自动加速延迟 (DAS) ?自动重复间隔 (ARR) ?](#q-加速器怎么弄自动加速延迟das自动重复间隔arr)
  - [Q: 操作最优化？多余操作？finesse？](#q-操作最优化多余操作finesse)
  - [Q: 我能建立私房(private room)吗？](#q-我能建立私房-private-room-吗)
  - [Q: 我可以离线玩Jstris吗？](#q-我可以离线玩jstris吗)
- [附加信息-Additional Information](#附加信息-additional-information)

- - -

## 总览-Overview

和其他大多数方块一样，Jstris使用世界基准（Guideline）规则。值得一提的是Jstris的录像回放（Replay）系统。每次游戏后都会自动生成游戏录像，观看回放、分析并自我提升，在Jstris的录像回放系统里都非常简单。

不同于其他网站，你可以相信Jstris的排行榜完全清白，拒绝作弊。排行榜由管理员（Moderators）时常查看并移除可疑的记录，来确保真实可信的全球成就表。（发现可疑记录也可以联系管理员检查哦~）

虽然点开即玩，无需注册，但仍然推荐在jstris上创建一个属于你自己的账号。点一下右上的注册，顺次写下用户名、邮箱、两遍密码就可以了。在拥有账号后，你可以查看大量关于你的个人数据，包括你的单人竞速模式下的最佳时间、多人游戏数据、进步数据、回放、等等。你还能在排行榜上看到你自己的名字（未注册也可以）！

![introduction][image2]

[\[回到目录\]](#目录-table-of-contents)
- - -

## 键位控制-Controls

Jstris可以让玩家在主游戏区下方的**设置**菜单自定义键位。默认键位如下：


|      操作命令         |   默认键位   |
| -------------------- | ----------- |
| 左移动                | ←           |
| 右移动                | →           |
| 软降（方块加速下落）    | ↓           |
| 硬降（方块直接到底）    | 空格(space) |
| 左转（逆时针）         | z           |
| 右转（顺时针）         | ↑           |
| 180°转                | a           |
| 暂存 (Hold)           | c           |

~~不推荐使用默认键位~~

[\[回到目录\]](#目录-table-of-contents)

## 多人游戏-Multiplayer

点击游戏区域底部左侧的 *大厅-Lobby* 按钮查看完整的房间列表。

### 默认房-Default Room

在进入网站后，所有玩家都会立即进入默认的**默认房-Default Room**，面向所有人开放。你可以在这里找到各种等级的技术选手。

所以在默认房里面可能会吃瘪！Jstris的一大特点就是可以让新手和世界级大触混合在一起，进行大混战。如果你玩累了
并想观战，可以输入`/spectate`或`/spec`进行旁观。想再次游戏时输入`/play`即可。

（旁观状态小提示：对手游戏区域右侧有一个放大镜按钮，点击可以选用**全屏模式-Full Screen**来隐藏自己的游戏区，能够更好的进行旁观）
 
[\[回到目录\]](#目录-table-of-contents)

### 机器人房-Bot Room

当然房间不只有默认房一个。点击游戏区域下方左侧的**大厅**查看完整的列房间表。Jstris中第二受欢迎的房间通常就是***机器人房-Bot Room**了。这样称呼这个房间是因为1个Bot（机器人）永远在线，位置就在你所有对手的左上角，还有着红色方块，在人群当中特别显眼易区分~

![MisaMino bot in opponents view][image4]

下面是在Jstris里按强度顺序列出的4个不同的Bot。在聊天框内输入对应指令可以更改Bot类型。

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (于2018.09.21删除)
- ~~Fool bot: `/changeBot fool`~~ (于2018.09.21删除)

*\*注意：只能在一场游戏结束后，下一场开始前输入指令，在游戏进行时输入的指令会被忽略。*

Misamino是目前已知的最强bot之一 ~~zzz尚未嵌入到js当中，等一个奏大爷适配~~ ，当bot使用5PPS（块/秒）的速度时，可以在单挑房内轻松暴打最强人类选手。然而bot在多人房间时表现并不佳，经常很快就会死掉。

所以你可以使用`/bot [PPS] `的命令来控制bot的摆块速度。[PPS]的取值区间为 0.3~5。
如`/bot 2 `即将bot的摆块速度改为2块/秒，`/bot 1.73 `改为1.73块/秒等。

[\[回到目录\]](#目录-table-of-contents)

### 单挑房-1v1 Room

**单挑房-1v1 Room**最多只能 2 人同时游玩，不过即使满人了其他人也可以进房旁观。来1v1 Room，和你的朋友，或者旗鼓相当的对手一决高下吧！

如果你在记录分数，想要清空计分榜重新计分的话，使用指令`/resetCounter`就可以重置积分到0。

[\[回到目录\]](#目录-table-of-contents)

### 机器人单挑房-Bot 1v1 Room

机器人单挑房。和机器人房的所有指令相同。

[\[回到目录\]](#目录-table-of-contents)

### 挖掘房-Cheese Room

发送垃圾行，是多人游戏中KO对手的主要方式。而挖掘垃圾行进行防御就成为了一个重要的能力。**挖掘房-Cheese Room**，也称作~~瑞士~~奶酪房间 ~~出自C2~~ ，就是练习挖掘能力的好去处。在这个房间里，你不需要发送垃圾行打向对手，只需要用最快速度完成对现有垃圾行的10行挖掘以获胜。

10行太简单了？使用`/set height [lines]`来更换起始行数（1~20）！

[\[回到目录\]](#目录-table-of-contents)

### 慢速房-Slow Room

不能和比你厉害的朋友一起愉快对战？被大触横行的默认房Bot Room虐惨了？或者你想弱化速度影响，以注重效率？这些情况在**慢速房-Slow Room**都可以解决！限速房默认设置速度为 2.0块/秒，即速度不能超过 2.0块/秒，否则就会屏幕暂时锁定。慢速房还有 700ms 的消行延迟来进一步限速。即消行后你需要等待 700ms 才能继续下一块操作。
所有的慢速房都会有一个小小的速度表标志[SPEEDOMETER_ICON]。自定义慢速房可以设定从0~20块/秒.

![the lobby, where you can join and create rooms][image5]

[\[回到目录\]](#目录-table-of-contents)

### 地图房-Map Room

**地图房-Map Room** 是从玩家制作的地图中随机抽出房间的挖掘模式。其中地图名后面的(D=?%)代表着这张地图的难度（Difficulty）百分比，0%为最简单而100%为最难。~~有全消要求的地图不会出现。~~
全消要求 / 固定序列的地图会在固定序列之后以包随机生成块。（待确认）

[\[回到目录\]](#目录-table-of-contents)

### 组队房-Team Room

最后的默认房是 **组队房-Team Room**。组队房中会预设蓝和红两个队伍，你的垃圾行不会打向队友，你也不必担心收到来自队友的垃圾行。选择蓝方或红方，然后为你的队伍赢得荣誉吧！~~打群架~~

![team game in progress][image11]

[\[回到目录\]](#目录-table-of-contents)
- - -

## 单人游戏-Singleplayer

### 竞速模式-Sprint

基础而又最简单的**竞速模式-Sprint**是Jstris最受欢迎的单人模式，以最快的速度消除指定行数完成游戏！Jstris支持20行、40行（默认）、100行和1000行的Sprint模式。

[\[回到目录\]](#目录-table-of-contents)

### 挖掘竞速-Cheese Race

**挖掘竞速-Cheese Race**和挖掘房相仿，以最快的速度消除所有垃圾行以完成游戏。相比单纯的竞速，挖掘竞速更需要思考和计算，要求你在挖掘垃圾行的过程中寻找最有效的方式。Jstris支持10行、18行、100行和无限行的Cheese Race模式。

[\[回到目录\]](#目录-table-of-contents)

### 限时极限-Ultra

**限时极限-Ultra**需要你在2分钟内取得尽可能高的分数！注重使用高级技巧，如T-spin、Back to back等可以获得更多的奖励分数。Ultra模式是提升你的高超技巧的熟练度的好去处。

[\[回到目录\]](#目录-table-of-contents)

### 生存模式-Survival

**生存模式-Survival**可能是单人游戏中最具有挑战性的模式。垃圾行将从游戏盘底部以1行/秒的固定速度上涨，你需要不断挖掘以保持存活！面对不断涨起的垃圾行在Survival模式中尽可能生存更久吧！~~苟住啊~~

[\[回到目录\]](#目录-table-of-contents)

### 地图-Maps

在2018下半年，Jstris引入了**地图-Maps**模式。地图带来了创造性元素，并且同时让玩家在不同的情形下，或是非常情形下的挖掘更加效率化。在 *地图设计器-Map Designer* 中创建你自己的地图。一旦公开发布 (publish) 你的地图后，世界上的任何人都可以玩你的地图，并且互相竞争完成地图的最快时间。地图每日发表限制5幅、待发表队列限制10幅。每个地图都有排行榜，并且还有金、银、铜三个奖章分别对应第一、第二、第三名。在任何地图中获取前三名来赢得奖章并不断刷新自己的记录以保住你在排行榜上的位置吧！

*\*注意：地图排行榜每小时的半点处更新一次，所以新更改可能不会立即生效。*

[\[回到目录\]](#目录-table-of-contents)
- - -

## 系统设置-Configuration

在创建属于你的房间时，你可以自定义在你的房间内游戏的规则！现在让我们了解每个选项。
使用指令`/config`在Jstris的任何房间查看预设的或房主进行的设置。

### 攻击连击表-Attack and Combo table

在Jstris中，默认的攻击和连击表如下:

| 攻击方式            |   送行数   |   |  连击数 |   送行数   |
| :----------------- | ---------: | - | ------: | ---------: |
| 放置方块            |      **0** |   |       0 |      **0** |
| 消除 1 行(single)   |      **0** |   |       1 |      **0** |
| 消除 2 行(double)   |      **1** |   |       2 |      **1** |
| 消除 3 行(triple)   |      **2** |   |       3 |      **1** |
| 消除 4 行           |      **4** |   |       4 |      **1** |
| T-spin Double (2)  |      **4** |   |       5 |      **2** |
| T-spin Triple (3)  |      **6** |   |       6 |      **2** |
| T-spin Single (1)  |      **2** |   |       7 |      **3** |
| T-spin Mini Single |      **0** |   |       8 |      **3** |
| 全清-Perfect Clear |     **10** |   |       9 |      **4** |
| Back-to-Back       |     **+1** |   |      10 |      **4** |
|                    |            |   |      11 |      **4** |
|                    |            |   |     12+ |      **5** |

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行分配方式-Garbage Distribution

在多人游戏中，垃圾行分配的方式共有8种。它们分别是：（后为使用指令）

- 目标指定-Targets `/set garbage targets`
- 平均分配-Divide `/set garbage divide`
- 全部送出-To all `/set garbage toAll`
- 接受最少-To least(Rec) `/set garbage toLeast`
- 发送最多-To most(Snt) `/set garbage toMost`
- 自攻自受-To self `/set garbage toSelf`
- 完全随机-Random `/set garbage random`
- 左轮转盘-Roulette `/set garbage roulette`

**目标指定-Targets**为默认设置，也应用最广。同TOP、TF的多人模式的准星一样，目标框在房间内每个人循环指向，时间均等（或有修正）。当你打出垃圾行时，你的垃圾行会打向目标框所指的玩家！

在**平均分配-Divide**中，你送出的任何垃圾行都会均等的分给每个玩家。比如对手有2人，你送出了一个T-spin Double（4行），每个对手都会得到2行垃圾行。

在**全部送出-To All**中，如同PPT的对战模式，你发送的垃圾行会全部送给每个对手，比如对手有4人，你发送了全清-Perfect Clear（10行），每个人都会收到10行攻击。由示例可以推测，开启To All选项的时候垃圾行的周转数目会比Divide更多更快，游戏时间也会更短。

在**接受最少-To least(Rec)**当中，垃圾行会送给当前 **接受(Received)** 总垃圾行**最少**的人。比如对手有3人，你发送了4行垃圾行。在你发送攻击的时候，对手A在该局游戏中已总计接受60行垃圾行，对手B接受53，对手C接受58。因为对手B当前总计接受行数最少，你发送的4行垃圾行会送给对手B。

在**发送最多-To Most(Snt)**当中，垃圾行会送给当前 **发送(Sent)** 总垃圾行**最多**的人。本质上你在攻击这个房间内最强的玩家。

在**自攻自受-To Self**当中，垃圾行会送给自己。虽然在多人当中不合理，但是单人练习时会很有用。

在**完全随机-Random**当中，垃圾行会随机送给随机对手。可以说是最公平的垃圾行分配系统。

在**左轮转盘-Roulette**当中，垃圾行会随机送给随机对手，***包括你自己***。~~论俄罗斯方块与俄罗斯轮盘~~

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行抵消-Garbage Blocking

~~Block v.阻挡，不过一般都称呼攻击抵消~~

在Jstris当中有4种垃圾行抵消系统，它们分别是：

- 完整抵消-Full
- 限制抵消-Limited
- 无抵消-None
- 即时送入-Instant

**完整抵消-Full**是Jstris中默认的抵消系统。其他平台使用完整抵消的有：*TF* (E+房) 、*TOP*和*PPT(Swap)* 。收到垃圾行后，你可以一直消行来抵消攻击，直到你放置一个方块而没有消行时，才会涨起右侧红条（预告条）高度的垃圾行。即：连击可以暂停涨垃圾行。

**限制抵消-Limited**和完整抵消的区别在于，收到垃圾行后，你只能用当前块去进行唯一一次的抵消垃圾行，放置当前方块后无论是否消行，都会涨垃圾行。垃圾行不会被你的连击所暂停。使用限制抵消的平台有：*PPT (VS)*、*TB*和*TF*(非E+房)。

**无抵消-None**模式下，垃圾行不能被抵消。收到垃圾行时，右侧红条仍然会提示，放置当前方块后无论是否消行都会涨红条高度的垃圾行，且不会抵消。比如对手送给你10行，即使你下一块做出了消4，垃圾行也不会减少到6。相反，你还是会涨10行垃圾行，但与此同时消4产生的四行垃圾行会向对手完整地打出去。

**即时送入-Instant**模式下，没有右侧红色预告条。垃圾行会在你接受到攻击的那一刻立刻涨起。没有抵消。

| 抵消系统         | 红色预告条 | 能否抵消？| 连击暂停涨行 |
| ---------------- | :--------: | :-------: | :----------: |
| 完整抵消-Full    |      √     |     √     |       √      |
| 限制抵消-Limited |      √     |     √     |       ×      |
| 无抵消-None      |      √     |     ×     |       ×      |
| 即时送入-Instant |      ×     |     ×     |       ×      |

[\[回到目录\]](#目录-table-of-contents)

### 序列生成器-Randomizer

序列的随机数生成器决定着你获得的方块序列。Jstris拥有4种序列生成器，它们分别是：

- 7块包-7-bag
- 14块包-14-bag
- 经典-Classic
- 单类块-One Block

**7块包-7-bag**是基本默认的序列。7种方块每种方块各一个打包在一起，包内随机排序，一个包一个包按顺序出现。相当于每7块都会固定出现7种方块各一次。~~妈妈再也不用担心我等不到棍子啦~~

**14块包-14-bag**和7块包类似，不过一包有14个方块，7种方块每种方块各两个。

**经典-Classic**为纯随机序列，出块没有任何规律，非常考察堆叠与序列处理能力。

**单类块-One Block**是最奇怪的序列。开局随机抽一种方块，然后在整个游戏当中都会只出现这一种方块。

[\[回到目录\]](#目录-table-of-contents)

### 预览数-Previews

Jstris默认有5个预览块。在自定义房间可以设置预览块的数量为0-5个。

[\[回到目录\]](#目录-table-of-contents)

### 实心垃圾行-Solid Garbage

实心（固定）垃圾行是“hurry up”阶段中底部涨起的不能消除的垃圾行。用以加快游戏进程，防止由于拉锯战导致游戏时间过长。

实心行会比普通垃圾行更暗些。在Bot Room中，实心行会在游戏开始2分钟后开始上涨。实心行出现时间在自定义房间也可以进行设置。

![Solid Garbage][image7]

[\[回到目录\]](#目录-table-of-contents)

### 消行延迟-Clear Delay

消行延迟即消行时不能做任何动作的时间。每进行一次消行，都会进入消行延迟，等到消行延迟结束后才进入下一个方块的操作。

很多旧方块和PPT等都拥有消行延迟，Jstris默认关闭，而且一般也不使用。需要时可以自定义为0-6000毫秒。

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行生效延迟-Garbage Delay

垃圾行生效延迟是指接受垃圾行时，红条出现到垃圾行可以进入场地的时间。默认设置为500ms，可以自定义为0~1000ms。生效延迟越长，在垃圾行生效前可摆放的块就越多，玩家就可以更加有效率的进行阻挡和抵消。

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行混乱度-Messiness

垃圾行混乱度指涨起垃圾行时垃圾行缺口的混乱程度。使用`/set messiness [-100~100]`指令可以改变房间内的垃圾行混乱度。-100是最整齐的，只在一列生成缺口（如左图）；100是最混乱的，每一列都一定会错位（如右图），使得挖掘难度非常大。

![Unmessy (-100)][image10] 
![Messy (100)][image1]

[\[回到目录\]](#目录-table-of-contents)

### 配置预设-Configuration presets

如果有您特别喜欢的房间设置配置，并且希望方便的回溯，则可以将设置另存为预设。

点击 *大厅-Lobby*，然后 *创建房间-Create Room*，然后选择 *简洁-Simple* 或 *全部-All* 选项，当你把设置自定义为你喜欢的情况后，点击最下方右侧的 *保存-Save* 按钮然后生成属于你的预设数据。复制，然后将内容粘贴到
[提交预设](/presets/submit)页面的 *预设数据-Preset data* 的文本框当中。 

当你提交预设后，你可以在[预设列表-List of presets](/presets)查看包括其他用户提交的预设。现在你可以轻松的建立同样规则的房间，而不用每个选项都再次改一遍。只需要 *创建房间-Create Room* ，然后 *使用自定义预设-Use Custom Preset* ，然后输入你的 预设标题 或 ID 就可以了。

[\[回到目录\]](#目录-table-of-contents)

### 模式-Mode

新建房间时，目前可以选择7种不同模式。分别是：

- 基本模式-Standard
- 组队模式-Team
- 挖掘模式-Cheese
- 在线竞速-Live Sprint
- 在线挖掘-Live Cheese
- 在线生存-Live Survival
- 在线地图-Live Maps v0.1

**基本模式-Standard**为普通的自由多人模式。

**组队模式-Team**创建一个自定义的组队房间。使用`/set teamName [队伍名]`命令可以更换你的队伍名。

**挖掘模式-Cheese**创建一个自定义挖掘房间。发送垃圾行，是多人游戏中KO对手的主要方式。而挖掘垃圾行进行防御就成为了一个重要的能力。**挖掘模式-Cheese**，也称作~~瑞士~~奶酪模式 ~~出自C2~~ ，就是练习挖掘能力的好去处。在这个房间里，你不需要发送垃圾行打向对手，只需要用最快速度完成对现有垃圾行的10行挖掘以获胜。10行太简单了？使用`/set height [lines]`来更换起始行数（1~20）！

**在线竞速-Live Sprint**模式可以让你和对手一起玩竞速模式。最先完成的人获胜。房间默认为40行竞速，可以使用以下指令更换竞速模式类型：

- 20L:     `/set gamemode sprint20`
- 40L:     `/set gamemode sprint40`
- 100L:    `/set gamemode sprint100`
- 1000L:   `/set gamemode sprint1000`

如果你在此模式当中打破你的记录，可惜的是记录并不能更新到你的个人账号。因为在线竞速被认为是线上回放，而非单人回放。但你仍然可以把录像保存到你的收藏（Favorites）。

~~自杀死亡后开40行练习的成绩会记录，因为此时是单人状态~~

**在线挖掘-Live Cheese**可以让你和对手一起进行挖掘模式。除了你只能设定目标在10行、18行和100行。在线挖掘模式和挖掘模式几乎相同。房间默认为10行挖掘，可以使用以下指令更换其他类型：

- 10L:     `/set gamemode cheese10`
- 18L:     `/set gamemode cheese18`
- 100L:    `/set gamemode cheese100`

**在线生存-Live Survival**可以让你和对手一起玩生存模式。活得最久的玩家获胜。

**在线地图-Live Maps v0.1**模式可以建立一个自定义的地图房。同地图挖掘房。

[\[回到目录\]](#目录-table-of-contents)

- - -

## 常见问题解答 FAQ

### Q: 我能在私房或者自定义房间使用bot吗？

A：
暂时不能。Jstris当前只有一个永远在Bot room内的Bot。不过私房bot在将来可以成为现实。~~还没弄，开发中，咕咕咕~~

~~茶管：自己写的机器人应该可以用，但请提前说好/做好标识，以免造成不必要的麻烦~~

[\[回到目录\]](#目录-table-of-contents)

### Q: 游戏结果当中的各种英文……都是啥?

A：
- T-spin：T型回旋、T转。T块的最后操作为旋转、且T块的4个角落被场地已有方块占领3个时（3角判定），此旋转称作T-spin。
- B2B：Back to Back，背靠背/大满贯。消4和T-spin消行后，下次消行再次消4/T-spin即为Back to Back。进行一次普通的消1~3会中断Back to Back。在Jstris的多人模式中一般会使本次攻击＋1，单人限时极限（Ultra）中可增加本次消行得到的分数。
- B2Bpm：Back to Back per minute。每分钟进行的B2B次数。B2B/分。
- APM：Attack per minute，每分钟攻击行数（送行数+抵消行数）。
（ActionPM/每分钟操作数用Key Per Minute/每分钟按键数表示）
- SPM：Sent per minute， 每分钟送出行数。不含抵消。
- PPS：Pieces per second，每分钟摆块数。块/秒。
- Rep：Replay，回放录像。



![game results table][image9]

[\[回到目录\]](#目录-table-of-contents)

### Q: 加速（器）怎么弄？自动加速延迟(DAS)？自动重复间隔(ARR)？

A：
先设想你在文本框按住键盘一个字母输入（比如a），刚刚按下时会只出现一个a，在**一小段时间**(DAS)后才会以**极短的时间间隔**(ARR)连续输出a。
时间轴大致是这样的感觉：

|----------DAS----------|ARR|ARR|ARR|ARR|ARR|ARR|ARR|ARR|ARR|...|
|-----------------------|---|---|---|---|---|---|---|---|---|---|
|a----------------------|a--|a--|a--|a--|a--|a--|a--|a--|a--|...|

当然，键盘的自动重复速度实在是太慢，所以我们在游戏中把这两个时间变为可调的参数。

DAS，全称Delay Auto Shift。即自动加速延迟。是在方块持续移动前你需要按下的时间长度。DAS调得非常低时，即使是轻轻按一下也会使得方块飞走。DAS调非常高时，你需要按下很长的时间才会使得方块连续移动。一般专业玩家会尽可能使用低DAS以提速。Jstris的默认设置为133毫秒，如果你仍然感觉移动过于敏感，可以尝试增加DAS数值，如果你感觉移动很慢，可以降低数值。调整并找到你最适合的DAS吧！

ARR，全称Auto Repeat Rate，即自动重复比率。**但Jstris当中**这个数值是指**自动重复间隔长短**。如果这个数值调低，则会移动非常快，如果这个数值调高，自动重复的移动会非常的慢，过大甚至慢于连点移动键。Jstris的默认ARR值为10。

将ARR调为0（即会在DAS时间结束后，方块几乎立即移动到墙）并配合下方所提到的的操作最优化可以明显提升速度。

[\[回到目录\]](#目录-table-of-contents)

### Q: 操作最优化？多余操作？finesse？

A：
在目前的10列方块游戏当中，最佳的移动方式可以使得**不超过两次移动**和**不超过两次旋转**就可以把方块硬降到任何可以硬降的位置。由于Jstris支持180°转，所以只需要**两次移动、一次旋转**。但finesse数值指操作缺欠数（finesse fault），即指不必要的**多余操作**数。**减少多余操作数对提升速度和效率非常非常重要**。

finesse数值不表示没能完成最简操作的摆块数量！如果在摆下一个块的过程中有多个多余操作，finesse数值也会涨起不止1点！

0 finesse代表无多余操作，按键效率最高。需要特别学习和使用。网络上有很多关于操作最优化相关的教程，墙内可以参考这个：[【代投】TH Hua方块教学视频：两步式操控法](https://www.bilibili.com/video/av14230002/?p=4).

[\[回到目录\]](#目录-table-of-contents)

### Q: 我能建立私房 (private room) 吗？

A：
可以！点击*大厅-Lobby*，然后点击*创建房间-Create Room*，查看*私人-Private*板块，复制并分享房间链接给你想邀请进来的小伙伴。

小提示：使用指令`/link`可以获取任何房间的地址，无论是公共房间还是私人。

[\[回到目录\]](#目录-table-of-contents)

### Q: 我可以离线玩Jstris吗？

A：
可以！进入单人模式，然后右键“页面另存为”（或Ctrl+S）为HTML。注意：离线只能玩单人模式，并且不会保存分数。

[\[回到目录\]](#目录-table-of-contents)
- - -

## 附加信息-Additional Information

Jstris的运营完全建立与各位的捐献和打赏之上，没有广告也不会有广告。由于存储了大量的录像回放和游戏数据，因此需要强大的服务器来运行Jstris。感谢你们所有的捐赠和打赏，这些资金都会用于Jstris的服务器的运行——更多详情请参阅[关于](/about)。

[\[回到目录\]](#目录-table-of-contents)

[image2]: ./images/guide-intro.png "introduction"
[image4]: ./images/image4.png "MisaMino bot in opponents view"
[image8]: ./images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ./images/image5.png "the lobby, where you can join and create rooms"
[image11]: ./images/image11.png "team game in progress"
[image7]: ./images/image7.png "Solid Garbage"
[image10]: ./images/image10.png "Unmessy (-100)"
[image1]: ./images/image1.png "Messy (100)"
[image9]: ./images/image9.png "game results table"
