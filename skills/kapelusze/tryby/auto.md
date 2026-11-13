# Tryb auto – kapelusze robią analizę same

Człowiek opisuje decyzję, a kapelusze zakładają agenci. Traktuj ich jak **członków zespołu na naradzie**: każdy mówi pod swoim kapeluszem, Ty prowadzisz i zapisujesz ich punkty na tablicy, a człowiek jest szefem, który widzi tablicę, może coś dopytać albo dodać i podejmuje decyzję. Wywiad, dane i otwarcie masz już za sobą (`SKILL.md`, kroki 1–2).

## Dwa sposoby wykonania, jedno źródło kart

Sprawdź, czy możesz uruchamiać osobnych agentów (narzędzie Agent albo Task i agenci `kapelusz-bialy`, `kapelusz-czerwony`, `kapelusz-zolty`, `kapelusz-czarny`, `kapelusz-zielony`; w pluginie mogą mieć przedrostek `kapelusze:`).

- **Możesz (Claude Code, Cowork): z agentami.** Każdy kapelusz robi osobny agent. Ty zostajesz w niebieskim.
- **Nie możesz (claude.ai, aplikacja Claude, ChatGPT): szybko.** Sam zakładasz kolejne karty z `karty/`, jedną po drugiej. Każdy krok zaczynasz wyraźnie: *„Zdejmuję niebieski, zakładam biały.”* Myślisz wtedy tylko według tej karty i jej formatu.

Powiedz to jednym zdaniem i idź dalej, np. *„Pracuję szybko: sam zakładam kolejne kapelusze, wynik ma ten sam format.”* Przy małej, odwracalnej decyzji możesz pracować szybko także w Claude Code. Gdy człowiek sam o to prosi przy decyzji średniej albo dużej, zgódź się i zaznacz to w otwarciu. Zapis w Claude Code robisz wtedy tak samo jak z agentami (krok 4). Wynik w obu sposobach ma ten sam format.

## 1. Kapelusze po kolei

Idziesz według programu. Każdy kapelusz (agent albo Ty po zmianie karty) dostaje:

- skupienie i przyjętą definicję problemu,
- przedmiot decyzji,
- zadanie swojego kapelusza (np. „⚫ tryb: ocena”, „🟢 zadanie: omijanie przeszkód”),
- mapę z wcześniejszych kroków (skrót punktów z kolorami),
- dane od człowieka i pliki, które wskazałeś.

Agentowi napisz też, że blok „Pytania do człowieka” z karty go nie dotyczy.

**Równolegle** uruchamiasz tylko kroki niezależne, np. żółty i czarny dla różnych opcji po ich wybraniu. Żółty i czarny dla tej samej opcji idą po kolei: najpierw żółty.

Między kapeluszami (krótko):
- punkty spoza kierunku (ryzyko pod żółtym, ocena pod zielonym) **przenosisz pod właściwy kolor**, nie wyrzucasz;
- spór zapisujesz jako oba zdania;
- **pilnujesz przedmiotu decyzji wobec każdego kapelusza, także żółtego.** Propozycja, która obiecuje szybszy efekt, niż daje produkt (pokaz, „audyt w 15 minut”), nie idzie dalej jako opcja;
- po zielonym zostawiasz **najwyżej 3 opcje** do pełnej oceny. Wybierasz je tak:
  1. opcje sprzeczne z przedmiotem decyzji idą **od razu do plonu** z dopiskiem dlaczego (np. „sprzeczne z produktem: obiecuje efekt w kwadrans”);
  2. opcje **różnią się zasadą**, nie szczegółem;
  3. **co najmniej jedna pochodzi od zielonego**, jeśli zielony dał coś zgodnego z przedmiotem decyzji.

  Resztę dajesz do **plonu**. Te, do których warto wrócić, z dopiskiem „do rozwinięcia”.

**Braki w trakcie.** Jeśli kapelusz zgłosi brak danych, bez których jego punkt jest tylko spekulacją, zbierasz takie braki i pytasz o nie **jedną wiadomością** w pauzie (część 3 pytania). Wyjątek: brak tak duży, że dalsza analiza nie ma sensu (np. nie wiadomo, co jest sprzedawane). Wtedy zatrzymaj się od razu i zapytaj. Braki „do sprawdzenia” zgłaszasz w pauzie jako propozycję researchu (`SKILL.md`, „Braki”).

**Co człowiek widzi, gdy pracujesz szybko.** Kapelusze pracują w pełni według kart. Na ekranie przed pauzą jest jednak tylko:
- każdy krok kapelusza jednym zdaniem, np. *„Zakładam biały → 8 faktów, 3 luki.”*;
- **tablica** w wersji tekstowej (`tablica.md`) i jako artefakt albo plik HTML;
- **pytanie w trzech częściach** z kroku 2.

Razem do ok. 400 słów, nie licząc wersji graficznej. Pełne odpowiedzi kapeluszy trafiają do pliku analizy (Claude Code, Cowork) albo pokazujesz je na życzenie (czat).

## 2. Pauza: czerwony człowieka

**Tu musisz się zatrzymać.** Nie piszesz rekomendacji, dopóki człowiek nie odpowie. Pokaż **tablicę** według `tablica.md`: wersję tekstową w rozmowie oraz artefakt albo plik HTML. Punkty agentów mają źródło `agent` (albo nazwę roli agenta), czerwony agentów też ma wiersz, a pola bez danych są oznaczone jako słabe. W „Decyzjach do tej pory” wpisz to, co już postanowiono: przyjętą definicję problemu i opcje wybrane do oceny. Kierunku jeszcze nie podajesz. Potem zadaj **jedno pytanie w trzech częściach**. Tekst wiadomości ma do ok. 400 słów:

1. Jak się czujesz z każdym wariantem? Jedno-dwa słowa, bez uzasadniania.
2. Na czym Ci w tej decyzji najbardziej zależy?
3. Jakie brakujące dane możesz podać od ręki? (wypisz luki z białego oraz wszystkie „Brakuje:” z żółtego i czarnego; gdy w danych nie ma terminów ani osób do kroków, dopytaj: „do kiedy chcesz to wiedzieć?”, „kto to zrobi?”). Jeśli coś da się sprawdzić na zewnątrz, dodaj propozycję: „mogę sprawdzić X, chcesz?”.

Na końcu dodaj jedno zdanie: *„Możesz też coś dopytać albo dodać, zanim zaproponuję wybór.”* Człowiek ma wtedy do dyspozycji:

| Człowiek pisze | Co robisz |
|---|---|
| `dopytaj czarny o …` (albo inny kolor) | wracasz do tego kapelusza z konkretnym pytaniem i dopisujesz odpowiedź na tablicy |
| `dodaj: …` | wpisujesz jego punkt pod właściwy kolor ze źródłem `ty` |
| `to się nie zgadza: …` | poprawiasz punkt, a starą wersję usuwasz |
| `sprawdź to` | research dla wskazanego braku (`SKILL.md`, „Braki”) |
| `pokaż pełną odpowiedź [kolor]` | pokazujesz całą odpowiedź agenta |
| `prowadź mnie dalej` | przechodzisz do `tryby/prowadzony.md` z tablicą, która już jest |

Po każdej takiej zmianie pokazujesz odświeżoną tablicę i wracasz do pytania w trzech częściach, jeśli człowiek jeszcze na nie nie odpowiedział.

Odpowiedź człowieka to dane:
- poprawka mapy („to nie pasuje do produktu”, „klienci boją się tego słowa”, „ta osoba nie ma czasu”) **aktualizuje mapę**; odrzucony pomysł znika z rekomendacji, kroków i testu, a Ty **go nie bronisz**. W plonie zostaje z dopiskiem „odrzucone przez Ciebie: [powód]”;
- to, na czym człowiekowi zależy, staje się **kryterium wyboru**;
- nowe liczby trafiają pod biały.

Gdy człowiek pisze „pomiń” albo „decyduj sam”, zaznacz w zamknięciu, że rekomendacja powstała bez jego czerwonego.

## 3. Zamknięcie w wersji skróconej

Do przeczytania w 5 minut:

1. **Otwarcie w 3 liniach:** skupienie · tryb · program.
2. **Tablica końcowa** według `tablica.md`: ta sama co w pauzie, uzupełniona o czerwony człowieka, jego poprawki, kierunek i „Decyzje do tej pory” (co odrzucił i dlaczego). W rozmowie wersja tekstowa, do tego ten sam artefakt albo plik HTML, odświeżony. Spory jako oba zdania. Zaznacz, co się zmieniło po odpowiedzi człowieka.
3. **Rekomendacja w 3 aktach:** sytuacja → komplikacja → „dlatego proponuję…” (co, dlaczego, jak) z jawnymi kryteriami.
4. **Pewność:** wysoka / średnia / niska i dlaczego.
5. **Brakujące dane.**
6. **Następne kroki** (co, kto, do kiedy) i **najtańszy test**. Osoby i terminy bierzesz z danych człowieka. Gdy ich nie ma, piszesz „kto: do ustalenia”, „do kiedy: do ustalenia”. Nie wymyślasz dat ani wyliczeń typu „zostały 2 miesiące”, chyba że wynikają z dat podanych przez człowieka. Test składasz z luk białego i opcji kapeluszy. Próg testu (np. ile zapisów) bierzesz od człowieka albo piszesz „próg do ustalenia”.
7. **Plon, zawsze, krótko:** pomysły nieocenione, „do rozwinięcia”, odsiane przez Ciebie (z dopiskiem dlaczego) i odrzucone przez człowieka (z dopiskiem „odrzucone przez Ciebie: [powód]”). Odrzuconych nie ma w rekomendacji ani w krokach.

## 4. Zapis

- **Claude Code, Cowork (z agentami i szybko):** zapisz pełną analizę (otwarcie, pełne odpowiedzi kapeluszy, czerwony człowieka, zamknięcie, plon) do `analizy/RRRR-MM-DD – <temat>.md` w folderze człowieka, a obok tablicę jako `analizy/RRRR-MM-DD – <temat> – tablica.html`. Podaj ścieżki jednym zdaniem.
- **Czat:** zaproponuj pełne odpowiedzi kapeluszy na życzenie, jedną wiadomością. Plon jest już w zamknięciu.

## Samokontrola trybu auto

- [ ] Przed pauzą na ekranie są tylko kroki jednym zdaniem, tablica i pytanie (tekst do ok. 400 słów).
- [ ] Człowiek dostał w pauzie możliwość dopytania i dodania punktów, a tablica została po tym odświeżona.
- [ ] Rekomendacja powstała po odpowiedzi człowieka albo ma dopisek, że bez jego czerwonego.
- [ ] W pełnej ocenie są najwyżej 3 opcje, zgodne z przedmiotem decyzji.
- [ ] Zamknięcie ma tablicę, kroki, test i plon.
