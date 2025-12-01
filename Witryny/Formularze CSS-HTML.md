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

#  Stylowanie tabel w CSS

## border
**Opis:** Dodaje obramowanie tabeli, wierszy lub komórek.  
W CSS skrót `border` składa się z **trzech wartości**:

1. **border-width** – grubość obramowania  
2. **border-style** – styl obramowania  
3. **border-color** – kolor obramowania  

### Przykład skrótu:
```css
border: 1px solid #ccc;
```

### Rozpisanie skrótu na właściwości:
```css
border-width: 1px;
border-style: solid;
border-color: #ccc;
```

---

### Przykład tabeli z obramowaniem
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead>
<tr style="background:bisque;">
<th style="padding:8px;color:black; border:1px solid #ccc;">A</th>
<th style="padding:8px;color:black; border:1px solid #ccc;">B</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid #ccc;">1</td>
<td style="padding:8px; border:1px solid #ccc;">2</td>
</tr>
<tr>
<td style="padding:8px; border:1px solid #ccc;">3</td>
<td style="padding:8px; border:1px solid #ccc;">4</td>
</tr>
</tbody>
</table>
</div>

---

## padding
**Opis:** Ustawia **wewnętrzny odstęp** między krawędzią komórki a jej zawartością.  
Ma wpływ na czytelność tabel.

### Skrót `padding`
`padding` może mieć **1–4 wartości**, które odpowiadają kolejno:

1 wartość → wszystkie strony  
```css
padding: 8px;
```

2 wartości → góra/dół, lewo/prawo  
```css
padding: 8px 16px;
```

4 wartości → góra, prawo, dół, lewo  
```css
padding: 5px 10px 15px 20px;
```

---

### Tabela bez paddingu
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr><th style="padding:0; border:1px solid #ccc;color:black;">Produkt</th><th style="padding:0; border:1px solid #ccc;color:black;">Cena</th></tr>
</thead>
<tbody>
<tr><td style="padding:0; border:1px solid #ccc;">Jabłko</td><td style="padding:0; border:1px solid #ccc;">2 zł</td></tr>
<tr><td style="padding:0; border:1px solid #ccc;">Gruszka</td><td style="padding:0; border:1px solid #ccc;">3 zł</td></tr>
</tbody>
</table>
</div>

---

### Tabela z paddingiem
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr><th style="padding:8px; border:1px solid #ccc;color:black;">Produkt</th><th style="padding:8px; border:1px solid #ccc;color:black;">Cena</th></tr>
</thead>
<tbody>
<tr><td style="padding:8px; border:1px solid #ccc;">Jabłko</td><td style="padding:8px; border:1px solid #ccc;">2 zł</td></tr>
<tr><td style="padding:8px; border:1px solid #ccc;">Gruszka</td><td style="padding:8px; border:1px solid #ccc;">3 zł</td></tr>
</tbody>
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
### Z collapse: 
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr><th style="padding:8px; border:1px solid #ccc;color:black;">Produkt</th><th style="padding:8px; border:1px solid #ccc;color:black;">Cena</th></tr>
</thead>
<tbody>
<tr><td style="padding:8px; border:1px solid #ccc;">Jabłko</td><td style="padding:8px; border:1px solid #ccc;">2 zł</td></tr>
<tr><td style="padding:8px; border:1px solid #ccc;">Gruszka</td><td style="padding:8px; border:1px solid #ccc;">3 zł</td></tr>
</tbody>
</table>
</div>

### Z separate
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:separate;">
<thead style="background:bisque;">
<tr><th style="padding:8px; border:1px solid #ccc;color:black;">Produkt</th><th style="padding:8px; border:1px solid #ccc;color:black;">Cena</th></tr>
</thead>
<tbody>
<tr><td style="padding:8px; border:1px solid #ccc;">Jabłko</td><td style="padding:8px; border:1px solid #ccc;">2 zł</td></tr>
<tr><td style="padding:8px; border:1px solid #ccc;">Gruszka</td><td style="padding:8px; border:1px solid #ccc;">3 zł</td></tr>
</tbody>
</table>
</div>


---

## text-align & vertical-align
```css
td {
  text-align: center;
  vertical-align: middle;
}
```

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
