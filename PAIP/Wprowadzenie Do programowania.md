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

|Sposób|Opis|
|---|---|
|**Opis słowny**|opis kroków|
|**Lista kroków**|sekwencja instrukcji|
|**Schemat blokowy**|graficznie: start/decyzje/operacje|
|**Drzewo algorytmu**|możliwe ścieżki wykonania|
|**Drzewo wyrażeń**|dla wyrażeń matematycznych|
|**Pseudokod**|styl programistyczny bez konkretnego języka|
|**Program**|kod w konkretnym języku (np. C++)|

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

## 🧱 TABLICE

### Jednowymiarowa

`int oceny[5] = {5,6,4,5,5};`

Indeksy od `0` do `N-1` (`oceny[0]` pierwsza).

### Dwuwymiarowa

`int macierz[2][3] = {{1,2,3},{4,5,6}};`

### Trójwymiarowa

`int szescian[3][3][3];`

---

## 🧰 Typy złożone

### Struktura (`struct`)

`struct Product {   string name;   string brand;   float price; }; Product p1;`

### Unia (`union`)

- Pola dzielą ten sam obszar pamięci (używane zamiennie).
    

### Klasa (`class`)

- Dane + metody. Podstawa OOP.
    

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

## 2. Podziały języków

### Ze względu na przetwarzanie

- **Kompilowane** – kompilacja → plik wykonywalny (`C, C++`).
    
- **Interpretowane** – wykonywane przez interpreter (`Python, JS`).
    

|Cecha|Kompilowane|Interpretowane|
|---|---|---|
|Prędkość|wyższa|niższa|
|Błędy|wykrywane przy kompilacji|przy uruchomieniu|

### Typowanie

- **Statyczne** – typy w kompilacji (C++, Java).
    

`int x = 10; // błąd: x = "tekst";`

- **Dynamiczne** – typy w runtime (Python).
    

`x = 10 x = "tekst"`

### Poziom

- **Wysokiego poziomu** – bliżej człowieka (Python, Java).
    
- **Niskiego poziomu** – bliżej sprzętu (Assembler, C).
    

### Zastosowania (przykłady)

- Desktop: `C, C++, C#, Java, Python`
    
- Web: frontend `JS/TS`, backend `Python, PHP, Ruby, Java`
    
- Mobile: `Kotlin/Java (Android), Swift (iOS)`
    
- Embedded: `C, C++, Assembler`
    

---

## 3. Paradygmaty programowania

### Definicja

Paradygmat = styl/konwencja programowania (jak opisujemy dane i działania).

### Imperatywny vs Deklaratywny

- **Imperatywny** – opisujesz _jak_ (instrukcje).
    
- **Deklaratywny** – opisujesz _co_ (wynik).
    

### Główne paradygmaty

- **Strukturalny** – logiczne bloki, brak `goto`.
    
- **Proceduralny** – funkcje/procedury.
    
- **Obiektowy (OOP)** – klasy, obiekty, metody.
    
- **Aspektowy (AOP)** – separacja aspektów (logowanie, bezpieczeństwo).
    
- **Generyczny** – szablony / generyki (C++, Java, C#).
    

---

## OOP – podstawy i 4 filary

### Klasa / Obiekt / Konstruktor / Destruktor

Przykład prosty (C++) w tekście.

### 4 filary

- **Abstrakcja** – wydzielenie istotnych cech.
    
- **Polimorfizm** – różne zachowania tej samej nazwy (przeciążanie, rzutowanie).
    
- **Dziedziczenie** – klasa potomna odziedzicza pola/metody.
    
- **Hermetyzacja** – kontrola dostępu (`private`, `protected`, `public`).
    

---

## 4. Definicje PROGRAMU (różne podejścia)

- **Ogólnie:** PROGRAM = algorytm zapisany w języku, wykonujący zadanie.
    
- **Proceduralnie:** zbiór podprogramów zarządzanych przez `main()`.
    
- **Obiektowo:** zestaw komunikujących się obiektów tworzonych z klas.
    

---

## 5. Zasady programowania (mnemoniki)

- **SOLID**, **KISS**, **DRY**, **YAGNI**
    
- **Object Calisthenics** – 9 zasad czystego kodu obiektowego
    

---

## 6. Wnioski

- Współczesne języki są **wieloparadygmatowe**.
    
- Wybór paradygmatu zależy od projektu, zespołu i wymagań.
    
- Zrozumienie paradygmatów przyspiesza naukę nowych języków.
    

---

## Kluczowe pojęcia do zapamiętania

Składnia, syntaktyka, semantyka · Kompilacja vs interpretacja · Typowanie statyczne vs dynamiczne · Poziomy języków · Imperatywny vs deklaratywny · Strukturalny/proceduralny/obiektowy · Klasa/obiekt/konstruktor/destruktor · 4 filary OOP · Przeciążanie, rzutowanie · Modyfikatory: `private`, `protected`, `public`