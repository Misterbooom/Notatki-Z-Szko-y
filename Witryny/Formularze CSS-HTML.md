## Podstawowa struktura tabeli
- `<table>` – tag gdzie jest cała tabela
- `<tr>` – wiersz tabeli  
- `<td>` – komórka danych  
- `<th>` – komórka nagłówka  
- `<thead>`, `<tbody>`, `<tfoot>` – semantyczne sekcje tabeli

### Przykład
```html
<table>
  <thead>
    <tr>
      <th>Imię</th>
      <th>Wiek</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ada</td>
      <td>24</td>
    </tr>
    <tr>
      <td>Kamil</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque; ">
<tr><th style="padding:8px; border:1px solid #ccc;color:black;">Imię</th><th style="padding:8px; border:1px solid #ccc;color:black;">Wiek</th></tr>
</thead>
<tbody>
<tr><td style="padding:8px; border:1px solid #ccc;">Ada</td><td style="padding:8px; border:1px solid #ccc;">24</td></tr>
<tr><td style="padding:8px; border:1px solid #ccc;">Kamil</td><td style="padding:8px; border:1px solid #ccc;">30</td></tr>
</tbody>
</table>
</div>

---

# 🎨 Stylowanie tabel w CSS

## border:
**Opis:** Dodaje obramowanie tabeli lub komórek.

```css
table, td, th {
  border: 1px solid #333;
}
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<tr><th style="border:1px solid white; padding:8px;">A</th><th style="border:1px solid white; padding:8px;">B</th></tr>
<tr><td style="border:1px solid white; padding:8px;">1</td><td style="border:1px solid white; padding:8px;">2</td></tr>
</table>
</div>

---

## border-collapse
**Opis:** Łączy lub rozdziela obramowania komórek.

**Wartości:**
- `collapse` – obramowania łączą się  
- `separate` – obramowania oddzielne (domyślne)

```css
table {
  border-collapse: collapse;
}
```

---

## padding w komórkach
```css
td, th {
  padding: 10px;
}
```

---

## text-align & vertical-align

```css
td {
  text-align: center;
  vertical-align: middle;
}
```

---

## background-color dla wierszy i komórek
```css
th {
  background-color: #e0e0e0;
}

tr:nth-child(even) {
  background-color: #f9f9f9;
}
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead>
<tr style="background:#e0e0e0;"><th style="padding:8px; border:1px solid #ccc;">Produkt</th><th style="padding:8px; border:1px solid #ccc;">Cena</th></tr>
</thead>
<tbody>
<tr style="background:#fff;"><td style="padding:8px; border:1px solid #ccc;">Jabłko</td><td style="padding:8px; border:1px solid #ccc;">2 zł</td></tr>
<tr style="background:#f9f9f9;"><td style="padding:8px; border:1px solid #ccc;">Gruszka</td><td style="padding:8px; border:1px solid #ccc;">3 zł</td></tr>
</tbody>
</table>
</div>

---

## width & table-layout

### Wartości:
- `auto` – szerokości na podstawie treści  
- `fixed` – równe kolumny

```css
table {
  width: 100%;
  table-layout: fixed;
}
```

---

## colspan & rowspan

```html
<td colspan="2">Połączone w poziomie</td>
<td rowspan="2">Połączone w pionie</td>
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="border-collapse:collapse; width:100%;">
<tr>
  <td style="border:1px solid #ccc; padding:8px;" colspan="2">colspan = 2</td>
  <td style="border:1px solid #ccc; padding:8px;" rowspan="2">rowspan = 2</td>
</tr>
<tr>
  <td style="border:1px solid #ccc; padding:8px;">A</td>
  <td style="border:1px solid #ccc; padding:8px;">B</td>
</tr>
</table>
</div>

---

## Zebra stripes

```css
tr:nth-child(odd) {
  background-color: #fafafa;
}
tr:nth-child(even) {
  background-color: #eaeaea;
}
```

---

## Tabele responsywne

**Opis:** Dodaje przewijanie poziome dla małych ekranów.

```html
<div class="table-wrapper">
  <table>...</table>
</div>
```

```css
.table-wrapper {
  overflow-x: auto;
}
```

<div style="overflow-x:auto; border:1px solid #ccc; border-radius:8px; padding:4px; margin:10px 0;">
<table style="border-collapse:collapse; min-width:500px;">
<tr><th style="padding:8px; border:1px solid #ccc;">Kol1</th><th style="padding:8px; border:1px solid #ccc;">Kol2</th><th style="padding:8px; border:1px solid #ccc;">Kol3</th><th style="padding:8px; border:1px solid #ccc;">Kol4</th></tr>
<tr><td style="padding:8px; border:1px solid #ccc;">A</td><td style="padding:8px; border:1px solid #ccc;">B</td><td style="padding:8px; border:1px solid #ccc;">C</td><td style="padding:8px; border:1px solid #ccc;">D</td></tr>
</table>
</div>

---
