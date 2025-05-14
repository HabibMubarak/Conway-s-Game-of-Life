# Game of Life - C++ Implementation

Dieses Projekt implementiert das **Game of Life**, ein zellulärer Automat, in C++. Es zeigt, wie eine Welt von Zellen über Generationen hinweg evolviert, basierend auf den einfachen Regeln des Spiels.

## Funktionen

- **Evolving**: Die Zellen der Welt evolvieren gemäß den Regeln des Game of Life.
- **Muster hinzufügen**: Du kannst beliebige Muster hinzufügen, wie z. B. einen Glider oder Toad.
- **Speichern und Laden**: Speichert die Welt in einer Datei und lädt sie später wieder.
- **Stabilität prüfen**: Das Programm prüft, ob die Welt stabil ist und keine weiteren Änderungen mehr auftreten.

## Dateien

- **World.h**: Enthält die `World`-Klasse, die die Welt des Game of Life verwaltet.
- **CLI.h**: Enthält die `CommandLineInterface`-Klasse für die Benutzeroberfläche und Interaktionen.

### World.h

Die `World`-Klasse stellt das Spielfeld dar, das aus Zellen besteht, die entweder lebendig (1) oder tot (0) sein können. Die Klasse bietet verschiedene Funktionen:

- **Konstruktoren**: 
    - `World(int height, int width)`: Erstellt eine Welt mit der gegebenen Höhe und Breite.
    - `World(std::string file_name)`: Lädt eine Welt aus einer Datei.

- **Methoden**:
    - `evolve()`: Entwickelt die Welt um eine Generation weiter.
    - `count_alive_neighbours(int x, int y)`: Zählt die lebenden Nachbarn einer Zelle.
    - `save(std::string file_name)`: Speichert die Welt in einer Datei.
    - `print()`: Gibt die Welt auf der Konsole aus.
    - `is_equal()`: Vergleicht zwei Welten zur Stabilitätsprüfung.
    - `is_stable()`: Prüft, ob die Welt stabil ist.
    - `load(std::string file_name)`: Lädt die Welt aus einer Datei.
    - `get_cell_state(int x, int y)`: Gibt den Zustand einer Zelle zurück.
    - `set_cell_state(int state, int x, int y)`: Setzt den Zustand einer Zelle.
    - `add_glider(int x, int y)`: Fügt ein Glider-Muster hinzu.
    - `add_toad(int x, int y)`: Fügt ein Toad-Muster hinzu.
    - `add_beacon(int x, int y)`: Fügt ein Beacon-Muster hinzu.
    - `add_methuselah(int x, int y)`: Fügt ein Methuselah-Muster hinzu.
    - `add_random_patterns(int n)`: Fügt zufällige Muster hinzu.

### CLI.h

Die `CommandLineInterface`-Klasse ermöglicht die Benutzerinteraktion über die Konsole. Sie zeigt das Menü und ermöglicht die Eingabe von Befehlen.

- **Methoden**:
    - `menu()`: Zeigt das Menü an und ermöglicht die Auswahl von Aktionen.

## Anforderungen

- Ein C++ Compiler (z. B. g++).
- Keine externen Bibliotheken erforderlich.

## Nutzung

1. Klone dieses Repository:

    ```bash
    git clone https://github.com/HabibMubarak/Conway-s-Game-of-Life.git
    ```

2. Kompiliere den Code:

    ```bash
    g++ GameOfLife.cpp cli.cpp World.cpp -o GameOfLife
    ```

3. Führe das Programm aus:

    ```bash
    ./GameOfLife
    ```

4. Die Welt wird in der Konsole angezeigt. Nach 10 Generationen wird die Welt in einer Datei gespeichert.

## Beispiel

Im Hauptprogramm wird eine Welt von 10x10 Zellen erstellt, ein Glider-Muster hinzugefügt und die Entwicklung über 10 Generationen gezeigt.

```cpp
World world(10, 10); // Erstelle eine Welt 10x10
world.add_glider(2, 2); // Füge ein Glider-Muster hinzu
world.print(); // Zeige die Welt an
