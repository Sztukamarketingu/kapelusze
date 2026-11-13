# Kapelusze – analiza decyzji z AI

**Narada kręci się w kółko, bo każdy myśli w innym kierunku naraz. Tu wszyscy myślą w tym samym.**

Dodatek do Claude'a, który prowadzi Twój problem, pomysł albo spór przez metodę sześciu kapeluszy myślowych Edwarda de Bono. Pod każdym kapeluszem patrzysz na sprawę z jednej strony: fakty, korzyści, ryzyka, nowe pomysły, emocje. Moderator w niebieskim kapeluszu układa kolejność, pilnuje kierunku i pokazuje, w jakim miejscu jesteś i czego brakuje.

## Trzy tryby pracy

Na starcie moderator pyta, jak chcesz pracować.

| Tryb | Jak to działa | Kiedy |
|---|---|---|
| **Prowadź mnie** | Moderator zadaje pytania pod każdym kapeluszem, a myślisz Ty. Swoje punkty dopisuje dopiero po Tobie i możesz je odrzucić. Po każdej rundzie pokazuje tablicę. | Chcesz sam przemyśleć decyzję i wiedzieć, skąd bierze się wynik. |
| **Narada** | Telefon leży na stole, a moderator prowadzi rozmowę zespołu głosem: „teraz żółty”, „to ryzyko, zapisuję pod czarny”, „potrzebuję tu białego”. Po spotkaniu dostajesz podsumowanie na piśmie. | Decyzję podejmuje kilka osób przy jednym stole. |
| **Zrób sam** | Kapelusze robią analizę, a Ty odpowiadasz na jedno pytanie przed rekomendacją. | Chcesz dostać gotową mapę do oceny. |

Tryb możesz podać od razu: „prowadź mnie przez kapelusze”, „narada w kapeluszach”, „przeanalizuj kapeluszami”.

## Jak wygląda tryb prowadzony

1. Piszesz: „Prowadź mnie przez kapelusze: czy dodać kursy online obok zajęć stacjonarnych”.
2. Moderator zadaje najwyżej 4 pytania: jaka decyzja, czym jest to, o czym decydujesz, co już wiesz, do kiedy.
3. Pokazuje program (które kapelusze i w jakiej kolejności) i czeka na Twoje „ok”.
4. Pod każdym kapeluszem pyta, a Ty odpowiadasz:

| Kapelusz | O co pyta |
|---|---|
| ⚪ Biały | co wiemy na pewno, czego nie wiemy, jak to sprawdzić |
| 🟡 Żółty | co w tym wartościowego, dla kogo i na czym to opierasz |
| ⚫ Czarny | co może pójść źle i które słowa odstraszą klienta |
| 🟢 Zielony | jak jeszcze można to zrobić i jak ominąć przeszkody |
| 🔴 Czerwony | jak się czujesz z każdym wariantem, bez uzasadniania |
| 🔵 Niebieski | moderator: program, porządek, tablica, następny krok |

5. Gdy pomysłów jest więcej, moderator prosi: „wybierz trzy i nimi się zajmujemy”. Reszta trafia do plonu.
6. **Po każdej rundzie tablica.** Widzisz na niej każdą opcję w każdym kapeluszu, pola puste i słabe, listę braków oraz proponowany kierunek. W Claude pojawia się jako artefakt, w Claude Code jako plik HTML w folderze `analizy/`.
7. Braki są w dwóch grupach. O dane z Twojej firmy moderator prosi Ciebie. To, co da się znaleźć na zewnątrz (ceny konkurencji, opinie, popyt), proponuje sprawdzić sam i po Twojej zgodzie dopisuje wnioski ze źródłem.
8. Na końcu decydujesz Ty. Dostajesz następne kroki i najtańszy test.

Przykładowe przebiegi trzech trybów: [`skills/kapelusze/przyklad.md`](skills/kapelusze/przyklad.md).

## Narada z telefonem na stole

1. Wgraj dodatek do Claude (instrukcja niżej, „Claude w przeglądarce i aplikacji”).
2. W aplikacji Claude na telefonie zacznij nową rozmowę i napisz „narada w kapeluszach”. Potem włącz tryb głosowy i połóż telefon na stole.
3. Powiedz, nad czym pracujecie, ile osób jest przy stole i ile macie czasu.
4. Rozmawiajcie normalnie. Moderator odzywa się po każdej pauzie, zwykle jednym zdaniem.
5. Do moderatora zwracacie się słowem „niebieski”: „niebieski, dalej”, „niebieski, co mamy?”, „niebieski, dorzuć”, „niebieski, cisza”, „niebieski, kończymy”.
6. Po spotkaniu napisz „podsumuj na piśmie”. Dostaniesz tablicę, decyzję, kroki z osobami i terminami oraz plon.

Moderator nie rozróżnia głosów, więc zapisuje punkty, a nie ich autorów. Tryb głosowy działa turami: moderator słyszy to, co padło od poprzedniej pauzy.

**W Claude Code i Cowork** w trybie „zrób sam” każdy kapelusz robi osobny agent, a analiza i tablica zapisują się w folderze `analizy/`. **W czacie** jeden agent zakłada kolejne kapelusze po kolei. Wynik ma ten sam format.

## Instalacja

### Claude Code

W terminalu, w Claude Code, wpisz:

```
/plugin marketplace add Sztukamarketingu/kapelusze
/plugin install kapelusze@kapelusze
```

Uwaga: w aplikacji desktop slash `/plugin` nie działa w oknie rozmowy. Otwórz wbudowany terminal, uruchom w nim `claude` i wpisz te dwie komendy tam.

Potem napisz „prowadź mnie przez kapelusze” albo `/kapelusze`.

### Claude w przeglądarce i aplikacji (claude.ai)

1. Pobierz plik `kapelusze.zip` z zakładki **Releases** tego repozytorium.
2. W Claude otwórz **Customize → Skills**, kliknij **+ Add → Upload skill** i wskaż pobrany plik.
3. W nowej rozmowie napisz „prowadź mnie przez kapelusze”.

### ChatGPT

Instrukcja wkrótce.

## Kiedy używać

- Ocena ważnego pomysłu: nowa usługa, zmiana ceny, nowy kanał sprzedaży.
- Nowy problem bez gotowego rozwiązania.
- Spór w zespole, który krąży w kółko.
- Zdarzenie, które już się stało: ruch konkurencji, utrata dużego klienta.
- Ostatnia kontrola gotowego planu przed wdrożeniem.

## Czego ten dodatek nie robi

- Nie podejmuje decyzji za Ciebie. Cena, oferta, budżet, strategia i sprawy prawne zostają Twoją decyzją.
- Nie wymyśla liczb o Twojej firmie. Czego nie wie, wpisuje na listę luk.
- Nie zastąpi danych. Gdy biały kapelusz mówi „nie wiemy”, pierwszym krokiem jest to sprawdzić.

## Więcej

Metody krok po kroku uczy mini kurs w Kuźni Sztuki Marketingu, a o programie „AI w biznesie i marketingu” przeczytasz na [sztukamarketingu.pl](https://sztukamarketingu.pl).

## Dla autorów zmian

Treść kapeluszy leży raz, w `skills/kapelusze/karty/`. Pliki w `agents/` generuje `./zbuduj.sh`, który pakuje też `dist/kapelusze.zip`. Poprawiasz kartę, uruchamiasz skrypt. Przebieg trybów jest w `skills/kapelusze/tryby/`, a szablon tablicy w `skills/kapelusze/tablica.html` (zmieniasz w nim tylko blok danych).

## Licencja

MIT – możesz używać, zmieniać i udostępniać dalej. Autor: Tomasz Szwecki, Sztuka Marketingu.
