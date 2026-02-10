# Pozycjonowanie w CSS


---

## 1. Wartości właściwości `position`

---

### 2.1 `static`

**Wartość domyślna.**

- Element znajduje się w normalnym przepływie dokumentu.
- Właściwości `top`, `right`, `bottom`, `left` **nie działają**.
- `z-index` nie ma zastosowania.

```css
.box {
  position: static;
}
```

Charakterystyka:
- Elementy ustawiają się jeden pod drugim (blokowe) lub obok siebie (inline).
- Brak możliwości ręcznego przesunięcia.

---

### 2.2 `relative`

- Element pozostaje w normalnym przepływie dokumentu.
- Można go przesunąć względem jego **pierwotnej pozycji**.
- Przesunięcie nie wpływa na inne elementy (zostaje „puste miejsce”).

```css
.box {
  position: relative;
  top: 20px;
  left: 30px;
}
```

Działanie:
- `top: 20px` → przesunięcie w dół o 20px.
- `left: 30px` → przesunięcie w prawo o 30px.

Najczęściej używane jako punkt odniesienia dla elementów `absolute`.

---

### 2.3 `absolute`

- Element zostaje **wyjęty z normalnego przepływu dokumentu**.
- Nie zajmuje miejsca w układzie.
- Pozycjonowany względem:
  - najbliższego przodka z `position: relative | absolute | fixed | sticky`,
  - jeśli brak – względem całej strony (viewportu).

```css
.container {
  position: relative;
}

.box {
  position: absolute;
  top: 0;
  right: 0;
}
```

Cechy:
- Można dokładnie określić położenie.
- Często używany do nakładek, ikon, tooltipów.

---

### 2.4 `fixed`

- Element wyjęty z normalnego przepływu.
- Pozycjonowany względem **okna przeglądarki (viewport)**.
- Nie przesuwa się podczas scrollowania.

```css
.menu {
  position: fixed;
  top: 0;
  left: 0;
}
```

Zastosowanie:
- Stałe menu,
- przycisk „Powrót do góry”,
- paski informacyjne.

---

### 2.5 `sticky`

- Łączy cechy `relative` i `fixed`.
- Działa jak `relative`, dopóki nie osiągnie określonej pozycji podczas scrollowania.
- Po przekroczeniu progu „przykleja się” do wskazanej krawędzi.

```css
.header {
  position: sticky;
  top: 0;
}
```

Wymaga:
- ustawionej wartości `top`, `bottom`, `left` lub `right`,
- odpowiedniego kontekstu przewijania.

Zastosowanie:
- Przyklejone nagłówki tabel,
- menu sekcji.

---

## 2. Właściwości `top`, `right`, `bottom`, `left`

Służą do określania odległości elementu od krawędzi.

Działają tylko dla:
- `relative`
- `absolute`
- `fixed`
- `sticky`

Nie działają dla `static`.

Przykład:

```css
.box {
  position: absolute;
  top: 10px;
  left: 20px;
}
```

Interpretacja:
- `top: 10px` → 10px od górnej krawędzi odniesienia,
- `left: 20px` → 20px od lewej krawędzi odniesienia.

Można używać:
- px
- %
- em
- rem
- vh / vw

---

## 3. Właściwość `z-index`

**`z-index` określa kolejność nakładania się elementów (oś Z).**

Działa tylko dla elementów, które mają `position` inne niż `static`.

```css
.box1 {
  position: absolute;
  z-index: 1;
}

.box2 {
  position: absolute;
  z-index: 2;
}
```

Zasady:
- Większa wartość → element wyżej.
- Mniejsza wartość → element niżej.
- Domyślna wartość: `auto`.

Uwaga:
`z-index` działa w obrębie tego samego kontekstu układania (stacking context).

---

## 4. Różnice między wartościami

| Wartość    | W normalnym przepływie | Względem czego pozycjonowany | Reaguje na top/left | Scroll |
|------------|------------------------|------------------------------|---------------------|--------|
| static     | Tak                    | —                            | Nie                 | Tak    |
| relative   | Tak                    | Własna pozycja               | Tak                 | Tak    |
| absolute   | Nie                    | Najbliższy przodek z position | Tak                | Tak    |
| fixed      | Nie                    | Viewport                     | Tak                 | Nie    |
| sticky     | Tak (częściowo)        | Rodzic + viewport            | Tak                 | Przykleja się |

---

## 5. Najczęstsze zastosowania w praktyce

**relative**
- Punkt odniesienia dla elementów `absolute`
- Delikatne przesunięcia elementów

**absolute**
- Tooltipy
- Ikony w polu input
- Nakładki

**fixed**
- Stałe menu
- Floating button
- Pasek cookies

**sticky**
- Przyklejony nagłówek
- Menu sekcji
- Spis treści

---

## 6. Podsumowanie

- `static` – brak kontroli położenia.
- `relative` – przesunięcie względem siebie.
- `absolute` – pełna kontrola, poza przepływem.
- `fixed` – stałe względem okna.
- `sticky` – dynamiczne przyklejanie przy scrollu.

Pozycjonowanie jest kluczowe do budowania układów, nakładek i interaktywnych elementów interfejsu.
