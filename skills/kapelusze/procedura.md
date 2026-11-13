# Analiza problemu sześcioma kapeluszami

## Kiedy używać

- **Ocena ważnego pomysłu albo propozycji**, np. nowa usługa, zmiana ceny, nowy kanał sprzedaży.
- **Nowy problem bez gotowego rozwiązania**, np. „spada liczba zapytań”, „zespół nie wyrabia się z realizacją”.
- **Spór**, w którym każdy broni swojego zdania, a rozmowa krąży w kółko.
- **Zdarzenie, które już się stało**, np. ruch konkurencji, zmiana przepisów, utrata dużego klienta.
- **Ostatnia kontrola gotowego planu** przed wdrożeniem.

**Kiedy nie używać:**
- przy prostych decyzjach liczbowych, które da się policzyć (np. czy wynik testu jest rozstrzygnięty);
- w sprawach prawnych, które zawsze trafiają do człowieka.

Gdy firma ma już własny sposób podejmowania danej decyzji (progi, wzór, regułę), kapelusze go **uzupełniają**, a nie zastępują. Dane i progi bierzesz z tej reguły, a kapeluszami przechodzisz po wariantach.

## Dane wejściowe

- **Opis problemu od człowieka:** co się dzieje, czego chce, do kiedy potrzebna jest decyzja. Emocje w opisie są w porządku, bo moderator z nich korzysta.
- **Pliki firmy**, jeśli człowiek je ma: strategia (gdzie gramy, czego nie robimy), cele, liczby firmy, opis klientów, historia prób i testów. Brak plików nie blokuje analizy: biały wypisuje, czego brakuje, a rekomendacja jest wtedy oznaczona jako wstępna.

## Wybór trybu pracy

Tryb wybiera człowiek na starcie. Sekwencje kapeluszy, limity i pułapki są wspólne dla wszystkich trybów.

| Tryb | Kiedy | Kto myśli | Co widać |
|---|---|---|---|
| **Prowadzony** | Człowiek chce sam przemyśleć decyzję i zrozumieć, skąd bierze się wynik | Człowiek. Moderator pyta pod każdym kapeluszem, przenosi punkty pod właściwy kolor i dopisuje swoje dopiero po nim | Po każdej rundzie tablica: kapelusze, braki, kierunek, następny krok |
| **Narada** | Decyzję podejmuje zespół na spotkaniu, także z telefonem na stole w trybie głosowym | Zespół. Moderator ogłasza kapelusze, zapisuje i pilnuje kierunku | W trakcie krótkie zdania, po spotkaniu podsumowanie na piśmie z tablicą |
| **Auto** | Człowiek chce dostać gotową analizę do oceny | Kapelusze | Tablica i pytanie w pauzie (można dopytać albo dodać), potem zamknięcie z tablicą końcową |

W trybie auto są dwa sposoby wykonania:

| Sposób | Kiedy | Jak działa | Ile odpowiedzi |
|---|---|---|---|
| **Szybko** | Decyzja mała, odwracalna, w jednej dziedzinie. Także każda decyzja w czacie, gdzie nie ma osobnych agentów, albo na prośbę człowieka | Jeden agent przechodzi po kolei przez kapelusze z sekwencji, za każdym razem zakładając kolejną kartę. Na ekranie przed pauzą: każdy krok jednym zdaniem, tablica i pytanie o czerwony człowieka | 1 wiadomość do pauzy, do ok. 400 słów |
| **Z agentami** | Decyzja średnia albo sporna | Osobny agent na każdy kapelusz i moderator. Każdy widzi mapę z wcześniejszych kroków | 5–8 |

## Wybór sekwencji

Każda sekwencja zaczyna się i kończy niebieskim. Zadania kapeluszy w nawiasach odpowiadają zadaniom z kart.

| Sytuacja | Sekwencja | Uwagi |
|---|---|---|
| **Ocena pomysłu** | 🔵 → ⚪ → 🟡 (ocena) → ⚫ (ocena) → 🟢 (omijanie przeszkód) → 🔴 → 🔵 | Żółty przed czarnym, żeby pomysł nie zginął przed obejrzeniem wartości |
| **Nowy problem** | 🔵 → ⚪ → 🟡 (propozycje) → 🟢 (alternatywy) → 🔵 porządkuje listę → dla max 3 opcji: 🟡 → ⚫ → 🔴 → 🔵 | Najpierw zwykłe propozycje, potem świeże. Oceniasz dopiero po zebraniu opcji |
| **Temat budzi emocje / spór** | 🔵 → 🔴 → ⚪ → 🟡 → ⚫ → 🟢 → 🔵 | Emocje wychodzą na początku i potem nie mieszają się z argumentami. Przy sporze moderator stosuje „w jakich okolicznościach każdy ma rację” |
| **Zdarzenie, które już się stało** | 🔵 → ⚪ → 🔴 → 🟡 (okazje) → ⚫ → 🟢 (okazja) → 🔵 | Obok strat szukasz okazji |
| **Kontrola gotowego planu** | 🔵 → ⚫ (projektowanie) → 🟡 (wzmocnienie) → 🟢 (omijanie przeszkód, jeśli trzeba) → 🔵 | Gdy decyzja „idziemy” już zapadła |

## Krok po kroku (tryb auto)

Przebieg trybu prowadzonego i narady jest w `tryby/prowadzony.md` i `tryby/narada.md`. Kolejność kapeluszy, reguły i pułapki z tego pliku obowiązują także tam.

1. **Człowiek podaje problem.** Wystarczy zdanie albo dwa. Przykład: „Przeanalizuj kapeluszami: czy wprowadzić abonament na obsługę social mediów zamiast rozliczeń za projekt”. Może też od razu wskazać tryb pracy.
2. **🔵 Otwarcie.** Moderator pisze według karty: skupienie, 2–3 definicje problemu, oczekiwany wynik, dane, tryb i program. Przy decyzji średniej lub dużej **pokazuje program człowiekowi i czeka na „ok”** albo poprawkę. Przy małej od razu idzie dalej.
3. **Kapelusze po kolei.** Każdy agent dostaje:
   - skupienie i definicję problemu z otwarcia,
   - zadanie swojego kapelusza (np. „⚫ tryb: ocena”),
   - mapę z wcześniejszych kapeluszy,
   - przedmiot decyzji (czym jest produkt i czego nie da się pokazać szybko),
   - pliki firmy wskazane przez moderatora, jeśli są,
   - swoją kartę.

   Odpowiada w formacie karty i robi jej samokontrolę.
4. **🔵 Między kapeluszami** (krótko, tylko gdy trzeba):
   - punkty spoza kierunku przenosi pod właściwy kolor;
   - spory zapisuje jako oba zdania i sprawdza, czy biały je rozstrzyga;
   - pilnuje przedmiotu decyzji wobec każdego kapelusza, także żółtego;
   - po zielonym porządkuje propozycje z żółtego i zielonego. Do pełnej oceny najwyżej 3: zgodne z przedmiotem decyzji, różne zasadą, co najmniej jedna od zielonego (jeśli zielony dał coś zgodnego z przedmiotem). Sprzeczne z przedmiotem decyzji idą od razu do plonu z dopiskiem dlaczego. Reszta też idzie do plonu, a te, do których warto wrócić, z dopiskiem „do rozwinięcia”. W tej analizie „do rozwinięcia” nie wraca do oceny, chyba że człowiek poprosi o to w pauzie;
   - gdy kapelusz nie dał wyniku, zapisuje to i proponuje kolejny krok.
5. **🔴 Czerwony człowieka.** Gdy mapa jest gotowa, moderator pokazuje warianty i pyta człowieka bez uzasadniania: „jak się czujesz z wariantem A, B i C, w jednym-dwóch słowach?”. W tym samym pytaniu prosi o to, na czym człowiekowi najbardziej zależy, i o brakujące dane, które może podać od ręki. To idzie **po** agentach, żeby zdanie szefa nie ustawiło całej analizy. Poprawki człowieka do mapy (np. „ten pomysł nie pasuje do produktu”) moderator wpisuje jako dane i aktualizuje mapę przed zamknięciem. Odrzucony pomysł znika z rekomendacji, kroków i testu. W plonie zostaje z dopiskiem „odrzucone przez Ciebie: powód”.
6. **🔵 Zamknięcie.** Według karty:
   - mapa z kolorami źródeł,
   - przegląd: co ustalone, co sporne, czego nie wiemy,
   - kryteria wyboru ze strategii i celów (albo z tego, na czym człowiekowi zależy),
   - rekomendacja w 3 aktach, pewność i brakujące dane,
   - następne kroki (osoby i terminy z danych człowieka albo „do ustalenia”) i najtańszy test,
   - plon, zawsze i krótko.
7. **Zapis.** W Claude Code i Cowork pełna analiza trafia do pliku `analizy/RRRR-MM-DD – <temat>.md`: decyzja, najtańszy test i plon zielonego, czyli pomysły nieocenione, kierunki i półgotowe pomysły. Tak samo przy pracy szybkiej. Obok zapisujesz tablicę jako plik HTML. W czacie pełne odpowiedzi kapeluszy pokazujesz na życzenie, a plon jest w zamknięciu.

## Reguły i progi

- **Najwyżej 3 opcje do pełnej oceny** (żółty + czarny dla każdej). Resztę zapisujesz w plonie.
- **Biały jako podprogram:** gdy w trakcie brakuje danych, wolno wrócić do białego, ale tylko po konkretną brakującą liczbę. Gdy tę liczbę da się znaleźć na zewnątrz (ceny konkurencji, opinie, popyt), moderator proponuje research, robi go po zgodzie człowieka i dopisuje wnioski pod biały ze źródłem.
- **Tablica po każdej rundzie** w trybie prowadzonym, w pauzie i na końcu w auto, w podsumowaniu narady (`tablica.md`).
- **Brak kluczowych danych** oznacza, że rekomendacja jest wstępna i najbliższym krokiem jest zdobycie tych danych.
- **Czerwony agentów** to kilka linijek, a nie osobny raport.
- **Dla ludzi na spotkaniu:** ok. 1 minuta na osobę na kapelusz (4 osoby to 4 minuty), czerwony to 1 minuta dla wszystkich. Przy zielonym, żółtym i czarnym najpierw 1–2 minuty na własne notatki.

## Pułapki

- **Kapelusz jako etykieta człowieka albo agenta** („Ty jesteś od czarnego”). Wszyscy noszą ten sam kapelusz w tym samym czasie.
- **Czarny przed żółtym przy ocenie pomysłu.** Wtedy pomysł przepada, zanim ktoś zobaczy jego wartość.
- **Moderator, który uśrednia albo ogłasza zgodę**, której nie było.
- **Ocenianie wszystkich pomysłów zielonego.** Wychodzi z tego 30 odpowiedzi, których nikt nie przeczyta. Porządkujesz i wybierasz najwyżej trzy.
- **Czerwony człowieka na początku.** Ustawia całą analizę pod zdanie szefa.
- **Brak zamknięcia:** dobra mapa bez decyzji, bez kroków i bez zapisu.
- **Wymuszanie decyzji, której nie widać.** Gdy mapa nie daje wyboru, moderator nazywa powód (brak danych, sprzeczne wartości, niepewna przyszłość), szuka drogi obejmującej obie opcje, a gdy jej nie ma, oddaje wybór czerwonemu człowieka albo wyznacza nowe skupienie. Ostatecznie każda decyzja jest czerwona.
- **Zielony albo żółty, który nie zna produktu.** Bez opisu przedmiotu decyzji na otwarciu agenci proponują rzeczy sprzeczne z tym, czym produkt naprawdę jest (np. „pokaz w 3 minuty” dla usługi, która wymaga przepracowania całej firmy). Żółty robi to nawet wtedy, gdy zna produkt, bo „typowa taktyka z branży” wygląda na bezpieczną. Moderator odsiewa takie propozycje przed pełną oceną.
- **Kapelusze zamiast danych.** Analiza nie zastąpi liczb. Gdy biały mówi, że czegoś nie wiemy, pierwszym krokiem jest to sprawdzić.

## Format wyniku

Wynik to otwarcie i zamknięcie w formacie z karty niebieskiego, a pomiędzy nimi praca kapeluszy w formatach z ich kart.

**Co człowiek widzi** (tryb auto, oba sposoby wykonania):
1. Otwarcie w 3 liniach (skupienie, tryb, program). Przy decyzji średniej lub dużej z pytaniem o „ok”.
2. Przed pauzą: każdy krok kapelusza jednym zdaniem („Zakładam biały → 8 faktów, 3 luki.”), tablica i pytanie o czerwony człowieka w trzech częściach. Tekst do ok. 400 słów. Człowiek może w tym miejscu coś dopytać albo dodać.
3. Po pauzie zamknięcie: tablica, rekomendacja w 3 aktach, pewność, brakujące dane, następne kroki, najtańszy test i plon.

Pełne odpowiedzi kapeluszy zapisujesz w pliku analizy (Claude Code, Cowork) albo pokazujesz na życzenie (czat).

## Kiedy decyduje człowiek

- Zawsze przy cenie, ofercie widocznej dla klientów, dużym budżecie, strategii i sprawach prawnych. Agent daje mapę i rekomendację, a decyzję podejmuje człowiek.
- Gdy definicja problemu zmienia całą analizę, człowiek wybiera ją na otwarciu.
- Czerwony człowieka jest częścią wyboru, a nie dodatkiem.
