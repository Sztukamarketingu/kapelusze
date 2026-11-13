# Tablica – podsumowanie graficzne po rundzie

Tablica pokazuje na jednym ekranie, jak pomysł wygląda w każdym kapeluszu, w jakim miejscu programu jesteśmy, czego brakuje i dokąd to zmierza. Człowiek ma po niej wiedzieć, co jest następnym krokiem.

**Runda** to jedno przejście przez kapelusze z programu: dla jednego pomysłu albo dla wybranych opcji (najwyżej trzech).

## Kiedy ją pokazujesz

- **Tryb prowadzony:** po każdej rundzie oraz na komendę `tablica`.
- **Tryb auto:** w pauzie, zanim powstanie rekomendacja, oraz w zamknięciu. Człowiek widzi na niej pracę agentów tak, jak widziałby notatki zespołu, i może coś dopytać albo dodać.
- **Narada:** w podsumowaniu na piśmie po spotkaniu. W trakcie rozmowy głosowej tablicy nie ma, jest „niebieski, co mamy?”.

## Co zawiera

1. **Gdzie jesteśmy** – program z zaznaczeniem, co zrobione, co teraz, co przed nami i co zostało pominięte.
2. **Kapelusze** – wiersz na kapelusz (biały, żółty, czarny, zielony, czerwony), przy 2–3 opcjach kolumna na opcję. W polu 2–4 najważniejsze punkty, każdy w jednym krótkim zdaniu.
3. **Stan pola:**
   - `pelne` – kapelusz był, punkty stoją na danych albo na doświadczeniu człowieka;
   - `slabe` – kapelusz był, ale punkty to domysły albo jest ich za mało, żeby decydować;
   - `puste` – tego kapelusza przy tej opcji jeszcze nie było.
4. **Źródło punktu:** `ty` (człowiek), `zespol` (narada), `agent` (agent kapelusza w trybie auto), `ai` (Twój dopisek), `research` (sprawdzone na zewnątrz, w treści podaj źródło). Gdy kapelusz zakłada agent z konkretną rolą, wpisz nazwę roli zamiast `agent`, np. `"zr": "dyrektor finansowy"`. Tablica pokaże ją tak, jak ją wpiszesz.
5. **Czego brakuje** – osobno „dane od Ciebie” i „do sprawdzenia (research)”.
6. **Kierunek** – Twoja propozycja w 1–2 zdaniach i to, co ją podważa. Gdy pól pustych albo słabych jest za dużo, kierunku nie podajesz (`"kierunek": null`), a tablica mówi, że jest za wcześnie.
7. **Decyzje do tej pory** – co już zostało postanowione po drodze: która definicja problemu, które trzy opcje idą do oceny, co człowiek odrzucił i dlaczego, a w zamknięciu decyzja końcowa. Tylko decyzje, które naprawdę padły.
8. **Następny krok** – jedno zdanie: kolejna runda, uzupełnienie danych, research, czerwony człowieka albo zamknięcie.
9. **Sporne** – dwa zdania, które się wykluczają, i to, co by je rozstrzygnęło.
10. **Plon** – pomysły odłożone.

Biały zwykle dotyczy całej sprawy, więc ma jedno pole na wszystkie opcje: w danych podajesz wtedy jedno pole w `pola`. Pod pozostałymi kapeluszami punkty, które padły, zanim pojawiły się opcje, albo nie dotyczą żadnej z nich, wpisujesz w `ogolne` tego wiersza. Nie dopisujesz ich na siłę do jednej z opcji. Czerwony wypełniasz tylko słowami człowieka albo zespołu.

Tablica niczego nie wygładza. Spór zapisujesz jako dwa punkty obok siebie. Puste pole zostaje puste.

## Jak ją pokazujesz

Zawsze **dwie rzeczy naraz**: wersja tekstowa w rozmowie oraz, tam gdzie się da, wersja graficzna z szablonu `tablica.html`.

### Wersja graficzna

Bierzesz `tablica.html` i podmieniasz **wyłącznie** zawartość bloku `<script id="dane" type="application/json">`. Stylów i skryptu nie ruszasz.

- **claude.ai i aplikacja Claude:** pokaż jako artefakt HTML o nazwie „Tablica kapeluszy”. Po kolejnej rundzie i po każdej zmianie danych na tablicy (nowa liczba, poprawka, wynik researchu) aktualizujesz ten sam artefakt.
- **Claude Code i Cowork:** zapisz jako `analizy/RRRR-MM-DD – <temat> – tablica.html` w folderze człowieka i podaj ścieżkę. Po kolejnej rundzie nadpisujesz ten sam plik.
- **Bez artefaktów i bez plików (np. ChatGPT bez canvas):** zostaje sama wersja tekstowa.

Pola danych:

```
temat      – skupienie z otwarcia, jedno zdanie
runda      – numer rundy
data       – RRRR-MM-DD; gdy nie znasz dzisiejszej daty, pomiń to pole
tryb       – "prowadzony" | "narada" | "auto"
program    – lista kroków: {"k": kolor, "stan": "zrobione" | "teraz" | "przed" | "pominiete"}
opcje      – lista 1–3 nazw; przy jednym pomyśle lista z jedną nazwą albo pusta
kapelusze  – lista wierszy: {"k": kolor, "pola": [{"stan": ..., "punkty": [{"t": tekst, "zr": źródło}]}]}
             liczba pól = liczba opcji albo 1 (pole wspólne)
             opcjonalnie "ogolne": [{"t": tekst, "zr": źródło}] – punkty wiersza, które nie dotyczą żadnej opcji
braki      – {"odCiebie": [...], "doSprawdzenia": [...]}
kierunek   – {"tekst": ..., "podwaza": ...} albo null
decyzje    – lista zdań; pusta, gdy nic jeszcze nie postanowiono
sporne     – lista zdań w postaci „A kontra B · rozstrzygnie: …”
nastepny   – jedno zdanie
plon       – lista
```

Kolory: `bialy`, `czerwony`, `zolty`, `czarny`, `zielony`, `niebieski` (bez polskich znaków). Dane muszą być poprawnym JSON-em. W tekstach nie używaj znaku `<`, a cudzysłów w środku zdania zapisuj jako „ ” albo poprzedzaj ukośnikiem wstecznym.

### Wersja tekstowa

Krótka, do przeczytania w pół minuty. Znaki stanu: ● pełne, ◐ słabe, ○ puste.

```
TABLICA · runda 1 · [temat]
Gdzie jesteśmy: 🔵✓ ⚪✓ 🟡✓ ⚫✓ 🟢✓ 🔴 ← teraz · 🔵

Opcja A – [nazwa]
⚪ ◐ [1–2 punkty]
🟡 ● [1–2 punkty]
⚫ ● [1–2 punkty]
🟢 ● [1–2 punkty]
🔴 ○

Opcja B – [nazwa]
…

Czego brakuje
– od Ciebie: […]
– do sprawdzenia: […] → „mogę to sprawdzić, chcesz?” (gdy masz czym szukać) albo „sprawdzisz to tu: […]”

Kierunek (moja propozycja, decyzja jest Twoja): […] · podważa ją: […]
Decyzje do tej pory: […]
Następny krok: […]
```

Przy jednym pomyśle pomijasz nagłówki opcji. Przy trzech opcjach trzymaj po jednym punkcie na kapelusz, żeby całość mieściła się na ekranie telefonu.

## Samokontrola tablicy

- [ ] Każdy punkt ma źródło, a żaden nie pojawił się pierwszy raz na tablicy.
- [ ] Puste i słabe pola są oznaczone, nie zamaskowane ogólnikiem.
- [ ] Braki są podzielone na „od Ciebie” i „do sprawdzenia”.
- [ ] Kierunek jest podpisany jako propozycja i ma to, co go podważa, albo go nie ma.
- [ ] W „Decyzjach do tej pory” są tylko decyzje, które padły w rozmowie.
- [ ] Jest następny krok.
