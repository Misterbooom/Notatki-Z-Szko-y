# Pozycjonowanie w CSS

Pozycjonowanie w CSS pozwala kontrolować położenie elementów na stronie oraz sposób, w jaki reagują na przewijanie i inne elementy.

---

# 1. Właściwość `position`

Określa sposób pozycjonowania elementu.  
Dostępne wartości: `static`, `relative`, `absolute`, `fixed`, `sticky`.

---

## 1.1 `static`

**Opis:** Domyślne położenie elementu w normalnym przepływie dokumentu.  
Nie reaguje na `top`, `left`, `right`, `bottom` ani `z-index`.

```css
.box {
  position: static;
}
```

### Przykład HTML

```html
<div class="box">Box 1</div>
<div class="box">Box 2</div>
```

<div style="margin:10px 0; background:#1e1e1e; padding:15px; border-radius:12px;">
  <div style="background:#2d2d2d; color:#fff; padding:10px; margin-bottom:5px; border-radius:8px;">Box 1</div>
  <div style="background:#3a3a3a; color:#fff; padding:10px; border-radius:8px;">Box 2</div>
</div>

**Wyjaśnienie:** Elementy ustawiają się jeden pod drugim zgodnie z naturalnym przepływem strony.

---

## 1.2 `relative`

**Opis:** Element pozostaje w przepływie, ale można go przesunąć względem jego pierwotnej pozycji.

```css
.box {
  position: relative;
  top: 20px;
  left: 30px;
}
```

### Przykład HTML

```html
<div class="box">Relative</div>
```

<div style="margin:10px 0; background:#1e1e1e; padding:20px; border-radius:12px;">
  <div style="position:relative; top:20px; left:30px; background:#4caf50; color:white; padding:10px; width:120px; border-radius:8px;">
    Relative
  </div>
</div>

**Wyjaśnienie:** Miejsce pierwotne zostaje zachowane – inne elementy nie przesuwają się.

---

## 1.3 `absolute`

**Opis:** Element wyjęty z przepływu, pozycjonowany względem najbliższego rodzica z `position` innym niż `static`.

```css
.container {
  position: relative;
}

.box {
  position: absolute;
  top: 10px;
  right: 10px;
}
```

### Przykład HTML

```html
<div class="container">
  <div class="box">Absolute</div>
</div>
```

<div style="margin:10px 0; position:relative; height:120px; background:#1e1e1e; border-radius:12px;">
  <div style="position:absolute; top:10px; right:10px; background:#ff9800; color:#000; padding:8px; border-radius:8px;">
    Absolute
  </div>
</div>

**Wyjaśnienie:** Element nie zajmuje miejsca w układzie. Można go ustawić w dowolnym miejscu względem rodzica.

---

## 1.4 `fixed`

**Opis:** Element wyjęty z przepływu, pozycjonowany względem okna przeglądarki. Nie przesuwa się przy scrollowaniu.

```css
.box {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```

### Przykład HTML

```html
<div class="box">Fixed</div>
```

<div style="margin:10px 0;">
  <div style="position:fixed; bottom:20px; right:20px; background:#000; color:#fff; padding:10px; border-radius:50px; box-shadow:0 0 10px rgba(0,0,0,0.6);">
    Fixed
  </div>
</div>

**Wyjaśnienie:** Element pozostaje widoczny w tym samym miejscu nawet podczas przewijania strony.

---

## 1.5 `sticky`

**Opis:** Łączy cechy `relative` i `fixed`. Działa jak `relative` dopóki nie osiągnie progu (`top`, `left`), wtedy „przykleja się”.

```css
.header {
  position: sticky;
  top: 0;
}
```

### Przykład HTML

```html
<div class="header">Sticky header</div>
```

<div style="margin:10px 0; background:#1e1e1e; border-radius:12px; padding:10px;">
  <div style="position:sticky; top:0; background:#6200ea; color:#fff; padding:8px; border-radius:8px;">
    Sticky header
  </div>
  <div style="height:60px;"></div>
</div>

**Wyjaśnienie:** Element przewija się razem ze stroną, ale zatrzymuje się przy określonym progu.

---

# 2. `z-index`

**Opis:** Określa kolejność nakładania elementów w osi Z. Działa tylko dla elementów z `position` innym niż `static`.

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

### Przykład HTML

```html
<div class="box1"></div>
<div class="box2"></div>
```

<div style="margin:20px 0; position:relative; height:120px; background:#1e1e1e; border-radius:12px;">
  <div style="position:absolute; width:80px; height:80px; background:#e91e63; top:20px; left:20px; z-index:1; border-radius:8px;"></div>
  <div style="position:absolute; width:80px; height:80px; background:#03a9f4; top:40px; left:40px; z-index:2; border-radius:8px;"></div>
</div>

**Wyjaśnienie:** Element z wyższym `z-index` będzie wyświetlany nad elementem z niższym.

---

# 3. Podsumowanie

- `static` – brak kontroli położenia.  
- `relative` – przesunięcie względem własnej pozycji, miejsce zachowane.  
- `absolute` – pełna kontrola, poza przepływem.  
- `fixed` – stałe względem okna, nie przewija się.  
- `sticky` – przykleja się przy scrollu po osiągnięciu progu.  

Ciemny styl ułatwia czytelność i sprawia, że przykłady są wyraźne wizualnie.
