# Game of Life - C++ Implementation

Dieses Projekt implementiert das **Game of Life**, ein zellulärer Automat, in C++. Es zeigt, wie eine Welt von Zellen über Generationen hinweg evolviert, basierend auf den einfachen Regeln des Spiels.

## Funktionen

- **Evolving**: Die Zellen der Welt evolvieren gemäß den Regeln des Game of Life.
- **Muster hinzufügen**: Du kannst beliebige Muster hinzufügen, wie z. B. einen Glider.
- **Speichern und Laden**: Speichert die Welt in einer Datei und lädt sie später wieder.
- **Stabilität prüfen**: Das Programm prüft, ob die Welt stabil ist und keine weiteren Änderungen mehr auftreten.

## Anforderungen

- Ein C++ Compiler (z. B. g++).
- Keine externen Bibliotheken erforderlich.

## Nutzung

1. Klone dieses Repository:

    ```bash
    git clone [https://github.com/dein-benutzername/game-of-life.gi](https://github.com/HabibMubarak/Conway-s-Game-of-Life.git)t
    ```

2. Kompiliere den Code:

    ```bash
    g++ GameOfLife.cpp cli.cpp World.cpp -o GameOfLife
    ```

3. Führe das Programm aus:

    ```bash
    ./GameOfLife
    ```

4. Die Weltinteraktion nun mithilfe der Commandline

## Funktionen im Detail

### `World` Klasse

Die Klasse `World` verwaltet das Spielfeld, das aus Zellen besteht. Jede Zelle kann lebendig (1) oder tot (0) sein.

- **Konstruktoren**: 
    - Ein Konstruktor zum Erstellen einer neuen Welt mit einer gegebenen Höhe und Breite.
    - Ein Konstruktor zum Laden einer Welt aus einer Datei.

- **Methoden**:
    - `evolve()`: Entwickelt die Welt nach den Regeln des Game of Life.
    - `add_glider(int x, int y)`: Fügt das Glider-Muster an einer gegebenen Position hinzu.
    - `save(std::string file_name)`: Speichert die aktuelle Welt in einer Datei.
    - `load(std::string file_name)`: Lädt eine Welt aus einer Datei.
    - `print()`: Gibt die Welt in der Konsole aus.
    - `is_stable()`: Prüft, ob die Welt stabil ist.

### Beispiel

Im Hauptprogramm wird eine Welt von 10x10 Zellen erstellt, ein Glider-Muster hinzugefügt und die Entwicklung über 10 Generationen gezeigt.

```cpp
World world(10, 10); // Erstelle eine Welt 10x10
world.add_glider(2, 2); // Füge ein Glider-Muster hinzu
world.print(); // Zeige die Welt an
