# 🎮 Arkanoid w Logisim

## 🧠 Opis projektu

Celem projektu było odtworzenie klasycznej gry **Arkanoid** w środowisku **Logisim**, z zachowaniem jak największej liczby funkcji oryginału. Gracz steruje paletką, odbija piłkę i rozbija bloczki, zdobywając punkty. Gra kończy się zwycięstwem po zdobyciu określonej liczby punktów lub zbiciu wszystkich bloczków, albo porażką po utracie piłki.

---

## ⚙️ Technologie

- 🧰 **Logisim** – główne środowisko projektowe  
- ⌨️ Obsługa klawiatury – sterowanie grą przyciskami `a` (lewo) i `d` (prawo)  
- 💾 Układy logiczne – ROM, RAM, dekodery, multipleksery, liczniki, komparatory  

---

## 🕹️ Zasady gry
1. Naciśnij `START`, aby rozpocząć grę.
2. Steruj paletką za pomocą `a` (lewo) i `d` (prawo).
3. Odbijaj piłkę, aby zbić bloczki.
4. Zdobądź wszystkie punkty lub zbij wszystkie bloczki, aby wygrać.
5. Jeśli piłka wypadnie poza planszę, przegrywasz.
6. Możesz rozpocząć grę ponownie, naciskając `START`.

---

## 📐 Architektura systemu

Projekt jest oparty na zasadach **OOP (Object-Oriented Programming)** – każdy komponent realizuje jedną, wyraźną funkcjonalność, a mniejsze moduły są integrowane w większe bloki. Główne komponenty:

### 🔹 Moduły gry

| Nazwa | Opis |
|-------|------|
| `BALL::SHIFTER` | Przesuwanie paletki w lewo/prawo |
| `BALL::DECODER` | Pozycjonowanie piłki na planszy |
| `BALL::COLLISION` | Wykrywanie kolizji z paletką, ścianami, bloczkami |
| `BALL::AXIS::X` / `Y` | Odbicia piłki i detekcja pozycji |
| `GAME::STATE` | Wyświetlanie komunikatów "WIN/LOSE" |
| `GAME::CONTROLLER` | Odczyt i dekodowanie sygnałów z klawiatury |
| `GAME::INIT` | Inicjalizacja gry i status piłki |
| `GAME::BLOCKS` | Obsługa bloczków i ich eliminacja |
| `GAME::SCORE::HIGHEST` | Zapamiętywanie najwyższego wyniku |
| `GAME::SCORE::CONDITION` | Zliczanie punktów i warunki zwycięstwa |
| `GAME::START` | Opóźnione uruchomienie gry |
| `BOARD::CONTROLLER` | Centralny kontroler gry |
| `GAME::SYSTEM` | Integracja wszystkich modułów gry |
| `UTILITY::DELAY` | Układ opóźniający do synchronizacji sygnałów |
| `GAME::WIN::CONDITION` | Zbiór warunków koniecznych do zwycięstwa |

---

## ✅ Zrealizowane funkcje

- Odbijanie piłki i interakcja z bloczkami
- Wyświetlacz planszy z dynamiczną grafiką
- Detekcja zwycięstwa i przegranej
- Zliczanie punktów i rejestrowanie najlepszego wyniku
- Obsługa restartu gry i blokada wielokrotnego uruchamiania
- Sterowanie za pomocą klawiatury (`a` i `d`)

---

## ❌ Niezrealizowane funkcje

- Brak pełnej eliminacji zbitych bloczków (możliwe ponowne trafienie)
- Brak dynamicznej zmiany liczby punktów wymaganych do wygranej

---

## 🔮 Możliwości rozwoju

- Port projektu do **Logisim Evolution**
- Dodanie efektów dźwiękowych
- Dynamiczne zmiany prędkości piłki
- Zmienny rozmiar planszy i paletki
- Poprawa obsługi zbicia wszystkich bloczków

---

## 🏁 Uruchamianie projektu

1. Otwórz plik `.circ` w programie **Logisim**.
2. Naciśnij przycisk `START`, aby rozpocząć rozgrywkę.
3. Użyj klawiszy `a` i `d`, aby sterować paletką.
4. Obserwuj wynik oraz komunikaty "WIN/LOSE".
