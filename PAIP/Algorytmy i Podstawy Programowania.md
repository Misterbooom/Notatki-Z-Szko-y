
# 🧠 KOMPRENDIUM  test DO NAUKI – ALGORYTMY I PODSTAWY PROGRAMOWANIA

## 1️⃣ ALGORYTM

### 📘 Definicja
**Algorytm** – jednoznacznie określony ciąg instrukcji, który w skończonej liczbie kroków prowadzi do rozwiązania problemu.

👉 W prostych słowach: to przepis, jak coś zrobić krok po kroku, żeby uzyskać wynik z podanych danych.

### 🧩 Cechy algorytmu
- **Poprawność** – daje poprawne wyniki dla poprawnych danych.  
- **Skończoność** – kończy się po określonej liczbie kroków.  
- **Efektywność** – wykonuje zadanie w jak najmniejszej liczbie kroków.  
- **Jednoznaczność** – dla tych samych danych zawsze daje ten sam wynik.  
- **Uniwersalność** – można go zastosować do różnych przypadków danego typu zadań.  
- **Określony początek i koniec** – wiadomo, kiedy się zaczyna i kończy.

---

### 🧮 Sposoby przedstawiania algorytmów

| Sposób               | Opis                                                           |
| -------------------- | -------------------------------------------------------------- |
| **[[Opis słowny]]**  | Po prostu opisujemy, co ma się dziać krok po kroku.            |
| **Lista kroków**     | Numerujemy polecenia: Krok 1 – wczytaj x, Krok 2 – policz…     |
| **Schemat blokowy**  | Graficzne przedstawienie algorytmu (start, decyzje, operacje). |
| **Drzewo algorytmu** | Pokazuje możliwe ścieżki wykonania kroków.                     |
| **Drzewo wyrażeń**   | Dla działań matematycznych, np. (3+2)-(4-2).                   |
| **Pseudokod**        | Zapis w stylu programowania, ale bez konkretnego języka.       |
| **Program**          | Gotowy kod w języku programowania (np. C++).                   |

**Przykład pseudokodu:**
```
jeśli x%2==0 to
    wypisz "liczba parzysta"
w przeciwnym wypadku
    wypisz "liczba nieparzysta"
koniec warunku
```

---

## 2️⃣ PODSTAWY PROGRAMOWANIA

### 💾 Co to są dane i zmienne?

Program przechowuje różne informacje – np. imiona, liczby, temperatury.  
Aby je zapisać, potrzebujemy **zmiennych**.

**Zmienna** – miejsce w pamięci komputera, w którym przechowywana jest wartość o określonym typie.

Przykład:
```cpp
int wiek = 17;
```

---

### 🧮 Typy danych (C++)
| Typ | Co przechowuje | Przykład |
|------|----------------|-----------|
| `int` | liczby całkowite | 10 |
| `double`, `float` | liczby z przecinkiem (używa się kropki) | 3.14 |
| `char` | pojedynczy znak | 'A' |
| `bool` | wartość logiczną: prawda (1) lub fałsz (0) | true |
| `string` | tekst | "Hello" |

---

### 🏷️ Identyfikatory (nazwy zmiennych)
Zasady:
- nie mogą zaczynać się od cyfry,  
- rozróżniają wielkość liter (`Liczba` ≠ `liczba`),  
- nie mogą być słowami kluczowymi (`if`, `for`, `int`, itp.),  
- warto nadawać **czytelne nazwy** (np. `age`, `studentName`).

**Style nazw:**
- `camelCase` → `myName`
- `PascalCase` → `MyName`
- `snake_case` → `my_name`

---

### 🌍 Zmienne lokalne i globalne
- **Lokalna** – działa tylko w swoim bloku kodu (np. wewnątrz funkcji).  
- **Globalna** – widoczna w całym programie.

---

### 🔢 Operatory

#### Operatory arytmetyczne:
| Operator | Działanie | Przykład |
|-----------|------------|-----------|
| `+` | dodawanie | x + y |
| `-` | odejmowanie | x - y |
| `*` | mnożenie | x * y |
| `/` | dzielenie | x / y |
| `%` | reszta z dzielenia | x % y |

**Inkrementacja i dekrementacja:**
- `++i` → zwiększ i o 1 (przed użyciem)  
- `i++` → zwiększ i o 1 (po użyciu)

#### Operatory przypisania:
`x += 5;` ⇔ `x = x + 5;`

#### Operatory porównania:
`==`, `!=`, `>`, `<`, `>=`, `<=`

#### Operatory logiczne:
| Operator | Znaczenie | Przykład |
|-----------|------------|-----------|
| `&&` | AND – oba warunki muszą być prawdziwe | x>0 && y>0 |
| `||` | OR – wystarczy, że jeden jest prawdziwy | x>0 || y>0 |
| `!` | NOT – negacja | !(x>0) |

---

## 🧱 TABLICE

### Tablica jednowymiarowa
Zbiór elementów tego samego typu, np. kilka ocen ucznia.

```cpp
int oceny[5] = {5, 6, 4, 5, 5};
```
➡️ Indeksowanie od 0 → pierwszy element to `oceny[0]`

### Tablica dwuwymiarowa
Można ją wyobrazić jak tabelkę (wiersze i kolumny).

```cpp
int macierz[2][3] = {{1,2,3}, {4,5,6}};
```

### Tablica trójwymiarowa
Wyobraź sobie kostkę Rubika:
```cpp
int szescian[3][3][3];
```

---

## 🧰 Typy złożone

Kiedy potrzebujemy przechować różne dane o jednym obiekcie (np. produkt ma nazwę, markę i cenę).

### Struktura (`struct`)
Grupuje dane różnego typu:
```cpp
struct Product {
  string name;
  string brand;
  float price;
};
Product p1;
```

### Unia (`union`)
Podobna do struktury, ale wszystkie pola **dzielą ten sam obszar pamięci** (czyli mogą być używane zamiennie).

### Klasa (`class`)
Rozszerzona struktura – oprócz danych może mieć też **funkcje (metody)**.  
Używana w programowaniu obiektowym.

---

## ✨ PODSUMOWANIE
- **Algorytm** = przepis na rozwiązanie problemu.  
- **Zmienna** = miejsce na dane w pamięci.  
- **Typ danych** = określa, jaki rodzaj wartości można przechowywać.  
- **Operatory** = narzędzia do działań matematycznych, logicznych i przypisań.  
- **Tablice** = przechowują wiele wartości tego samego typu.  
- **Struktury / Unie / Klasy** = przechowują dane złożone.  
