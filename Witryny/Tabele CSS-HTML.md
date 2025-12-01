# 📊 Podstawowa struktura i stylowanie tabel w CSS

---

## Podstawowa struktura tabeli
- `<table>` – tag, w którym znajduje się cała tabela  
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
<thead style="background:bisque;">
<tr>
<th style="padding:8px; border:1px solid white; color:black;">Imię</th>
<th style="padding:8px; border:1px solid white; color:black;">Wiek</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">Ada</td>
<td style="padding:8px; border:1px solid white;">24</td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">Kamil</td>
<td style="padding:8px; border:1px solid white;">30</td>
</tr>
</tbody>
</table>
</div>

---

# 🎨 Stylowanie tabel w CSS

---

## border
**Opis:** Dodaje obramowanie tabeli, wierszy lub komórek.  

**Skrót `border`** składa się z trzech wartości:  
1. **border-width** – grubość obramowania  
2. **border-style** – styl obramowania  
3. **border-color** – kolor obramowania  

### Przykład skrótu
```css
border: 1px solid white;
```

### Rozpisanie skrótu
```css
border-width: 1px;
border-style: solid;
border-color: white;
```

---

### Tabela z obramowaniem
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr>
<th style="padding:8px; border:1px solid white; color:black;">A</th>
<th style="padding:8px; border:1px solid white; color:black;">B</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">1</td>
<td style="padding:8px; border:1px solid white;">2</td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">3</td>
<td style="padding:8px; border:1px solid white;">4</td>
</tr>
</tbody>
</table>
</div>

---

## padding
**Opis:** Ustawia wewnętrzny odstęp między krawędzią komórki a jej zawartością, zwiększając czytelność tabeli.

### Skrót `padding`
- 1 wartość → wszystkie strony  
```css
padding: 8px;
```
- 2 wartości → góra/dół, lewo/prawo  
```css
padding: 8px 16px;
```
- 4 wartości → góra, prawo, dół, lewo  
```css
padding: 5px 10px 15px 20px;
```

---

### Tabela bez paddingu
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr>
<th style="padding:0; border:1px solid white; color:black;">Produkt</th>
<th style="padding:0; border:1px solid white; color:black;">Cena</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:0; border:1px solid white;">Jabłko</td>
<td style="padding:0; border:1px solid white;">2 zł</td>
</tr>
<tr>
<td style="padding:0; border:1px solid white;">Gruszka</td>
<td style="padding:0; border:1px solid white;">3 zł</td>
</tr>
</tbody>
</table>
</div>

---

### Tabela z paddingiem
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr>
<th style="padding:8px; border:1px solid white; color:black;">Produkt</th>
<th style="padding:8px; border:1px solid white; color:black;">Cena</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">Jabłko</td>
<td style="padding:8px; border:1px solid white;">2 zł</td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">Gruszka</td>
<td style="padding:8px; border:1px solid white;">3 zł</td>
</tr>
</tbody>
</table>
</div>

---

## border-collapse
**Opis:** Łączy lub rozdziela obramowania komórek.  

**Wartości:**
- `collapse` – obramowania łączą się  
- `separate` – obramowania oddzielne (domyślne)

### collapse
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse;">
<thead style="background:bisque;">
<tr>
<th style="padding:8px; border:1px solid white; color:black;">Produkt</th>
<th style="padding:8px; border:1px solid white; color:black;">Cena</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">Jabłko</td>
<td style="padding:8px; border:1px solid white;">2 zł</td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">Gruszka</td>
<td style="padding:8px; border:1px solid white;">3 zł</td>
</tr>
</tbody>
</table>
</div>

### separate
<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="width:100%; border-collapse:separate;">
<thead style="background:bisque;">
<tr>
<th style="padding:8px; border:1px solid white; color:black;">Produkt</th>
<th style="padding:8px; border:1px solid white; color:black;">Cena</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">Jabłko</td>
<td style="padding:8px; border:1px solid white;">2 zł</td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">Gruszka</td>
<td style="padding:8px; border:1px solid white;">3 zł</td>
</tr>
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

## colspan & rowspan
```html
<td colspan="2">Połączone w poziomie</td>
<td rowspan="2">Połączone w pionie</td>
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden;">
<table style="border-collapse:collapse; width:100%;">
<tr>
<td style="border:1px solid white; padding:8px;vertical-align:middle;text-align:center;" colspan="2">colspan = 2</td>
<td style="border:1px solid white; padding:8px;vertical-align:middle;text-align:center;" rowspan="2">rowspan = 2</td>
</tr>
<tr>
<td style="border:1px solid white; padding:8px;vertical-align:middle;text-align:center;">A</td>
<td style="border:1px solid white; padding:8px;vertical-align:middle;text-align:center;">B</td>
</tr>
</table>
</div>

---

## border-radius
**Opis:** Zaokrąla rogi tabeli lub komórek.  

### Właściwości
- `border-radius: 8px;` – zaokrąglenie wszystkich rogów  
- Różne wartości dla każdego rogu:
```css
border-radius: 10px 0 10px 0; /* góra-lewo, góra-prawo, dół-prawo, dół-lewo */
```

---

### Przykład tabeli z zaokrąglonymi rogami
<div style="margin:10px 0; border-radius:20px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse; border-radius:12px;">
<thead style="background:bisque;">
<tr>
<th style="padding:8px; border:1px solid white;color:black;">Produkt</th>
<th style="padding:8px; border:1px solid white;color:black;">Cena</th>
<th style="padding:8px; border:1px solid white;color:black;">Zdjęcie</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">Jabłko</td>
<td style="padding:8px; border:1px solid white;">2 zł</td>
<td style="padding:8px; border:1px solid white;"><img src="https://picsum.photos/50" alt="jabłko" style="border-radius:6px;"></td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">Gruszka</td>
<td style="padding:8px; border:1px solid white;">3 zł</td>
<td style="padding:8px; border:1px solid white;"><img src="https://picsum.photos/50?2" alt="gruszka" style="border-radius:6px;"></td>
</tr>
</tbody>
</table>
</div>

---

### Przykład różnych wartości border-radius
<div style="margin:10px 0; border-radius:20px 5px 20px 5px; overflow:hidden;">
<table style="width:100%; border-collapse:collapse; border-radius:20px 5px 20px 5px;">
<thead style="background:lightblue;">
<tr>
<th style="padding:8px; border:1px solid white;color:black;">Produkt</th>
<th style="padding:8px; border:1px solid white;color:black;">Cena</th>
<th style="padding:8px; border:1px solid white;color:black;">Zdjęcie</th>
</tr>
</thead>
<tbody>
<tr>
<td style="padding:8px; border:1px solid white;">Banana</td>
<td style="padding:8px; border:1px solid white;">4 zł</td>
<td style="padding:8px; border:1px solid white;"><img src="https://picsum.photos/50?3" alt="banan" style="border-radius:10px;"></td>
</tr>
<tr>
<td style="padding:8px; border:1px solid white;">Winogrono</td>
<td style="padding:8px; border:1px solid white;">5 zł</td>
<td style="padding:8px; border:1px solid white;"><img src="https://picsum.photos/50?4" alt="winogrono" style="border-radius:10px;"></td>
</tr>
</tbody>
</table>
</div>
