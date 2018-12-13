# Jstris 导航-游戏指南-Jstris Guide

欢迎来到Jstris，一个简单的在线多人方块游戏。Jstris向来以低延迟的游戏著称，并且吸引着世界上的各路神仙玩家前来。该导航将向你介绍本游戏的基本事项。

## 写在最前：
这篇文章不会完全翻译自Eddie的英文Guide，会以尽量适合中文玩家的说法以及信息进行说明。（意译和重写）

为了让各位和玩家进行英语交流间减少障碍，保留了部分常用英语。

~~目前版本是茶管子在考研前几天闹心复习不下去的时候瞎写的~~

~~有问题[请进群里](https://jq.qq.com/?_wv=1027&k=58mxfPJ)告诉我以后会改的~~

- - -


## **目录-Table of Contents**

- [总览-Overview](#总览-overview)
- [多人游戏-Multiplayer](#多人游戏-multiplayer)
  - [机器人房-Bot Room](#机器人房-bot-room)
  - [单挑房-1v1 Room](#单挑房-1v1-room)
  - [挖掘房-Cheese Room](#挖掘房-cheese-room)
  - [限速房-Speed Limit Room](#限速房-speed-limit-room)
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
- [常见问题解答 FAQ-Frequently Asked Questions](#常见问题解答-faq)
  - [Q: 游戏结果当中的各种英文……都是啥？](#q-游戏结果当中的各种英文都是啥)
  - [Q: 加速（器）怎么弄?自动加速延迟 (DAS) ?自动重复间隔 (ARR) ?](#q-加速器怎么弄自动加速延迟das自动重复间隔arr)
  - [Q: 操作最优化？多余操作？finesse？](#q-操作最优化多余操作finesse)
  - [Q: 我能建立私房(private room)吗？](#q-我能建立私房-private-room-吗)
  - [Q: 我可以离线玩Jstris吗？](#q-我可以离线玩jstris吗)
- [附加信息-Additional Information](#附加信息-additional-information)

- - -

## 总览-Overview

和其他方块一样，Jstris使用世界基准（Guideline）规则。值得一提的是Jstris的录像回放（Replay）系统。每次游戏后都会自动生成游戏录像。回放、分析并自我提升，在Jstris的Replay里都非常简单。

不同于其他网站，Jstris的排行榜真实可靠，拒绝被黑。排行榜由管理员（Moderators）时常查看并移除可疑的记录，来确保真实可信全球成就表。（发现可疑记录也可以联系管理员检查哦~）

虽然点开即玩，无需注册，但仍然推荐在jstris上创建账号。点一下右上的注册，顺次写下 用户名、邮箱、两遍密码就可以了，很快的~ 在拥有账号后，你可以查看大量的数据，包括你的单人模式下的最佳时间、多人数据、进步数据、回放、等等。你还能在排行榜上看到你自己（未注册用户的分数也包含在内）。

![introduction][image2]

[\[回到目录\]](#目录-table-of-contents)
- - -

## 多人游戏-Multiplayer

### 机器人房-Bot Room

在进入网站后，所有玩家都会立即进入默认的**Bot Room**，即机器人房间。这样称呼是因为1个Bot（机器人）永远在线。位置也永远在你所有对手的左上角，还有着红色方块，在人群当中特别显眼易区分~

![MisaMino bot in opponents view][image4]

下面是在Jstris里按强度顺序列出的4个不同的Bot。在聊天框内输入对应指令更改Bot类型。

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (于2018.09.21删除)
- ~~Fool bot: `/changeBot fool`~~ (于2018.09.21删除)

*\*注意：只能在两场游戏间输入指令，在游戏进行中输入指令会被忽略。*

Misamino是目前已知的最强bot之一 ~~zzz尚未嵌入到js当中，等一个奏大爷适配~~ ，当bot使用5PPS（块/秒）的速度时，可以在单挑房内轻松暴打最强人类选手。然而bot在多人房间时表现并不佳，经常很快就会死掉。

所以你可以使用`/bot [PPS] `的命令来控制bot的摆块速度。[PPS]的取值区间为 0.3~5。
如`/bot 2 `即将bot的摆块速度改为2块/秒，`/bot 1.73 `改为1.73块/秒等。

 
在默认房Bot Room里面可能会吃瘪！Jstris的一大特点就是可以让新手和世界大触混合在一起，互相进行大混战。如果你玩累了只想观战，可以使用指令`/spectate` 或 `/spec` 进行旁观。想再次加入游戏时，使用指令`/play`。

[\[回到目录\]](#目录-table-of-contents)

### 单挑房-1v1 Room

当然房间不止有Bot Room一个，点击游戏区域底部左侧的 *大厅-Lobby* 按钮查看完整房间列表。Jstris中第二受欢迎的通常就是**单挑房-1v1 Room**了。这个房间最大只能 2 人同时游玩，不过其他人可以进房旁观。用1v1 Room来和你的朋友，或者旗鼓相当的对手一决高下吧！
如果你在记录分数，想重新计分的话，使用指令`/resetCounter`就可以分数清零。

[\[回到目录\]](#目录-table-of-contents)

### 挖掘房-Cheese Room

发送垃圾行，是多人游戏中KO对手的主要方式。而挖掘垃圾行就成为了一个重要的能力。定行挖掘模式，也称作~~瑞士~~奶酪模式 ~~出自C2~~ ，是练习挖掘能力的好去处。最快速度完成10行挖掘以获胜。10行太简单了？使用`/set height [lines]`来更换起始行数（1~20）。

[\[回到目录\]](#目录-table-of-contents)

### 限速房-Speed Limit Room

不能和比你厉害的朋友一起愉快对战？被大触横行的默认房Bot Room虐惨了？这就轮到了限速房的出场了！限速房默认设置速度为 1.5块/秒，超速的话会使得屏幕暂时锁定。
任何限速房都有一个限速标志![SPEEDOMETER_ICON][image8]。自定义房间可以设定0.1~20块/秒PPS（0为不限速）。

![the lobby, where you can join and create rooms][image5]

[\[回到目录\]](#目录-table-of-contents)

### 组队房-Team Room

最后的默认房是 **组队房-Team Room**，选择蓝方或红方，然后为你的队伍赢得荣誉吧！~~打群架~~

![team game in progress][image11]

[\[回到目录\]](#目录-table-of-contents)
- - -

## 单人游戏-Singleplayer

### 竞速模式-Sprint

基础而又最简单的**竞速模式-Sprint**是Jstris最受欢迎的单人模式，以最快的速度消除指定行数。Jstris支持20行、40行（默认）、100行和1000行模式。

[\[回到目录\]](#目录-table-of-contents)

### 挖掘竞速-Cheese Race

**挖掘竞速-Cheese Race**相比单纯的竞速更需要思考和计算，要求你在挖掘过程中寻找最有效的方式。Jstris支持10行、18行、100行和无限行挖掘模式。

[\[回到目录\]](#目录-table-of-contents)

### 限时极限-Ultra

**限时极限-Ultra**注重使用高级技巧如T-spin和Back to back等及其奖励分数，是提升你在多人游戏中高超技巧的使用的好方法。

[\[回到目录\]](#目录-table-of-contents)

### 生存模式-Survival

**生存模式-Survival**可能是单人游戏中最具有挑战性的模式，类似于以1行/秒的固定速度涨垃圾行的挖掘模式。面对不断涨起的行尽可能生存更久吧！

[\[回到目录\]](#目录-table-of-contents)

### 地图-Maps

近日，Jstris引入了**地图-Maps**模式。地图模式带入了创造元素，同时也让玩家准备好在困难与不寻常的位置进行高效挖掘。在 *地图设计器-Map Designer* 创建你自己的地图。一旦公开发布 (publish) 地图后，世界上的任何人都可以玩你的地图，并且互相竞争最快时间。地图每日发表限制5幅、待发表队列限制10幅。每个地图都有排行榜，并且还有金、银、铜三个奖章分别对应第一、第二、第三名。在任何地图中获取前三名来赢得奖章并保住你在排行榜的位置吧！

*\*注意：地图排行榜每小时的xx:30更新一次，所以新更改可能不会立即生效。*

[\[回到目录\]](#目录-table-of-contents)
- - -

## 系统设置-Configuration

使用指令`/config`在Jstris的任何房间查看设置。现在让我们了解每个选项。

### 攻击连击表-Attack and Combo table

在Jstris中，默认的攻击和连击表如下（可在自定义房间中更改）:

| 攻击方式            |   送行数   |   |  连击数 |   送行数   |
| :----------------- | ---------: | - | ------: | ---------: |
| 0 行               |      **0** |   |       0 |      **0** |
| 1 行    (single)   |      **0** |   |       1 |      **0** |
| 2 行    (double)   |      **1** |   |       2 |      **1** |
| 3 行    (triple)   |      **2** |   |       3 |      **1** |
| 4 行               |      **4** |   |       4 |      **1** |
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

在多人游戏中，有4种垃圾行分配的方式如下：（后为使用指令）

- 目标指定-Targets `/set garbage targets`
- 平均分配-Divide `/set garbage divide`
- 全部送出-To all `/set garbage toAll`
- 送给最少-To least `/set garbage toLeast`

**目标指定-Targets**为默认设置，也应用最广。同TOP、TF的多人模式的准星一样，目标框在房间内每个人循环指向，在均等而恰当的时机，无论目标框指向谁都会让你的垃圾行向那里送出。

在**平均分配-Divide**中，你送出的任何垃圾行都会均等的分给每个玩家。比如对手有2人，你送出了一个T-spin Double（4行），每个对手都会得到2行。

在**全部送出-To All**中，如同PPT的对战模式，你发送的垃圾行会全部送给每个对手，比如对手有4人，你发送了PC（全清）（10行），每个人都会收到10行攻击。由示例可以推测，开启To All选项的时候垃圾行的周转数目会比Divide更多更快，游戏也会更短。

在**送给最少-To least**当中，垃圾行会送给当前接受总垃圾行最少的人。比如对手有3人，你发送了4行。在你发送攻击的时候，对手A总计接受50行，对手B接受53，对手C接受58。因为对手A当前总计接受行数最少，你消除的4行会送给他。

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行抵消-Garbage Blocking

~~Block v.阻挡，不过一般都称呼攻击抵消~~

在Jstris当中有4种垃圾行抵消系统如下：

- 完整抵消-Full
- 限制抵消-Limited
- 无抵消-None
- 即时送入-Instant

**完整抵消-Full**是Jstris中默认的抵消系统。其他平台使用完整抵消的有：*TF* (E+房) 和*TOP*、*PPT(Swap)*。你可以一直消行抵消攻击，直到你摆放一块没有消行时，才会涨右侧红条（预告条）高度的垃圾行。即：连击可以暂停涨垃圾行。

**限制抵消-Limited**和完整抵消的区别在于，你只能用当前块的攻击力去抵消一次红条，放置方块后无论是否消行，都会涨垃圾行。垃圾行不会被你的连击所暂停。使用限制抵消的平台有：*PPT (VS)*、*TB*和*TF*(非E+房)。

**无抵消-None**模式下，垃圾行不能被抵消。收到垃圾行时，右侧红条仍然会提示，放置块后会涨红条高度的垃圾行，且不能抵消。比如对手送给你10行，即使你下一块消4，垃圾行不会减少到6。相反，你还是会涨10行垃圾行，与此同时你会向对手送出4行。

**即时送入-Instant**模式下，没有右侧红色预告条。垃圾行会在你接受到攻击的那一刻立刻涨起。没有抵消。

| 抵消系统         | 红色预告条 | 能否抵消？| 连击暂停涨行 |
| ---------------- | :--------: | :-------: | :----------: |
| 完整抵消-Full    |      √     |     √     |       √      |
| 限制抵消-Limited |      √     |     √     |       ×      |
| 无抵消-None      |      √     |     ×     |       ×      |
| 即时送入-Instant |      ×     |     ×     |       ×      |

[\[回到目录\]](#目录-table-of-contents)

### 序列生成器-Randomizer

序列的随机数生成器决定着你获得的方块序列。Jstris拥有4种序列生成如下：

- 7块包-7-bag
- 14块包-14-bag
- 经典-Classic
- 单类块-One Block

**7块包-7-bag**是基本默认的序列。顾名思义，一包7块，每种方块各一个。包内随机排序
，但每7块都会固定出现7种各一次。~~妈妈再也不用担心我等不到棍子啦~~

**14块包-14-bag**和7块包类似，不过一包14块，每种方块各两个，包内随机排序，每14块都会固定出现7种方块各两次。

**经典-Classic**为纯随机序列，非常考察堆叠与序列处理能力。

**单类块-One Block**是最奇怪的序列。开局随机抽一种方块，然后在整个游戏当中都会只出现这一种方块。

[\[回到目录\]](#目录-table-of-contents)

### 预览数-Previews

Jstris默认有5个预览块。在自定义房间可以调整预览数从0到5。

[\[回到目录\]](#目录-table-of-contents)

### 实心垃圾行-Solid Garbage

实心（固定）垃圾行是“hurry up”阶段中底部涨起的不能消除的行，以防止游戏时间过长，加快游戏进度。实心行会比普通垃圾行更暗些。在默认的Bot Room中，实心行会在2分钟后开始上涨。实心行在自定义房间也可以自定义设置。

![Solid Garbage][image7]

[\[回到目录\]](#目录-table-of-contents)

### 消行延迟-Clear Delay

消行延迟即消行时不能做任何动作的时间。很多旧方块、PPT拥有消行延迟，Jstris默认关闭，而且一般也不使用。需要时可以自定义为0-6000毫秒。

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行生效延迟-Garbage Delay

垃圾行生效延迟是指接受垃圾行时，红条出现到垃圾行生效时间。默认设置为500ms。可以自定义为0~1000ms。生效延迟越长，在垃圾行生效前可摆放的块就越多，对手就可以更加有效率的进行阻挡和抵消。

[\[回到目录\]](#目录-table-of-contents)

### 垃圾行混乱度-Messiness

垃圾行混乱度指消除某些类型垃圾行的难度。使用`/set messiness [-100~100]`指令可以改变房间内的垃圾行混乱度。-100是最整齐的，只在一列生成空隙（如左图）；100是最混乱的，每一列都一定会错位（如右图），使得挖掘难度非常大。

![Unmessy (-100)][image10] 
![Messy (100)][image1]

[\[回到目录\]](#目录-table-of-contents)
- - -

## 常见问题解答 FAQ

### Q: 游戏结果当中的各种英文……都是啥?

A：
- T-spin：T型回旋、T转。T块的最后操作为旋转、T块的4角占有3个时（3角判定），此旋转称作T-spin。
- B2B：Back to Back，背靠背/大满贯。消4和T-spin消行后，再次消4/T-spin时即为Back to Back。在Jstris的多人模式中一般攻击＋1，单人限时极限（Ultra）中可增加分数。
- B2Bpm：Back to Back per minute。每分钟B2B次数。B2B/分。
- APM：Attack per minute，每分钟攻击行数（送行数+抵消行数）。
（ActionPM/每分钟操作数用Key Per Minute/每分钟按键数表示）
- SPM：Sent per minute， 每分钟送行数。不含抵消。
- PPS：Pieces per second，每分钟摆块数。块/秒。
- Rep：Replay，回放录像。



![game results table][image9]

[\[回到目录\]](#目录-table-of-contents)

### Q: 加速（器）怎么弄？自动加速延迟(DAS)？自动重复间隔(ARR)？

A：先设想你在文本框按住键盘一个字母输入（比如a），刚刚按下时会只出现一个a，在**一小段时间**(DAS)后才会以**极短的时间间隔**(ARR)连续输出a。
大致是这样的感觉：

|----------DAS----------|ARR|ARR|ARR|ARR|ARR|ARR|ARR|ARR|ARR|...|
|-----------------------|---|---|---|---|---|---|---|---|---|---|
|a----------------------|a--|a--|a--|a--|a--|a--|a--|a--|a--|...|

当然，键盘的自动重复速度实在是太慢，所以我们在游戏中把这两个时间变为可调的参数。

DAS，全称Delay Auto Shift。即自动加速延迟。是在方块持续移动前你需要按下的时间长度。DAS调非常低时，即使是轻轻按一下也会使得方块移动。DAS调非常高时，你需要按下很长的时间才会使得方块连续移动。一般专业玩家会尽可能使用低DAS以提速。Jstris的默认设置为133。如果你仍然感觉移动过于敏感，可以尝试增加DAS数字；如果你感觉移动很慢，可以降低数字。调整并找到你最适合的DAS吧。

ARR，全称Auto Repeat Rate，自动重复比率。但**Jstris当中**这个数值是指**自动重复间隔长短**。如果这个数值调低，则会移动非常快，如果这个数值调高，自动重复的移动会非常的慢，过大甚至慢于连点移动键。Jstris的默认ARR值为0，即会在DAS结束后几乎立即移动到墙。如果感觉不适应可以尝试增大数值到合适为止。

[\[回到目录\]](#目录-table-of-contents)

### Q: 操作最优化？多余操作？finesse？

A：在目前的10列方块游戏当中，最佳的移动方式可以使得**不超过两次移动**和**不超过两次旋转**就可以把方块硬降到任何可以硬降的位置。由于Jstris支持180°转所以甚至只需要**两次移动一次旋转**。finesse vt.巧妙处理 但finesse数值指操作缺欠数（finesse fault），即指不必要的**多余操作**数。**减少多余操作数对提升速度和效率非常非常重要**。0 finesse代表无多余操作。需要特别学习和使用。网络上有很多关于操作最优化相关的教程，可以参考这个：[Tutorial: How to Play Fast!](https://youtu.be/_QBs703nOnk?t=502).

[\[回到目录\]](#目录-table-of-contents)

### Q: 我能建立私房 (private room) 吗？

A：可以！点击*大厅-Lobby*，然后点击*创建房间-Create Room*，然后查看*私人-Private*板块，复制并分享房间链接给你想让他们加入的人。小提示：使用指令`/link`可以获取任何房间的地址，无论是公共房间还是私人。

[\[回到目录\]](#目录-table-of-contents)

### Q: 我可以离线玩Jstris吗？

A：可以。进入单人模式，然后右键“页面另存为”（或Ctrl+S）为HTML。注意：离线只能玩单人模式，并且不会保存分数。

[\[回到目录\]](#目录-table-of-contents)
- - -

## 附加信息-Additional Information

Jstris的运营完全建立与各位的捐献和打赏之上，没有广告也不会有广告。由于存储了大量的录像回放和游戏数据，因此需要强大的服务器来运行Jstris。感谢你们所有的捐赠和打赏，这些资金都会用于Jstris的服务器的运行————更多详情请参阅[关于](/about)。

[\[回到目录\]](#目录-table-of-contents)

[image2]: ../images/guide-intro.png "introduction"
[image4]: ../images/image4.png "MisaMino bot in opponents view"
[image8]: ../images/image8.png "speedometer icon for Speed Limit Rooms"
[image5]: ../images/image5.png "the lobby, where you can join and create rooms"
[image11]: ../images/image11.png "team game in progress"
[image7]: ../images/image7.png "Solid Garbage"
[image10]: ../images/image10.png "Unmessy (-100)"
[image1]: ../images/image1.png "Messy (100)"
[image9]: ../images/image9.png "game results table"
