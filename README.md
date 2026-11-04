# Kapelusze – analiza decyzji z AI

**Narada kręci się w kółko, bo każdy myśli w innym kierunku naraz. Tu wszyscy myślą w tym samym.**

Dodatek do Claude'a, który przeprowadza Twój problem, pomysł albo spór przez metodę sześciu kapeluszy myślowych Edwarda de Bono. Opisujesz decyzję, a kolejne kapelusze patrzą na nią z jednej strony naraz: fakty, korzyści, ryzyka, nowe pomysły, emocje. Moderator w niebieskim kapeluszu pilnuje porządku, pyta Cię o zdanie przed rekomendacją i kończy mapą, następnymi krokami oraz najtańszym testem.

## Jak to wygląda

1. Piszesz: „Przeanalizuj kapeluszami: czy dodać kursy online obok zajęć stacjonarnych”.
2. Moderator zadaje najwyżej 4 pytania: jaka decyzja, czym jest to, o czym decydujesz, co już wiesz, do kiedy.
3. Pokazuje program (które kapelusze i w jakiej kolejności) i czeka na Twoje „ok”.
4. Kapelusze pracują po kolei:

| Kapelusz | Co robi |
|---|---|
| ⚪ Biały | fakty i luki: co wiemy na pewno, czego nie wiemy, jak to sprawdzić |
| 🟡 Żółty | korzyści z uzasadnieniem i oceną szansy |
| ⚫ Czarny | ryzyka, dopasowanie do firmy, słowa, które mogą odstraszyć klienta |
| 🟢 Zielony | nowe pomysły i sposoby na ominięcie przeszkód |
| 🔴 Czerwony | wyczucie i przewidywane reakcje ludzi, bez uzasadniania |
| 🔵 Niebieski | moderator: otwarcie, porządek, zamknięcie |

5. **Pauza na Twoje zdanie.** Moderator pyta, jak się czujesz z każdym wariantem, na czym Ci najbardziej zależy i jakie dane możesz dopisać. Twoje poprawki zmieniają mapę: odrzucony pomysł znika i nikt go nie broni.
6. Wynik do przeczytania w 5 minut: mapa w tabeli, rekomendacja, pewność, następne kroki i najtańszy test.

Przykładowy przebieg: [`skills/kapelusze/przyklad.md`](skills/kapelusze/przyklad.md).

**W Claude Code i Cowork** każdy kapelusz robi osobny agent, a pełna analiza zapisuje się w pliku `analizy/`. **W czacie** jeden agent zakłada kolejne kapelusze po kolei. Wynik ma ten sam format.

## Instalacja

### Claude Code

W terminalu, w Claude Code, wpisz:

```
/plugin marketplace add Sztukamarketingu/kapelusze
/plugin install kapelusze@kapelusze
```

Uwaga: w aplikacji desktop slash `/plugin` nie działa w oknie rozmowy. Otwórz wbudowany terminal, uruchom w nim `claude` i wpisz te dwie komendy tam.

Potem napisz „przeanalizuj kapeluszami” albo `/kapelusze`.

### Claude w przeglądarce i aplikacji (claude.ai)

1. Pobierz plik `kapelusze.zip` z zakładki **Releases** tego repozytorium.
2. W Claude otwórz **Customize → Skills**, kliknij **+ Add → Upload skill** i wskaż pobrany plik.
3. W nowej rozmowie napisz „przeanalizuj kapeluszami”.

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

Treść kapeluszy leży raz, w `skills/kapelusze/karty/`. Pliki w `agents/` generuje `./zbuduj.sh`, który pakuje też `dist/kapelusze.zip`. Poprawiasz kartę, uruchamiasz skrypt.

## Licencja

MIT – możesz używać, zmieniać i udostępniać dalej. Autor: Tomasz Szwecki, Sztuka Marketingu.
