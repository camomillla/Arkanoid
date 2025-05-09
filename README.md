# ?? Arkanoid w Logisim

## ?? Opis projektu

Celem projektu by�o odtworzenie klasycznej gry **Arkanoid** w �rodowisku **Logisim**, z zachowaniem jak najwi�kszej liczby funkcji orygina�u. Gracz steruje paletk�, odbija pi�k� i rozbija bloczki, zdobywaj�c punkty. Gra ko�czy si� zwyci�stwem po zdobyciu okre�lonej liczby punkt�w lub zbiciu wszystkich bloczk�w, albo pora�k� po utracie pi�ki.

---

## ?? Technologie

- ?? **Logisim** � g��wne �rodowisko projektowe  
- ?? Obs�uga klawiatury � sterowanie gr� przyciskami `a` (lewo) i `d` (prawo)  
- ?? Uk�ady logiczne � ROM, RAM, dekodery, multipleksery, liczniki, komparatory  

---

## ??? Zasady gry
1. Naci�nij `START`, aby rozpocz�� gr�.
2. Steruj paletk� za pomoc� `a` (lewo) i `d` (prawo).
3. Odbijaj pi�k�, aby zbi� bloczki.
4. Zdob�d� wszystkie punkty lub zbij wszystkie bloczki, aby wygra�.
5. Je�li pi�ka wypadnie poza plansz�, przegrywasz.
6. Mo�esz rozpocz�� gr� ponownie, naciskaj�c `START`.

---

## ?? Architektura systemu

Projekt jest oparty na zasadach **OOP (Object-Oriented Programming)** � ka�dy komponent realizuje jedn�, wyra�n� funkcjonalno��, a mniejsze modu�y s� integrowane w wi�ksze bloki. G��wne komponenty:

### ?? Modu�y gry

| Nazwa | Opis |
|-------|------|
| `BALL::SHIFTER` | Przesuwanie paletki w lewo/prawo |
| `BALL::DECODER` | Pozycjonowanie pi�ki na planszy |
| `BALL::COLLISION` | Wykrywanie kolizji z paletk�, �cianami, bloczkami |
| `BALL::AXIS::X` / `Y` | Odbicia pi�ki i detekcja pozycji |
| `GAME::STATE` | Wy�wietlanie komunikat�w "WIN/LOSE" |
| `GAME::CONTROLLER` | Odczyt i dekodowanie sygna��w z klawiatury |
| `GAME::INIT` | Inicjalizacja gry i status pi�ki |
| `GAME::BLOCKS` | Obs�uga bloczk�w i ich eliminacja |
| `GAME::SCORE::HIGHEST` | Zapami�tywanie najwy�szego wyniku |
| `GAME::SCORE::CONDITION` | Zliczanie punkt�w i warunki zwyci�stwa |
| `GAME::START` | Op�nione uruchomienie gry |
| `BOARD::CONTROLLER` | Centralny kontroler gry |
| `GAME::SYSTEM` | Integracja wszystkich modu��w gry |
| `UTILITY::DELAY` | Uk�ad op�niaj�cy do synchronizacji sygna��w |
| `GAME::WIN::CONDITION` | Zbi�r warunk�w koniecznych do zwyci�stwa |

---

## ? Zrealizowane funkcje

- Odbijanie pi�ki i interakcja z bloczkami
- Wy�wietlacz planszy z dynamiczn� grafik�
- Detekcja zwyci�stwa i przegranej
- Zliczanie punkt�w i rejestrowanie najlepszego wyniku
- Obs�uga restartu gry i blokada wielokrotnego uruchamiania
- Sterowanie za pomoc� klawiatury (`a` i `d`)

---

## ? Niezrealizowane funkcje

- Brak pe�nej eliminacji zbitych bloczk�w (mo�liwe ponowne trafienie)
- Brak dynamicznej zmiany liczby punkt�w wymaganych do wygranej

---

## ?? Mo�liwo�ci rozwoju

- Port projektu do **Logisim Evolution**
- Dodanie efekt�w d�wi�kowych
- Dynamiczne zmiany pr�dko�ci pi�ki
- Zmienny rozmiar planszy i paletki
- Poprawa obs�ugi zbicia wszystkich bloczk�w

---

## ?? Uruchamianie projektu

1. Otw�rz plik `.circ` w programie **Logisim**.
2. Naci�nij przycisk `START`, aby rozpocz�� rozgrywk�.
3. U�yj klawiszy `a` i `d`, aby sterowa� paletk�.
4. Obserwuj wynik oraz komunikaty "WIN/LOSE".