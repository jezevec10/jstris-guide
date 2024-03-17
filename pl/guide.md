# Jstris Guide

Witaj w Jstris! Jstris to prosta gra sieciowa polegająca na układaniu spadających bloków. Jstris jest znany ze swojej szybkiej rozgrywki i przyciąga utalentowanych graczy z całego świata. Ten przewodnik wprowadzi Cię do prostych funkcji tej gry.

- - -

**Spis treści**

- [Przegląd](#przegląd)
- [Sterowanie](#sterowanie)
- [Tryb wieloosobowy](#tryb-wieloosobowy)
  - [Pokój Domyślny](#pokój-domyślny)
  - [Pokój z botami](#bot-room)
  - [Pokój 1 na 1](#1v1-room)
  - [Powolny pokój](#slow-room)
  - [Pokój z mapami](#map-room)
- [Singleplayer](#singleplayer)
  - [Sprint](#sprint)
  - [Cheese Race](#cheese-race)
  - [Ultra](#ultra)
  - [Przetrwanie](#survival)
  - [Mapy](#maps)
  - [20TSD](#20tsd)
- [Konfiguracja](#configuration)
  - [Tablica ataków i kombo](#attack-and-combo-table)
  - [Rozłożenie śmieci](#garbage-distribution)
  - [Blokowanie śmieci](#garbage-blocking)
  - [Kombo](#blocks)
  - [Randomizer](#randomizer)
  - [Podgląd](#previews)
  - [Solidne śmieci](#solid-garbage)
  - [Opóźnienie blokady](#lock-delay)
  - [Opóźnienie czyszczenia](#clear-delay)
  - [Poziom grawitacji](#gravity-lvl)
  - [Opóźnienie śmieci](#garbage-delay)
  - [Nieuporządkowanie](#messiness)
  - [Konfiguracje wstępne](#configuration-presets)
  - [Tryby gry](#mode)
- [Często zadawane pytania](#faq)
  - [P: Czy mogę dodać bota do mojego prywatnego lub własnego pokoju?](#q-can-i-add-a-bot-to-my-private-or-custom-room)
  - [P: Co znaczą te wszystkie skróty w tabeli Rezultatów Gry?](#q-what-do-those-abbreviations-in-the-game-results-table-mean)
  - [P: Co to jest DAS?](#q-what-is-das)
  - [P: Co to jest ARR?](#q-what-is-arr)
  - [P: Co to jest finezja?](#q-what-is-finesse)
  - [P: Czy mogę utworzyć prywatny pokój?](#q-can-i-create-a-private-room)
  - [P: Czy mogę grać w Jstris bez dostępu do sieci?](#q-can-i-play-jstris-offline)
- [Dodatkowe informacje](#additional-information)

- - -

## Przegląd

Jstris używa tych samych podstawowych mechanik co inne układanki ze spadającymi klockami tego typu. Zasady tej gry są w większości zgodne z wytycznymi na których podstawie tworzone są oficjalne gry. Godna uwagi cecha tej gry jest jej rozległe użycie powtórek. W każdym trybie gry w którym grasz i który ukończyłeś/aś, powtórka będzie automatycznie wygenerowana dla Ciebie. Oglądanie i analizowanie swoich własnych gier jest integralną częścią doskonalenia swojej rozgrywki. Powtórki Jstrisa bardzo ułatwiają owe analizy.

W przeciwieństwie do innych stron, bądź pewny że rankingi Jstrisa są kompletnie czyste i pozbawione oszustów. Moderatorzy skrupulatnie usuwają podejrzane rekordy by mieć pewność że lista globalnych osiągnięć jest warta zaufania.

Możesz grać bez rejestrowania się, lecz by używać wszystkich funkcji tej strony, stworzenie konta jest zalecane. By to zrobić, kliknij na przycisk *Zarejestruj się* w prawym górnym rogu. Wymagane są jedynie: e-mail, nazwa użytkownika i hasło. Z kontem, możesz zobaczyć mnogość statystyk, włącznie z twoimi Najlepszymi Czasami w trybach jednoosobowych, statystykami z gier wieloosobowych, statystykami postępów, powtórkami, i wiele innych. Możesz także zobaczyć siebie w Rankingu (wyniki użytkowników niezarejestrowanych są pominięte).

![introduction][image2]
- - -

## Sterowanie

Jstris allows for players to customize their controls at any time in the **Settings** menu that is located underneath the main play area. Default controls are as follows:

|   Polecenie      | Domyślny klawisz |
| ---------------- | ---------------- |
| Przesuń w lewo   | strzałka w lewo  |
| Przesuń w prawo  | strzałka w prawo |
| Upuść miękko     | strzałka w dół   |
| Upuść twardo     | spacja           |
| Obróć w lewo     | z                |
| Obróć w prawo    | strzałka w górę  |
| Obróć o 180°     | a                |
| Przytrzymaj blok | c                |

## Tryb wieloosobowy

### Pokój domyślny

Po wejściu na stronę, wszyscy gracze są natychmiast wrzuceni do **Pokoju domyślnego**, w którym znajdziesz graczy z każdego poziomu uzdolnienia.

Gra w domyślnym pokoju może być ciężka! Unikalną cechą Jstrisa jest to, że wrzuca początkujących i światowej klasy przeciwników, włącznie ze wszystkimi pomiędzy, w jedną arenę! Jeżeli jesteś zmęczony grą i chcesz po prostu oglądać, użyj komendy `/spectate` lub `/spec`. Jeśli chcesz zagrać ponownie, użyj komendy `/play`.

### Pokój z botami

# *&lt;This section is very outdated, nowadays bot rooms are private rooms created by using the menu.&gt;*

Pokój domyślny nie jest jedynym dostępnym pokojem. By zobaczyć pełną listę pokoi, wciśnij przycisk *lobby* blisko lewego dolnego rogu twojej planszy. Drugim najpopularniejszym pokojem na Jstris jest zazwyczaj **Pokój z botami**, nazwany tak ponieważ w nim występuje co najmniej jeden Bot. Bot jest zawsze umiejscowiony w prawym górnym rogu przeciwników. Łatwo da się go zauważyć przez swój unikalny czerwony kolor.

![MisaMino bot in opponents view][image4]

W Jstris występują 4 boty. Wymienione są poniżej, posortowane zgodnie z ich siłą, wraz z komendami do zmiany bota, wpisywane do okienka czatu.

- MisaMino: `/changeBot misamino`
- ColdClear
- Freybot
- Dellacherie
- ~~Real_Block: `/changeBot real`~~ (usunięty dnia *&lt;insert date of removal here&gt;*)
- ~~jez_Block: `/changeBot jez`~~ (usunięty dnia 21.09.2018)
- ~~Fool bot: `/changeBot fool`~~ (usunięty dnia 21.09.2018)

*\*Zwróć uwagę na to że wszystkie komendy muszą być wykonane pomiędzy grami. Wszystkie komendy wykonane w trakcie gry nie dadzą żadnych rezultatów.*

MisaMino jest jak na razie najmocniejszym botem, być może nawet najsilniejszym botem stawiającym spadające bloki kiedykolwiek stworzonym. Kiedy zestawiony z maksymalną prędkością 5 PPS (Pieces Per Second - bloków na sekundę), MisaMino staje się potężnym przeciwnikiem który rozwala nawet najsilniejszych ludzi w pojedynku. Jednakże osiągi bota są dużo słabsze gdy w Pokoju z botami znajduje się powyżej 5 ludzi - może natychmiast przegrać. To nas prowadzi do naszej następnej komendy: `/botPPS`.

Prędkość bota może być zmieniona. By to zrobić, wpisz `/bot ?` - w miejsce `?` wpisz jakąkolwiek liczbę pomiędzy 0.3 a 5. Na przykład, gdybym chciał by bot grał z prędkością 2 PPS, wpisałbym `/bot 2`. Gdybym chciał by bot grał z prędkością 1,73 PPS, wpisałbym `/bot 1.73`. Zwróć uwagę, by użyć kropki jako separatora dziesiętnego, a nie przecinka!

### Pokój 1 na 1

W **Pokoju 1 na 1** może grać maksimum 2 użytkowników, jednakże każdy może dołączyć i oglądać nawet jeśli pokój jest pewny. Użyj tego pokoju aby powalczyć ze swoimi znajomymi albo by zawalczyć przeciwko godnemu przeciwnikowi. Jeżeli zapisujesz wyniki, i chcesz je zresetować, użyj komendy `/resetCounter` - wszystkie wyniki zostaną zresetowane do 0.

### Powolny pokój

Chcesz pograć ze znajomym ale różnica poziomów uzdolnienia pomiędzy wami jest zbyt wysoka? Albo może po prostu zaczynasz i jesteś zmęczony przegrywaniem niemalże natychmiastowo w Pokoju z botami zdominowanego przez profesjonalnych graczy? A może po prostu chciałbyć/chciałabyś poćwiczyć efektywność w swojej grze poprzez eliminację prędkości z równania? Dla tychże okazji znajduje się Powolny pokój. Domyślne ograniczenie prędkości Powolnego pokoju to 1.5 PPS, co oznacza że gracz nie może przekroczyć 1.5 PPS przez zbyt długi czas. Jakiekolwiek próby przekroczenia tej prędkości spowodują, że gracz nie może upuszczać bloków przez chwilę. Dodatkowo, Powolny Pokój posiada opóźnienie przy czyszczeniu linii o długości 500 ms. To oznacza, że po każdym wyczyszczeniu linii, musisz poczekać 500 ms zanim możesz kontrolować następne klocki. Wszystkie Powolne pokoje są oznaczone małym prędkościomierzem - [SPEEDOMETER_ICON]. Własne Powolne pokoje mogą mieć dowolne ograniczenie prędkości pomiędzy 0 PPS a 20 PPS.

![the lobby, where you can join and create rooms][image5]

### Pokój z mapami

**Pokój z mapami** to miejsce, gdzie musisz jak najszybciej wyczyścić losowe mapy stworzone przez użytkowników. (D=?%) wyświetlane obok każdej mapy to poziom trudności (centyl) tej mapy. 0% to najłatwiejsze mapy, 100% to najtrudniejsze mapy. Mapy które wymagają Perfekcyjnego Wyczyszczenia nie są w puli wybieranych map.

- - -

## Tryb jednoosobowy

### Sprint

Będący podstawowym trybem z prostym celem, **Sprint** jest najpopularniejszym trybem jednoosobowym w Jstris. Wyczyść X linii tak szybko, jak tylko potrafisz. Jstris oferuje Sprinty na 20, 40, 100 i 1000 linii.

### Cheese Race

Będącym mniej bezczelnym i bardziej analiczyczym trybem niż Sprint, **Cheese Race** wymaga więcej myślenia - musisz przekopać się przez linie śmieci jak naszybciej i/lub jak najefektywniej. Jstris oferuje Cheese Race na 10, 18 i 100 lini, oraz nieskończony Cheese Race.

### Ultra

**Ultra** jest trybem, gdzie w czasie 2 minut musisz osiągnąć jak najwyższy wynik. Ultra wynagradza zaawansowane techniki takie jak T-spiny i Back-to-Back, które są użyteczne także przy wysyłaniu potężnych ataków do swoich przeciwników w trybie wieloosobowym.

### Przetrwanie

**Przetrwanie** to najprawdopodobniej najbardziej wyzywający tryb jednoosobowy tej gry. **Przetrwanie** jest bardzo podobny do Cheese Race, jednak śmieci są dodawane do twojej planszy stale co sekundę. Przetrwaj przeciwko szybko podnoszącym się śmieciom jak najdłużej, jak tylko potrafisz.

### Mapy

Późno w roku 2018, Tryb **Mapy** został wprowadzony do Jstrisa. Mapy wprowadzają element kreatywności oraz przygotowywują graczy na efektywne przekopywanie się przez trudne lub dziwne pozycje. Stwórz swoją własną mapę w *Projektancie map*. Gdy opublikujesz mapę, gracze z całego świata mogą rozgrywać ją i walczyć o jak najlepszy czas. Mapy posiadają limit 5 publikacji na dzień oraz 10 nieopublikowanych map w kolejce. Każda mapa posiada ranking. Na każdej mapie rozdawane są 3 medale - Złoty za pierwsze miejsce, Srebrny za drugie miejsce i Brązowy za trzecie miejsce. Stań na podium mapy by wygrać medale i zabezpieczyć swoje miejsce w rankingu!

*\*Zwróć uwagę na to, że ranking Map aktualizuje się tylko kilka razy dziennie, więc nowe zmiany nie są natychmiastowe.*

### 20TSD

Celem tego trybu jest osiągnięcie jak największej ilości Podwójnych T-spinów. Gra kończy się jeżeli twoje wyczyszczenie linii nie jest podwójnym T-spinem. Tryb jest nazwany 20TSD, ponieważ oryginalnym konceptem było wykonanie sprintu na 40 linii używając 20 podwójnych T-spinów (20 x 2 = 40). Gra w trybie 20TSD nie kończy się po osiągnięciu 20 podwójnych T-spinów. Niektórzy teraz regularnie przekraczają barierę 20 podwójnych T-spinów.

- - -

## Konfiguracja

By zobaczyć konfigurację dowolnego pokoju na Jstris, użyj komendy `/config`. Teraz omówmy każde z ustawień.

### Tablica ataków i kombo

Domyślna tablica ataków i kombo w Jstris (która może być dostosowana w prywatnych pokojach) wygląda następująco:

| Typ ataku                     | Wysłane linie |   | Kombo   | Wysłane linie |
| :---------------------------- | ------------: | - | ------: | ------------: |
| 0 linii                       |         **0** |   |       0 |        **+0** |
| 1 linia (single)              |         **0** |   |       1 |        **+0** |
| 2 linie (double)              |         **1** |   |       2 |        **+1** |
| 3 linie (triple)              |         **2** |   |       3 |        **+1** |
| 4 linie                       |         **4** |   |       4 |        **+1** |
| TSD (Podwójny T-spin)         |         **4** |   |       5 |        **+2** |
| TST (Potrójny T-spin)         |         **6** |   |       6 |        **+2** |
| TSS (Pojedynczy T-spin)       |         **2** |   |       7 |        **+3** |
| MTSS (Pojedynczy T-spin Mini) |         **0** |   |       8 |        **+3** |
| Perfekcyjne Wyczyszczenie     |        **10** |   |       9 |        **+4** |
| Back-to-Back                  |        **+1** |   |      10 |        **+4** |
|                               |               |   |      11 |        **+4** |
|                               |               |   |     12+ |        **+5** |

### Rozłożenie śmieci

W Jstris dostępne jest 8 różnych systemów rozłożenia wysyłanych śmieci w grach wieloosobowych. One są następująco:

- Targets (Cele) `/set garbage targets`
- Divide (Podzielone równo) `/set garbage divide`
- To all (Do wszystkich) `/set garbage toAll`
- To least (Do najmniejszej) `/set garbage toLeast`
- To most (Do największej) `/set garbage toMost`
- To self (Do siebie) `/set garbage toSelf`
- Random (Losowo) `/set garbage random`
- Roulette (Ruletka) `/set garbage roulette`

**Targets (Cele)** to zawsze domyślny (z wyłączeniem Pokoju drużynowego) i jak na razie najbardziej popularny system rozłożenia śmieci. W systemie Targets, cel jest co jakiś stały czas przesuwany pomiędzy wszystkie osoby w pokoju. Wysyłasz śmieci do osoby która jest akurat na twoim celowniku.

W systemie **Divide (Podzielone równo)**, śmieci które wysyłasz są równo podzielone pomiędzy wszystkich graczy. Na przykład, w pokoju z dwoma innymi przeciwnikami, jeśli wyślesz podwójnego T-spina (4 linie), każdy z twoich przeciwników odbierze 2 linie.

W systemie **To all (Do wszystkich)**, śmieci które wysyłasz są wysyłane do każdego gracza w pokoju. Na przykład, jeżeli wyślesz Perfekcyjne Wyczyszczenie (10 linii), każdy z 4 przeciwników odbierze 10 linii, co łącznie daje 40 linii. Jak możesz zauważyć z tego przykładu, pokoje z tym systemem mają tendencję do posiadania bardzo szybkich, szalonych gier, z szybko unoszącymi się śmieciami.

W systemie **To least (Do najmniejszej)**, śmieci które wysyłasz są wysyłade do osoby która *odebrała* najmniej śmieci jak do tej pory. Na przykład, w pokoju z trzema innymi przeciwnikami, wysyłasz 4 linie. Przeciwnik A odebrał 50 linii jak do tąd w momencie w którym atak został wysłany przez Ciebie. Przeciwnik B odebrał 53 linie. Przeciwnik C odebrał 58 linii. Ponieważ przeciwnik A odebrał najmniej linii jak do tąd, 4 linie zostaną wysłane do przeciwnika A.

W systemie **To most (Do największej)**, śmieci które wysyłasz są wysyłane do osoby która *wysłała* najwięcej śmieci jak do tej pory. W skrócie, atakujesz najsilniejszą osobę w pokoju.

W systemie **To self (Do siebie)**, śmieci wysyłasz do samego siebie. System niepraktyczny w trybie wieloosobowym, ale może być użyteczny jeżeli chcesz poćwiczyć samemu z tym systemem.

W systemie **Random (Losowo)**, śmieci które wysyłasz są wysyłane do losowego gracza. Prawdopodobnie najuczciwszy system rozłożenia śmieci.

W systemie **Roulette (Ruletka)**, śmieci które wysyłasz są wysyłane do losowego gracza, *wliczając w to siebie*.

### Blokowanie śmieci

W Jstris występują 4 systemy blokowania śmieci:

- Full (Pełny)
- Limited (Ograniczony)
- None (Żaden)
- Instant (Natychmiastowy)

**Full (Pełny)** to domyślny system blokowania śmieci w Jstris. Inne klienty używające systemu **Full** to *TF* (pokoje e+), *TOP* oraz *TE:C*. W tym systemie nadchodzące śmieci pojawiają się jako czerwony pasek po prawej stronie planszy. Śmieci nie podnoszą się, dopóki nie upuścisz klocka, który nie czyści linii. Ilość śmieci może być zredukowana poprzez wysyłanie linii (na przykład czyszcząc 4 linie na raz). Dopóki czyścisz linie (na przykład podczas kombo), śmieci nie będą się podnosić, dopóki nie skończysz swojego kombo.

**Limited (Ograniczony)** system blokowania śmieci jest bardzo podobny do Full (Pełnego) z jedną różnicą. Nadchodzące śmieci są wstawiane po upuszczeniu klocka, nie ważne czy ten klocek wyczyścił linię czy też nie. Innymi słowami, nadchodzące śmieci mogą być wstawione podczas wykonywania kombo, w przeciwieństwie do systemu Full. Tak jak w Full, możesz redukować ilość śmieci poprzez wysyłanie linii. Klienty które używają systemu Limited to na przykład *PPT2*, *PPT*, *TB* i *TF* (oprócz pokoi e+).

W systemie **None (Żadnym)**, śmieci nigdy nie mogą być zredukowane lub zniwelowane. Nadchodzące śmieci najpierw się pojawią jako czerwony pasek (tak jak w Full i Limited) a potem będą wstawione na twoją planszę jak tylko upuścisz klocek. Jeśli przeciwnik wyśle ci 10 linii, nawet jeśli wyczyścisz 10 linii twoim następnym klockiem, ilość śmieci nie będzie ograniczona do 6. Zamiast tego, ty wciąż otrzymasz 10 linii śmieci podczas gdy 4 linie zostaną wysłane do przeciwnika.

W systemie **Instant (Natychmiastowym)** nie ma czeronego paska. Gdy przeciwnik atakuje, śmieci pojawią się natychmiast na twojej planszy. Nie da się ich zablokować.

|                          | Czerwony pasek (kolejka) | Blokowanie? |
| ------------------------ | :----------------------: | :---------: |
| Full (Pełny)             |           Tak            |     Tak     |
| Limited (Ograniczony)    |           Tak            |     Tak     |
| None (Żaden)             |           Tak            |     Nie     |
| Instant (Natychmiastowy) |           Nie            |     Nie     |

### Bloki

W Jstris występuje 8 rodzajów bloków.

- Standard (Standardowe)
- Big (Duże)
- ARS
- Penta (Pentomino)
- M123
- All-29 (Wszystkie 29)
- C2RS
- O-spin

**Standard (Standardowe)** Podstawowy zestaw 7 tetromino który znasz i kochasz. Najczęściej używane, domyślne bloki.

**Big (Duże)** 7 tetromino, jednak te bloki są czterokrotnie większe. Zadają one masywne obrażenia.

**ARS** 7 tetromino posiadająych ARS (Arika Rotation System), włącznie ze sprawdzaniem centralnej kolumny. Zaimplementowane przez NueSB.

**Penta (Pentomino)** 18 różnych pentomino.

**M123** Bloki składające się z 1, 2 lub 3 kwadratów (mino). Łącznie 4 unikalne bloki M123.

**All-29** Wszystkie bloki składające się z 1, 2, 3, 4 lub 5 kwadratów (mino) - łącznie 29 unikalnych bloków. Bloki Standard, M123 i Penta w jednym worku.

**C2RS** 7 tetromino posiadających system obrotów z gry Cultris 2.

**O-spin** 7 tetromino posiadających żartobliwy system obrotów. W tym systemie możliwy jest potrójny O-spin (2x obrót w lewo) i poczwórny O-spin (1x obrót w prawo) są możliwe. Możliwe są też inne niekonwencjonalne spiny, ponieważ tablica przesunięć posiada 15 przesunięć. Dla porównania, SRS posiada ich tylko 5.

### Randomizer

Randomizery to systemy losujące w jakiej kolejności i jakie dostaniesz kolejne bloki. Jstris posiada 11 różnych randomizerów:

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

**7-bag** to standardowy i domyślny randomizer. Wyobraź sobie mały worek z każdym z 7 różnych bloków. Wyjmujesz bloki z worka, jeden po jednym, dopóki worek nie zostanie opróżniony. Następnie dostajesz kolejny workek z każdym z 7 bloków. Następnie znowu wyjmujesz bloki jeden po jednym. I tak w kółko. Tak działa 7-bag.

**14-bag** jest podobny do 7-bag, jednak worek jest 2 razy większy. Worek tym razem posiada po 2 z każdego z 7 różnych bloków. Jeszcze raz, wyjmujesz klocki z worka, jeden po jednym, dopóki worek nie zostanie opróżniony. I tak w kółko.

**Classic** daje ci losowe klocki. Układanie klocków przy tym randomizerze jest wyzywające.

**C2Sim** Symulacja randomizera z gry Cultris 2, objaśnionym w tym [poście napisanym przez Integration](http://harddrop.com/forums/index.php?showtopic=5080&st=0&p=71443&#entry71443).

**One block** Ten randomizer na początku losuje blok. Przez całą grę będziesz otrzymywać jedynie ten jeden blok.

**Two block** Ten randomizer jest podobny to One Block, jednakże on losuje 2 bloki, które będziesz otrzymywać naprzemiennie przez całą grę.

**One 7-bag** Na początku gry jest losowany losowy ciąg 7 różnych bloków. Ten ciąg będzie zapętlony przez całą grę. Używany przez *TE:C* w trybach Relax jeśli *Tetromino Order* zostanie ustawiony na *Fixed*.

**One 14-bag** Na początku gry jest losowany losowy ciąg 14 bloków - po 2 z 7 różnych bloków. Ten ciąg będzie zapętlony przez całą grę.

**Repeat+7b** Działa jak 7-bag, jednak dowolny klocek w worku może zostać powtórzony 1-7 razy.

**BSblock+7b** 7-bag, jednak może on dodać bloki z innych zestawów (dlatego w nazwie jest BS - Block Sets), takich jak pentomino lub duże bloki.

**BigBlock+7b** 7-bag, jednak mogą się w nim pojawiać duże bloki.

### Podgląd

Domyślnie Jstris ma podgląd na następne 5 klocków. We własnych pokojach możesz ustawić podgląd na od 0 do 5 klocków.

### Solidne śmieci

Solidne śmieci to niewyczyszczalne śmieci które nadchodzą z dołu planszy by “pośpieszyć” grę tak aby nie przedłużała się w nieskończoność. Solidne śmieci są ciemniejsze niż zwykłe śmieci. W domyślnych pokojach, solidne śmieci zaczynają się pojawiać od 2 minuty gry. Solidne śmieci są dostosowywalne we własnych pokojach.

![Solid Garbage][image7]

### Opóźnienie blokady

Opóźnienie blokady określa, ile czasu klocek może zostać na ziemi, zanim ten klocek zostanie zablokowany. W Jstris występują trzy typy opóźnienia blokady które mogą być dostosowane. Pierwszy (L1) określa przez jaki czas klocek może pozostać na ziemi nieruchomo, zanim ten klocek zostanie zablokowany. Domyślne opóźnienie L1 to 500 ms. Drugi (L2) określa przez jaki czas klocek może pozostać na ziemi, jeśli jest on poruszany w lewo/prawo, zanim ten klocek zostanie zablokowany. Domyślne opóźnienie L2 to 5000 ms (5 s). Zwróć uwagę na to, że jeśli klocek jest obrócony, opóźnienie L2 zostaje zresetowane i klocek może pozostać aktywny przez czas dłuższy niż 5000 ms.
Trzeci, L3, określa przez jaki czas klocek może być aktywny, zanim zostanie automatycznie upuszczony bez Twojej zgody. Domyślne opóźnienie L3 to 20000 ms (20 s).

### Clear Delay

Clear delay is a fixed amount of time that passes after you clear any line(s). During this time, you can’t do anything. Many classic block games and PPT use clear delay, but Jstris by default has 0 delay, and for the most part it is never used here. However, it is customizable if you want to turn it on. Its range is 0 milliseconds to 6000 milliseconds.

### Gravity lvl

Gravity level refers to the rate at which the pieces fall down the matrix automatically. The Gravity can be adjusted from levels 0-28. The default Gravity is 1. If gravity is 0, the piece will not fall down at all until it is autolocked after the 20 second L3 lock delay (see section Lock Delay). A Gravity level of 28 is equal to 20G, which means pieces will instantly fall from the top to bottom. 

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
