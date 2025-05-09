# ?? Arkanoid w Logisim

## ?? Opis projektu

Celem projektu by³o odtworzenie klasycznej gry **Arkanoid** w œrodowisku **Logisim**, z zachowaniem jak najwiêkszej liczby funkcji orygina³u. Gracz steruje paletk¹, odbija pi³kê i rozbija bloczki, zdobywaj¹c punkty. Gra koñczy siê zwyciêstwem po zdobyciu okreœlonej liczby punktów lub zbiciu wszystkich bloczków, albo pora¿k¹ po utracie pi³ki.

---

## ?? Technologie

- ?? **Logisim** – g³ówne œrodowisko projektowe  
- ?? Obs³uga klawiatury – sterowanie gr¹ przyciskami `a` (lewo) i `d` (prawo)  
- ?? Uk³ady logiczne – ROM, RAM, dekodery, multipleksery, liczniki, komparatory  

---

## ??? Zasady gry
1. Naciœnij `START`, aby rozpocz¹æ grê.
2. Steruj paletk¹ za pomoc¹ `a` (lewo) i `d` (prawo).
3. Odbijaj pi³kê, aby zbiæ bloczki.
4. Zdob¹dŸ wszystkie punkty lub zbij wszystkie bloczki, aby wygraæ.
5. Jeœli pi³ka wypadnie poza planszê, przegrywasz.
6. Mo¿esz rozpocz¹æ grê ponownie, naciskaj¹c `START`.

---

## ?? Architektura systemu

Projekt jest oparty na zasadach **OOP (Object-Oriented Programming)** – ka¿dy komponent realizuje jedn¹, wyraŸn¹ funkcjonalnoœæ, a mniejsze modu³y s¹ integrowane w wiêksze bloki. G³ówne komponenty:

### ?? Modu³y gry

| Nazwa | Opis |
|-------|------|
| `BALL::SHIFTER` | Przesuwanie paletki w lewo/prawo |
| `BALL::DECODER` | Pozycjonowanie pi³ki na planszy |
| `BALL::COLLISION` | Wykrywanie kolizji z paletk¹, œcianami, bloczkami |
| `BALL::AXIS::X` / `Y` | Odbicia pi³ki i detekcja pozycji |
| `GAME::STATE` | Wyœwietlanie komunikatów "WIN/LOSE" |
| `GAME::CONTROLLER` | Odczyt i dekodowanie sygna³ów z klawiatury |
| `GAME::INIT` | Inicjalizacja gry i status pi³ki |
| `GAME::BLOCKS` | Obs³uga bloczków i ich eliminacja |
| `GAME::SCORE::HIGHEST` | Zapamiêtywanie najwy¿szego wyniku |
| `GAME::SCORE::CONDITION` | Zliczanie punktów i warunki zwyciêstwa |
| `GAME::START` | OpóŸnione uruchomienie gry |
| `BOARD::CONTROLLER` | Centralny kontroler gry |
| `GAME::SYSTEM` | Integracja wszystkich modu³ów gry |
| `UTILITY::DELAY` | Uk³ad opóŸniaj¹cy do synchronizacji sygna³ów |
| `GAME::WIN::CONDITION` | Zbiór warunków koniecznych do zwyciêstwa |

---

## ? Zrealizowane funkcje

- Odbijanie pi³ki i interakcja z bloczkami
- Wyœwietlacz planszy z dynamiczn¹ grafik¹
- Detekcja zwyciêstwa i przegranej
- Zliczanie punktów i rejestrowanie najlepszego wyniku
- Obs³uga restartu gry i blokada wielokrotnego uruchamiania
- Sterowanie za pomoc¹ klawiatury (`a` i `d`)

---

## ? Niezrealizowane funkcje

- Brak pe³nej eliminacji zbitych bloczków (mo¿liwe ponowne trafienie)
- Brak dynamicznej zmiany liczby punktów wymaganych do wygranej

---

## ?? Mo¿liwoœci rozwoju

- Port projektu do **Logisim Evolution**
- Dodanie efektów dŸwiêkowych
- Dynamiczne zmiany prêdkoœci pi³ki
- Zmienny rozmiar planszy i paletki
- Poprawa obs³ugi zbicia wszystkich bloczków

---

## ?? Uruchamianie projektu

1. Otwórz plik `.circ` w programie **Logisim**.
2. Naciœnij przycisk `START`, aby rozpocz¹æ rozgrywkê.
3. U¿yj klawiszy `a` i `d`, aby sterowaæ paletk¹.
4. Obserwuj wynik oraz komunikaty "WIN/LOSE".