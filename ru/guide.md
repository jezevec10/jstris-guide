# Руководство Jstris 

Добро пожаловать в Jstris, простую головоломку с онлайн мультиплеером. Jstris известен своей скоростью и привлекает к себе талантливых игроков со всего света. Данное руководство расскажет вам в общих чертах об этой игре.

- - -

**Содержание**

- [Обзор](#обзор)
- [Управление](#управление)
- [Против игроков](#против-игроков)
  - [Default Room](#default-room)
  - [Bot Room](#bot-room)
  - [1v1 Room](#1v1-room)
  - [Slow Room](#slow-room)
  - [Map Room](#map-room)
- [Одиночная игра](#одиночная-игра)
  - [Спринт](#спринт)
  - [Очистка](#очистка)
  - [Ультра](#ультра)
  - [Выживание](#выживание)
  - [Карты](#карты)
  - [20TSD](#20tsd)
- [Настройка](#настройка)
  - [Атака и Комбо](#атака-и-комбо)
  - [Распределение мусора](#распределение-мусора)
  - [Блокировка мусора](#блокировка-мусора)
  - [Блоки](#блоки)
  - [Рандомайзер](#рандомайзер)
  - [Длина очереди](#длина-очереди)
  - [Заполнения постоянным мусором](#заполнение-постоянным-мусором)
  - [Задержка перед фиксацией](#задержка-перед-фиксацией)
  - [Задержка очистки](#задержка-очистки)
  - [Гравитация](#гравитация)
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

## Обзор 

Jstris использует те же самые базовые механики, как и большинство похожих игр. Он использует правила оригинальной игры. Одной из основных особенностей является обширное использование реплеев. Для каждой законченной вами игры будет сгенерирован реплей. Просмотр и анализ своих игр является неотъемлемой частью самосовершенствования, и реплеи Jstris предоставляют вам такую возможность.

В отличии от других игр, вы можете быть уверены, что лидеры Jstris абсолютно чисты и не используют читы. Модераторы удаляют подозрительные записи, чтобы гарантировать заслуживающий доверия список глобальных достижений.

Возможно играть без регистрации, но для того, чтобы получить доступ ко всем возможностям сайта, рекомендуется создать аккаунт. Для этого, выберите пункт *Зарегистрироваться* в верхнем правом углу. Необходимы только email, имя пользователя и пароль. С аккаунтом, вы можете видеть множество статистики, вкючая вашие лучшие рекорды в одиночных режимах, статистику мультиплеера, статистику улучшения, реплеи и многое другое. Вы также можете видеть себя в списке глобальных достижений (анонимные достижения не показаны).

![Обзор][image2]
- - -

## Управление

Jstris позволяет игрокам настроить своё управление в любое время в меню **Настройки**, которое расположени под игровым полем. Управление по умолчанию представлено ниже:

|      Команда      | Клавиша по умолчанию |
| ----------------- | -------------------- |
| Налево            | left                 |
| Направо           | right                |
| Медленное падение | down                 |
| Быстрое падение   | space                |
| Поворот налево    | z                    |
| Поворот направо   | up                   |
| Переворот         | a                    |
| Замена            | c                    |

## Против игроков

### Default Room

При входе на сайт, все игроки изначально попадают в **Default room** - комнату со свободным доступом, где можно встретить игроков любого уровня.

Игра в комнате по умолчанию может быть тяжелой. Уникальной особенностью Jstris является то, что он смешивает скромных новичков с мировыми топ игроками, и всеми остальными. Если вы устали играть и хотите просто наблюдать, используйте команду  `/spectate` или `/spec`. Чтобы вернуться к игре, используйте `/play`.

### Bot Room

Default Room не единственная доступная комната. Чтобы увидеть весь список, нажмите кнопку *Лобби* под игровым полем. Следующей по популярности комнатой является комната с ботами **Bot Room**, названная так, потому что в ней всегда присутствует бот. Вы можете узнать его по красному цвету, он находится среди других оппонентов в левом верхнем углу.

![Бот MisaMino среди оппонентов][image4]

В Jstris 4 вида ботов. В списке ниже они отсортированы по силе, также представлены команды для смены бота.

- MisaMino: `/changeBot misamino`
- Real_Block: `/changeBot real`
- ~~jez_Block: `/changeBot jez`~~ (удалён 2018.09.21)
- ~~Fool bot: `/changeBot fool`~~ (удалён 2018.09.21)

*\*Любые команды должны быть введены между играми. Всякая команда, введённая во время игры, игнорируется.*

Misamino - самый сильный бот, возможно, сильнейший среди когда-либо созданных ботов. На его максимальной скорости 5 PPS (фигур в секунду), он становится грозным оппонентом, который может легко победить самых сильных живых игроков в режиме 1 на 1. Однако, производительности бота не хватает когда в комнате больше 5 живых игроков, и обычно он сразу же проигрывает. Для настройки бота можно использовать команду /botPPS.

Скорость бота может быть изменена. Для этого, введите `/bot ?` , где замените знак вопроса на любое число между .3 и 5. Для примера, если я хочу чтобы бот играл на 2 PPS, я напечатаю `/bot 2`. Если я хочу, чтобы бот играл на 1.73 PPS, я напечатаю `/bot 1.73`.

### 1v1 Room

Комната **1v1 Room** позволяет играть только двоим игрокам, хотя кто угодно может войти и смотреть матч, даже если комната заполнена. Используйте эту комнату для игры с друзьями или с достойным оппонентом. Для того, чтобы сбросить счёт побед, используйте команду `/resetCounter` и все победы будут обнулены.

### Slow Room

Хотите сыграть с другом, но один из вас играет значительно лучше другого? Или вы просто новичок и устали мгновенно проигрывать в комнатах с про-игроками? Или вы хотите улучшить эффективность своей игры, убрав скорость из общего зачёта? В Jstris есть Slow Toom (медленная комната) для всех этих случаев. По умолчанию скорость медленной комнаты ограничена 2.0 PPS, что означает игроки не могут превысить этот порог. Если человек играет быстрее, его экран будет временно заблокирован. В дополнение к ограничению скороcти, медленная комната имеет задержку 500 мс при очистке линий. Это означает что при каждой очистке вы будеде ждать 500 мс, прежде чем можно будет делать что-либо ещё. Все медленные комнаты обозначаются значком спидометра - [SPEEDOMETER_ICON]. Медленные комнаты могут иметь ограничение от 0 до 20 PPS.

![Лобби, в котором вы можете создавать комнаты и присоединяться к ним][image5]

### Map Room

**Map Room** - это место, где можно соревноваться в очистке на случайной пользовательской карте. Число (D=?%), показываемое рядом с именем карты, означает сложность карты, где 0% - легчайшая карта, и 100% - сложнейшая. Карты, требующие завершения с Perfect Clear, не выпадают в этой комнате.

- - -

## Одиночная игра

### Спринт

Базовый режим с простейшей целью, **Спринт** - самый популярный режим одиночной игры в Jstris. Очистите Х линий так быстро, как можете. В Jstris есть спринт режимы для 20, 40, 100 и 1000 линий.

### Очистка

Не такой быстрый, и более аналитический, чем Спринт, режим **Очистки** предполагает больше размышлений в процессе очищения мусора наиболее эффективным способом. В Jstris есть режимы очистки для 10, 18, 100 и бесконечного числа линий.

### Ультра

Режим, рассчитанный на набор максимального количество очков, и награждающий за продвинутые техники, такие, как T-спины и back-to-back. **Ультра** - замечательный способ тренировать атаку для последующего применения в режимах против игроков.

### Выживание

Возможно, самый сложный режим среди всех режимов одиночной игры. **Выживание** похож на очистку, но мусор добавляется с постояннной скоростью: 1 линия в секунду. Выживайте против растущих линий так долго, как можете.

### Карты

Режим **Карты** был добавлен в Jstris в конце 2018 года. Карты вносят элемент креативности, при этом улучшая навыки очистки в сложных и необычных позициях. Создайте свою карту в **Дизайнере Карт**. Как только карта опубликована, игроки из любой точки мира могут играть и соревноваться в скорости на вашей карте. В Jstris ограничивает создание карт пятью публикациями в день и десятью неопубликованными картами в очереди. Карты включены в таблицу рекордов. На каждой карте можно завоевать три медали, золотую за первое, серебряную за второе, бронзовую за третье место. Пробуйте войти в топ-3 на любой карте чтобы завоевать медали и своё место в таблице лидеров!

*\*Таблица лидеров карт обновляется несколько раз в день, поэтому изменения в ней не мгновенно отражают текущую ситуацию.*

### 20TSD

Цель этого режима - выполнить как можно больше TSD (T-spin Double) друг за другом. Если вы очищаете линию, не используя TSD, игра завершается. Режим назван 20TSD, потому что изначально люди выполняли спринт длиной 40 линий, используя только TSD (20 х 2 = 40). Однако, многие игроки выходят за эти рамки и регулярно превышают число 20.

- - -

## Настройка

Чтобы увидеть настройки любой комнаты, используйте команду `/config`. Ниже мы пробежимся по всем возможным опциям.

### Атака и Комбо

По умолчанию, атака и комбо в Jstris выглядят так (можно перенастроить в приватных комнатах):

| Тип атаки          | Количество посланных линий |   | Комбо # | Количество посланных линий |
| :----------------- | -------------------------: | - | ------: | -------------------------: |
| 1 линия (single)   |                      **0** |   |       1 |                      **0** |
| 2 линии (double)   |                      **1** |   |       2 |                      **1** |
| 3 линии (triple)   |                      **2** |   |       3 |                      **1** |
| 4 линии            |                      **4** |   |       4 |                      **1** |
| T-spin Double      |                      **4** |   |       5 |                      **2** |
| T-spin Triple      |                      **6** |   |       6 |                      **2** |
| T-spin Single      |                      **2** |   |       7 |                      **3** |
| T-spin Mini Single |                      **0** |   |       8 |                      **3** |
| Perfect Clear      |                     **10** |   |       9 |                      **4** |
| Back-to-Back       |                     **+1** |   |      10 |                      **4** |
|                    |                            |   |      11 |                      **4** |
|                    |                            |   |     12+ |                      **5** |

### Распределение мусора

В Jstris существует 8 опций для распределения мусора от вашей атаки в матчах против игроков:

- Targets (Цели) `/set garbage targets`
- Divide (Разделение) `/set garbage divide`
- To all (Всем) `/set garbage toAll`
- To least (Наименьшему) `/set garbage toLeast`
- To most (Наибольшему) `/set garbage toMost`
- To self (Себе) `/set garbage toSelf`
- Random (Случайно) `/set garbage random`
- Roulette (Рулетка) `/set garbage roulette`

**Targets** (Цели) - обычно является опцией по умолчанию и самым популярным выбором. В этом режиме, цель равновероятно выбирается по очереди из всех оппонентов в комнате. Игрок, являющийся целью в момент атаки и получает посланный вами мусор.

**Divide** (Разделение) - мусор делится поровну между игроками комнаты. Например, если вы выполняете TSD в комнате с двумя другими оппонентами, каждый из них получит по 2 линии мусора.

**To all** (Всем) - все производимые вами атаки отсылаются каждому из ваших оппонентов в комнате. К примеру, если вы выполняете Perfect Clear в комнате с 4-мя оппонентами, то каждый из них получает 10 линий мусора, то есть, вы посылаете 40 линий мусора в целом. Из приведённого примера вы уже наверное поняли, что игры в этом режиме с беспорядочно возрастающим мусором характерно короткие.

**To least** (Наименьшему) - мусор получает игрок, который *пострадал* меньше всех от предыдущих атак. Предположим, в комнате с тремя оппонентами, вы посылаете 4 линии. Игрок А уже получил 50 линий урона к этому моменту. Игрок Б получил 53. Игрок В получил 58. Так, как игрок А получил меньше всего линий, вся ваша атака - 4 линии, отправляется к нему.

**To most** (Наибольшему) - мусор получает игрок, которые *послал* больше всего атак. По сути, вы атакуете самого сильного игрока комнаты.

**To self** (Себе) - ваша атака отсылается вам самому. Непрактично в игре против других игроков, но кому-то этот режим может быть полезен для тренировок в одиночку.

**Random** (Случайно) - атака отсылается случайному оппоненту. Возможно, самый честный режим.

**Roulette** (Рулетка) - тоже самое, что предыдущее, но атака может быть послана и вам в том числе.

### Блокировка мусора 

В Jstris 4 типа блокировки мусора:

- Full (Полная)
- Limited (Ограниченная)
- None (Отсутствует)
- Instant (Мгновенная)

**Full** (Полная) - блокировка по умолчанию. Другие клиенты, которые используют Full, это *TF* (комнаты e+) и *TOP*.  В этом режиме, появляется индикатор мусора в виде красной полосы справа от вашего игрового поля. Мусор не попадает на ваше поле до тех пор, пока вы не поставите блок. Мусор может быть уменьшен с помощью вашей атаки (например, снятием 4-х линий). Если вы начали комбо, то мусор будет заморожен от появления на поле до тех пор, пока вы не закончите своё комбо.

**Limited** (Ограниченная) - данный тип блокировки очень похож на Full, но с одним отличием. Входящий мусор попадает на ваше поле вне зависимости от того, выполняете ли вы комбо или нет. Другими словами, мусор не приостанавливается во время комб, как в режиме Full. Входящий мусор также может быть уменьшен с помощью атак. Клиенты, использующие Limited включают *PPT*, *TB* и *TF* (не e+ комнаты).

**None** (Отсутствует) - в этом режиме, мусор не может быть уменьшен или отменён. Изначально он появляется в виде красной полосы (как в режимах Full и Limited), и попадает на ваше игровое поле как только вы поставите блок. К примеру, если оппонент послал вам 10 линий, даже если вы сняли 4 линии следующим блоком, то входящий мусор не будет уменьшен до 6 линий. Вместо этого, вы получите все 10 линий мусора, и пошлёте оппоненту 4 линии.

**Instant** (Мгновенная) - в этом режиме вообще нет красной полосы. Мусор попадает на ваше поле в момент, когда оппонент посылвает его. Отмера части мусора невозможна.

|         | Красная полоса | Отмена |
| ------- | :------------: | :----: |
| Full    |       Да       |  Да    |
| Limited |       Да       |  Да    |
| None    |       Да       |  Нет   |
| Instant |       Нет      |  Нет   |

### Блоки

В игре 8 типов наборов блоков.

- Standard
- Big
- ARS
- Penta
- M123
- All-29
- C2RS
- O-spin

**Standard** Самые распространённые и простые тетромино, с которыми вы уже вероятно знакомы. Являются блоками по умолчанию.

**Big** Увеличенные в 4 раза по сравнению со стандартными блоками, такие блоки наносят массивный урон.

**ARS** Стандартные блоки, но управляемые ARS (Arika rotation system), включая CC-проверку. Запрограммированы NueSB

**Penta** Пентомино блоки, 18 разных фигур.

**M123** Блоки размером 1,2 и 3. Всего существует 4 разных блока такого типа.

**All-29** Блоки размером 1,2,3,4,5, всего 29 разных блоков. Включает в себя 7 стандартных, 4 M123 и 18 пентаблоков.

**C2RS** стандартные блоки, но управляемые Cultris 2 rotation system.

**O-spin** система поворотов, возникшая из мемов, где возможны тройной (2 х по часовой стрелке) и четверной (1 х против часовой стрелки) повороты фигуры О. Также, возможны другие нетрадиционные повороты (из за того, что таблица толчков содержит 15 уровней, тогда как стандартная система поворотов SRS содержит только 4 уровня).

### Рандомайзер

Рандомайзер - это формула, по которой формируется порядок выпадающих блоков. Jstris имеет 11 разных рандомайзеров:

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

**7-bag** - стандартный рандомайзер по умолчанию. Представьте себе мешок с 7-ю фигурами, по одной из всех возможных. Вы вытаскиваете из мешка фигуры одну за одной, до тех пор, пока он не опустеет. Тогда вы получаете точно такой же новый мешок, опять с 7-ю фигурами. Опять вытаскиваете одну за одной до тех пор, пока он не опустеет. Повторяете. Так и работает 7-bag рандомайзер.

**14-bag** - похож на 7-bag, но двойного размера, с двумя фигурами каждого типа из 7-ми возможных блоков. Также вытаскиваете по одной фигуре до тех пор, пока мешок не опустеет. Повторяете.

**Classic** - полностью случайные фигуры. Этот рандомайзер делает постройку очень трудным делом.

**C2Sim** - рандомайзер Cultris 2, описанный здесь [post by Integration](http://harddrop.com/forums/index.php?showtopic=5080&st=0&p=71443&#entry71443)

**One block** - этот рандомайзер даёт вам только одну фигуру, выбранную случайно в начале игры. Вам будет выпадать только этот блок.

**Two block** - рандомайзер, похожий на предыдущий, но дающий два разных блока вместо одного.

**One 7-bag** - первый мешок в игре будет повторяться бесконечно. Используя этот рандомайезр, одна и та же очередь из 7 фигур будет выпадать снова и снова.

**One 14-bag** - похоже на предыдущий режим, но очередь ограничена 14-ю фигурами, которые будут повторяться снова и снова.

**Repeat+7b** - работает, как 7-bag, только каждая фигура в мешке имеет шанс быть повторённой 1-7 раз.

**BSblock+7b** - работает, как 7-bag, только может включать фигуры из других наборов блоков, например, пентомино или больших блоков.

**BigBlock+7b** - работает, как 7-bag, только может включать большие блоки.

### Длина очереди 

Jstris по умолчанию показывает 5 превью очереди. В созданных вами комнатах, вы можете настроить от нуля до пяти превью.

### Заполнение постоянным мусором

Постоянный мусор это неочищаемые линии, которые прибавляются снизу для того, чтобы подогнать игру и она не продолжалась бесконечно. Такие линии немного темнее, чем обычный мусор. В комнате с ботом постоянный мусор по умолчанию начинает появляться через 2 минуты. Этот параметр может настраиваться в созданных вами комнатах.

![Solid Garbage][image7]

### Задержка перед фиксацией

Задержка перед фиксацией означает сколько времени установленная фигура будет ожидать прежде чем зафиксируется. В Jstris есть три типа задержек, которые можно настроить. Первая, L1, означает задержку перед фиксацией фигуры после софт дропа. По умолчанию, задержка L1 = 500 мс. Вторая, L2, означает как долго можно перемещать уроненную софт дропом фигуру налево или направо (по умолчанию 5000 мс). Следует заметить, что если фигуру повернули, то L2 сбрасывается и фигура может быть перемещена дольше, чем в течении обычных 5000 мс, что приводит нас к задержке L3. L3 означает максимальное количество времени после появления фигуры на поле, перед её финальной фиксацией, вне зависмости от совершаемых вами действий. По умолчанию, L3 = 20000 мс.

### Задержка очистки

Задержка очистки это фиксированное количество времени, которое проходит после очистки одной или более линий. Во время этой задержии вы не можете ничего делать. Много классических пазловых игр и PPT используют задержку очистки, но в Jstris по умолчанию задержка очистки = 0, и для большинства режимов она никогда не используется. Однако, это настраивается, если вы хотите включить её. Допустимые значения - от нуля и до 6000 мс.

### Гравитация

Гравитация представляет собой скорость, с которой фигуры автоматически падают вниз. Гравитация может быть изменена в пределах 0-28 уровня. Гравитация по умолчанию = 1. Если гравитация =0, то фигура не упадёт вниз до тех пор, пока не истечёт задержка L3 (по умолчанию, 20 секунд). 28 уровень гравитации эквивалентен 20G, при этом фигура мгновенно падает до самого низа.

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
- Live Survival
- Live Maps v0.1

**Standard** mode is normal multiplayer free-for-all. 

**Team** mode creates a custom Team Room. Pick a side, red or blue, and battle and bring glory for your team. To set your own team name, use the command `/set teamName ?` where the ? is replaced with your team name. 

![team game in progress][image11]

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
