# 🧠 KOMPRENDIUM test DO NAUKI – ALGORYTMY I PODSTAWY PROGRAMOWANIA

## 1️⃣ ALGORYTM

### 📘 Definicja

**Algorytm** – jednoznacznie określony ciąg instrukcji, który w skończonej liczbie kroków prowadzi do rozwiązania problemu.  
👉 W prostych słowach: przepis krok-po-kroku, jak uzyskać wynik z danych.

### 🧩 Cechy algorytmu

- **Poprawność** – poprawne wyniki dla poprawnych danych.
    
- **Skończoność** – kończy się po określonej liczbie kroków.
    
- **Efektywność** – minimalna liczba kroków.
    
- **Jednoznaczność** – deterministyczny dla tych samych danych.
    
- **Uniwersalność** – działa dla klasy podobnych zadań.
    
- **Określony początek i koniec**.
    

---

### 🧮 Sposoby przedstawiania algorytmów

| Sposób                   | Opis                                        |
| ------------------------ | ------------------------------------------- |
| [[Opis słowny]]          | opis kroków                                 |
| **[[Lista kroków]]**     | sekwencja instrukcji                        |
| **[[Schemat blokowy]]**  | graficznie: start/decyzje/operacje          |
| **[[Drzewo algorytmu]]** | możliwe ścieżki wykonania                   |
| **[[Drzewo wyrażeń]]**   | dla wyrażeń matematycznych                  |
| **[[Pseudokod]]**        | styl programistyczny bez konkretnego języka |
| **Program**              | kod w konkretnym języku (np. C++)           |

**Przykład pseudokodu:**

`jeśli x%2==0 to     wypisz "liczba parzysta" w przeciwnym wypadku     wypisz "liczba nieparzysta" koniec warunku`

---

## 2️⃣ PODSTAWY PROGRAMOWANIA

### 💾 Dane i zmienne

**Zmienna** – miejsce w pamięci przechowujące wartość określonego typu.

`int wiek = 17;`

### 🧮 Typy danych (C++)

|Typ|Co przechowuje|Przykład|
|---|---|---|
|`int`|liczby całkowite|`10`|
|`double`, `float`|liczby zmiennoprzecinkowe|`3.14`|
|`char`|pojedynczy znak|`'A'`|
|`bool`|wartość logiczna|`true`|
|`string`|tekst|`"Hello"`|

### 🏷️ Identyfikatory

- Nie zaczynają się od cyfry.
    
- Rozróżniają wielkość liter.
    
- Nie są słowami kluczowymi.
    
- Stosuj czytelne nazwy (`age`, `studentName`).
    

**Style nazw:** `camelCase`, `PascalCase`, `snake_case`

### 🌍 Zakres zmiennych

- **Lokalna** – tylko wewnątrz bloku/funkcji.
    
- **Globalna** – widoczna w całym programie.
    

---

### 🔢 Operatory

#### Arytmetyczne

|Operator|Działanie|
|---|---|
|`+`|dodawanie|
|`-`|odejmowanie|
|`*`|mnożenie|
|`/`|dzielenie|
|`%`|reszta z dzielenia|

**Inkrementacja / Dekrementacja**

`++i; // preinkrementacja i++; // postinkrementacja --i; i--;`

#### Przypisania

`x += 5; // x = x + 5 x /= 2; // x = x / 2`

#### Porównania

`==`, `!=`, `>`, `<`, `>=`, `<=`

#### Logiczne

|Operator|Znaczenie|Przykład|
|---|---|---|
|`&&`|AND|`x>0 && y>0`|
|`||`|
|`!`|NOT|`!(x>0)`|

---

## ## 🧱 TABLICE

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
---

## ## 🧰 Typy złożone

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

## ✨ PODSUMOWANIE (krótko)

- **Algorytm** = przepis rozwiązania.
    
- **Zmienna** = miejsce na dane.
    
- **Typ** = co można przechowywać.
    
- **Operatory** = działania, porównania, logika.
    
- **Tablice** = kolekcje tego samego typu.
    
- **Struktury/Unie/Klasy** = złożone dane.
    

---

## 1. JĘZYK PROGRAMOWANIA – definicje i pojęcia

### Definicja

Język programowania to formalny sposób zapisu algorytmu + reguły składni i semantyki.

### Trzy aspekty

- **Składnia** – forma zapisu (dla programisty).
    
- **Syntaktyka** – formalna struktura (dla kompilatora).
    
- **Semantyka** – znaczenie (co program robi).
    

---

## 2. Podziały języków programowania

### Ze względu na sposób przetwarzania kodu

- **Języki kompilowane** – kod źródłowy jest **tłumaczony przez kompilator** na kod maszynowy (plik wykonywalny), który można uruchomić bezpośrednio w systemie operacyjnym.  
    🔹 Przykłady: `C, C++, Rust, Go`.
    
- **Języki interpretowane** – kod źródłowy jest **analizowany i wykonywany linia po linii** przez interpreter, bez tworzenia pliku binarnego.  
    🔹 Przykłady: `Python, JavaScript, PHP, Ruby`.
    

|Cecha|Kompilowane|Interpretowane|
|---|---|---|
|**Prędkość działania**|Zazwyczaj wyższa, bo wykonywany jest kod maszynowy|Niższa, bo interpreter analizuje kod w czasie rzeczywistym|
|**Wykrywanie błędów**|Przy kompilacji (przed uruchomieniem)|Podczas wykonywania programu|
|**Dystrybucja**|Plik wykonywalny (bez źródeł)|Kod źródłowy (uruchamiany przez interpreter)|

### Ze względu na typowanie zmiennych

- **Statyczne typowanie** – typy danych są znane już na etapie kompilacji; każda zmienna ma określony typ, którego nie można zmienić.  
    🔹 Przykłady: `C++, Java, Rust`.
    
    `int x = 10; x = "tekst"; // błąd kompilacji`
    
- **Dynamiczne typowanie** – typ zmiennej ustalany jest w czasie działania programu; typ może się zmieniać.  
    🔹 Przykłady: `Python, JavaScript`.
    
    `x = 10 x = "tekst"  # dozwolone`
    

### Ze względu na poziom abstrakcji

- **Języki wysokiego poziomu** – zbliżone do języka naturalnego, ułatwiające programowanie (automatyczne zarządzanie pamięcią, bogate biblioteki).  
    🔹 Przykłady: `Python, Java, C#, Kotlin`.
    
- **Języki niskiego poziomu** – bliskie architekturze sprzętu, dają pełną kontrolę nad pamięcią i zasobami, ale są trudniejsze w użyciu.  
    🔹 Przykłady: `Assembler, C`.
    

### Ze względu na zastosowania

- **Aplikacje desktopowe:** `C, C++, C#, Java, Python`
    
- **Aplikacje webowe:**
    
    - Frontend: `JavaScript, TypeScript`
        
    - Backend: `Python, PHP, Ruby, Java, Node.js`
        
- **Aplikacje mobilne:**
    
    - `Kotlin, Java` (Android)
        
    - `Swift` (iOS)
        
- **Systemy wbudowane (embedded):** `C, C++, Assembler`
    

---

## 3. Paradygmaty programowania

### Definicja

**Paradygmat programowania** to sposób (styl) myślenia o programowaniu – zestaw zasad i konwencji, które określają **jak organizujemy dane i operacje** w kodzie.

### Imperatywny vs Deklaratywny

- **Imperatywny** – opisuje _jak_ coś zrobić, krok po kroku (ciąg instrukcji zmieniających stan programu).  
    🔹 Przykład: C, Python, Java.
    
    `suma = 0 for x in lista:     suma += x`
    
- **Deklaratywny** – opisuje _co_ chcemy uzyskać, a nie _jak_ to zrobić.  
    🔹 Przykład: SQL, HTML, Prolog.
    
    `SELECT SUM(x) FROM tabela;`
    

### Główne paradygmaty

- **Strukturalny** – program dzielony na logiczne bloki i instrukcje sterujące (`if`, `for`, `while`), bez użycia `goto`.
    
- **Proceduralny** – kod organizowany w funkcje (procedury), które można wielokrotnie wywoływać.
    
- **Obiektowy (OOP)** – świat programu modelowany przez obiekty posiadające dane (pola) i zachowania (metody).
    
- **Aspektowy (AOP)** – separacja tzw. aspektów przekrojowych, np. logowanie, autoryzacja, obsługa błędów.
    
- **Generyczny (szablonowy)** – pisanie uniwersalnych funkcji/klas działających na różnych typach danych (np. `templates` w C++, `generics` w Javie i C#).
    

---

## 4. Program – definicje

- **Ogólnie:** program to **algorytm zapisany w języku programowania**, który wykonuje określone zadanie.
    
- **W podejściu proceduralnym:** program to **zbiór funkcji i procedur** zarządzanych przez funkcję `main()`.
    
- **W podejściu obiektowym:** program to **zestaw współpracujących obiektów**, tworzonych na podstawie klas.
    

---

## 5. Zasady programowania (mnemoniki)

- **SOLID** – 5 zasad dobrego projektowania obiektowego:
    
    - **S** – Single Responsibility
        
    - **O** – Open/Closed
        
    - **L** – Liskov Substitution
        
    - **I** – Interface Segregation
        
    - **D** – Dependency Inversion
        
- **KISS** – _Keep It Simple, Stupid_ – prostota ponad złożoność.
    
- **DRY** – _Don’t Repeat Yourself_ – unikanie powielania kodu.
    
- **YAGNI** – _You Aren’t Gonna Need It_ – nie implementuj funkcji, których jeszcze nie potrzebujesz.
    
- **Object Calisthenics** – zestaw 9 zasad czystego kodu obiektowego, np. jedna odpowiedzialność na klasę, brak `else`, małe klasy, proste metody.
    

---

## 6. Wnioski

- Współczesne języki są **wieloparadygmatowe** – łączą cechy różnych stylów (np. Python: proceduralny + obiektowy + funkcyjny).
    
- Wybór paradygmatu zależy od:
    
    - rodzaju projektu,
        
    - wielkości zespołu,
        
    - wymagań wydajnościowych i skalowalności.
        
- Zrozumienie różnych paradygmatów pomaga szybciej **uczyć się nowych języków** i **lepiej projektować rozwiązania**.
    
- Dobry programista potrafi **dopasować styl programowania** do konkretnego problemu, zamiast trzymać się jednego podejścia.