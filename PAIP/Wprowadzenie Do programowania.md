# 🧠 KOMPRENDIUM TEST DO NAUKI – ALGORYTMY I PODSTAWY PROGRAMOWANIA

---

## 1️⃣ ALGORYTM

### 📘 Definicja

**Algorytm** – jednoznacznie określony ciąg instrukcji, który w skończonej liczbie kroków prowadzi do rozwiązania problemu.  
👉 W prostych słowach: przepis krok-po-kroku, jak uzyskać wynik z danych.

---

### 🧩 Cechy algorytmu

- **Poprawność** – poprawne wyniki dla poprawnych danych.
    
- **Skończoność** – kończy się po określonej liczbie kroków.
    
- **Efektywność** – minimalna liczba kroków.
    
- **Jednoznaczność** – deterministyczny dla tych samych danych.
    
- **Uniwersalność** – działa dla klasy podobnych zadań.
    
- **Określony początek i koniec.**
    

---

### 🧮 Sposoby przedstawiania algorytmów

| Sposób               | Opis                                        |
| :------------------- | :------------------------------------------ |
| [[Opis słowny]]      | opis kroków                                 |
| [[Lista kroków]]     | sekwencja instrukcji                        |
| [[Schemat blokowy]]  | graficznie: start/decyzje/operacje          |
| [[Drzewo algorytmu]] | możliwe ścieżki wykonania                   |
| [[Drzewo wyrażeń]]   | dla wyrażeń matematycznych                  |
| [[Pseudokod]]        | styl programistyczny bez konkretnego języka |
| [[Program]]          | kod w konkretnym języku (np. C++)           |

**Przykład pseudokodu:**

```text
jeśli x % 2 == 0 to
    wypisz "liczba parzysta"
w przeciwnym wypadku
    wypisz "liczba nieparzysta"
koniec warunku
```

---

## 2️⃣ PODSTAWY PROGRAMOWANIA

### 💾 Dane i zmienne

**Zmienna** – miejsce w pamięci przechowujące wartość określonego typu.

```cpp
int wiek = 17;
```

---

### 🧮 Typy danych (C++)

|Typ|Co przechowuje|Przykład|
|:--|:--|:--|
|`int`|liczby całkowite|`10`|
|`double`, `float`|liczby zmiennoprzecinkowe|`3.14`|
|`char`|pojedynczy znak|`'A'`|
|`bool`|wartość logiczna|`true`|
|`string`|tekst|`"Hello"`|

---

### 🏷️ Identyfikatory

- Nie zaczynają się od cyfry.
    
- Rozróżniają wielkość liter.
    
- Nie są słowami kluczowymi.
    
- Stosuj czytelne nazwy (`age`, `studentName`).
    

**Style nazw:** `camelCase`, `PascalCase`, `snake_case`

---

### 🌍 Zakres zmiennych

- **Lokalna** – tylko wewnątrz bloku/funkcji.
    
- **Globalna** – widoczna w całym programie.
    

---

### 🔢 Operatory

#### Arytmetyczne

|Operator|Działanie|
|:--|:--|
|`+`|dodawanie|
|`-`|odejmowanie|
|`*`|mnożenie|
|`/`|dzielenie|
|`%`|reszta z dzielenia|

**Inkrementacja / Dekrementacja**

```cpp
++i; // preinkrementacja
i++; // postinkrementacja
--i;
i--;
```

#### Przypisania

```cpp
x += 5; // x = x + 5
x /= 2; // x = x / 2
```

#### Porównania

`==`, `!=`, `>`, `<`, `>=`, `<=`

#### Logiczne

|Operator|Znaczenie|Przykład|
|:--|:--|:--|
|`&&`|AND|`x > 0 && y > 0`|
|`||`|
|`!`|NOT|`!(x > 0)`|

---

## 🧱 TABLICE

### Tablica jednowymiarowa

Zbiór elementów tego samego typu.

```cpp
int oceny[5] = {5, 6, 4, 5, 5};
```

➡️ Indeksowanie od 0 → pierwszy element to `oceny[0]`

### Tablica dwuwymiarowa

```cpp
int macierz[2][3] = {{1,2,3}, {4,5,6}};
```

### Tablica trójwymiarowa

```cpp
int szescian[3][3][3];
```

---

## 🧰 Typy złożone

### Struktura (`struct`)

```cpp
struct Product {
  string name;
  string brand;
  float price;
};
Product p1;
```

### Unia (`union`)

Podobna do struktury, ale wszystkie pola **dzielą ten sam obszar pamięci**.

### Klasa (`class`)

Rozszerzona struktura – oprócz danych może mieć **metody**.

---

## ✨ PODSUMOWANIE (krótko)

- **Algorytm** = przepis rozwiązania.
    
- **Zmienna** = miejsce na dane.
    
- **Typ** = co można przechowywać.
    
- **Operatory** = działania, porównania, logika.
    
- **Tablice** = kolekcje danych.
    
- **Struktury / Unie / Klasy** = dane złożone.
    

---

## 1️⃣ JĘZYK PROGRAMOWANIA – definicje i pojęcia

### Definicja

Język programowania to formalny sposób zapisu algorytmu + reguły składni i semantyki.

### Trzy aspekty

- **Składnia** – forma zapisu (dla programisty).
    
- **Syntaktyka** – formalna struktura (dla kompilatora).
    
- **Semantyka** – znaczenie (co program robi).
    

---

## 2️⃣ Podziały języków programowania

### Ze względu na sposób przetwarzania kodu

- **Kompilowane** – tłumaczone na kod maszynowy.  
    🔹 Przykłady: `C, C++, Rust, Go`
    
- **Interpretowane** – analizowane linia po linii.  
    🔹 Przykłady: `Python, JavaScript, PHP`
    

|Cecha|Kompilowane|Interpretowane|
|:--|:--|:--|
|Prędkość|wyższa|niższa|
|Wykrywanie błędów|przy kompilacji|w czasie działania|
|Dystrybucja|plik binarny|kod źródłowy|

---

### Ze względu na typowanie zmiennych

- **Statyczne typowanie** – typ znany przy kompilacji.
    
- **Dynamiczne typowanie** – typ ustalany w trakcie działania.
    

---

### Ze względu na poziom abstrakcji

- **Wysokiego poziomu** – zbliżone do języka naturalnego.
    
- **Niskiego poziomu** – bliskie sprzętowi.
    

---

### Ze względu na zastosowanie

|Zastosowanie|Języki|
|:--|:--|
|Aplikacje desktopowe|`C, C++, C#, Java, Python`|
|Web (frontend)|`JavaScript, TypeScript`|
|Web (backend)|`Python, PHP, Java, Node.js`|
|Mobilne|`Kotlin, Java, Swift`|
|Embedded|`C, C++`|

---

## 3️⃣ Paradygmaty programowania

### Definicja

**Paradygmat programowania** – sposób myślenia o programie.

### Imperatywny vs Deklaratywny

- **Imperatywny** – opisuje _jak_ coś zrobić.  
    🔹 Przykład: C, Python, Java.
    

```python
suma = 0
for x in lista:
    suma += x
```

- **Deklaratywny** – opisuje _co_ chcemy uzyskać.  
    🔹 Przykład: SQL, HTML.
    

```sql
SELECT SUM(x) FROM tabela;
```

---

### Główne paradygmaty

- Strukturalny
    
- Proceduralny
    
- Obiektowy (OOP)
    
- Aspektowy (AOP)
    
- Generyczny (szablonowy)
    

---

## 4️⃣ Program – definicje

- Program = algorytm zapisany w języku programowania.
    
- W proceduralnym – zbiór funkcji.
    
- W obiektowym – zbiór współpracujących obiektów.
    

---

## 5️⃣ Zasady programowania (mnemoniki)

- **SOLID** – zasady projektowania obiektowego.
    
- **KISS** – prostota.
    
- **DRY** – unikanie powielania kodu.
    
- **YAGNI** – nie twórz czego nie potrzebujesz.
    
- **Object Calisthenics** – zasady czystego kodu.
    

---

## 6️⃣ OOP – podstawy i 4 filary

  

### Klasa / Obiekt / Konstruktor / Destruktor

  

**Klasa** – szablon opisujący dane (pola) i zachowania (metody) obiektów.

```cpp

class Samochod {
public:
    string marka;
    int rok;

    Samochod(string m, int r) {

        marka = m;
        rok = r;
    }
    void pokaz() {

        cout << marka << " z roku " << rok << endl;
    }
};

```

**Obiekt** – instancja klasy, czyli konkretna realizacja.

```cpp

Samochod s1("Audi", 2015);

s1.pokaz();

```

  

**Konstruktor** – metoda wywoływana przy tworzeniu obiektu.

**Destruktor** – metoda wywoływana przy usuwaniu obiektu.

  

---

  

### 4 Filary

| Nazwa             | Opis                                                |
| ----------------- | --------------------------------------------------- |
| **Abstrakcja**    | wydzielenie istotnych cech                          |
| **Polimorfizm**   | różne zachowania tej samej nazwy                    |
| **Dziedziczenie** | klasa potomna dziedziczy pola/metody                |
| **Hermetyzacja**  | kontrola dostępu (`private`, `protected`, `public`) |


  

---

  

## 7️⃣ Wnioski

  

- Współczesne języki są wieloparadygmatowe.

- Wybór paradygmatu zależy od projektu.

- Zrozumienie stylów pomaga szybciej uczyć się nowych języków.

- Dobry programista dopasowuje styl do problemu.