# Właściwości CSS związane z tłem — przykłady

Poniżej znajdziesz przykłady wszystkich podstawowych właściwości CSS dotyczących tła w formacie Markdown dla Obsidiana.

---

## background-color
**Opis:** Ustawia kolor tła.

```css
background-color: lightblue;
```
<div style="background-color: lightblue; height:100px; border:1px solid #ccc"></div>

---

## background-image
**Opis:** Ustawia obraz jako tło.

```css
background-image: url('https://picsum.photos/300');
```
<div style="background-image: url('https://picsum.photos/300'); height:100px; border:1px solid #ccc"></div>

---

## background-repeat
**Opis:** Określa powtarzanie obrazu.

```css
background-repeat: no-repeat;
```
<div style="background-image: url('https://picsum.photos/100'); background-repeat: no-repeat; height:100px; border:1px solid #ccc"></div>

---

## background-position
**Opis:** Określa położenie obrazu.

```css
background-position: center;
```
<div style="background-image: url('https://picsum.photos/200'); background-position: center; height:100px; border:1px solid #ccc"></div>

---

## background-size
**Opis:** Określa rozmiar obrazu tła.

```css
background-size: cover;
```
<div style="background-image: url('https://picsum.photos/300'); background-size: cover; height:100px; border:1px solid #ccc"></div>

---

## background-attachment
**Opis:** Określa czy tło przewija się ze stroną.

```css
background-attachment: fixed;
```
<div style="background-image: url('https://picsum.photos/400'); background-size: cover; background-attachment: fixed; height:100px; border:1px solid #ccc"></div>

---

## background-clip
**Opis:** Określa obszar wyświetlania tła.

```css
background-clip: content-box;
```
<div style="padding:20px; background-image:url('https://picsum.photos/200'); background-clip: content-box; border:10px solid black; height:100px"></div>

---

## background-origin
**Opis:** Punkt odniesienia tła.

```css
background-origin: border-box;
```
<div style="padding:20px; border:10px solid black; background-image:url('https://picsum.photos/250'); background-origin: border-box; height:100px"></div>

---

## background-blend-mode
**Opis:** Jak mieszają się warstwy tła.

```css
background-blend-mode: multiply;
```
<div style="background-image: url('https://picsum.photos/300'); background-color: red; background-blend-mode: multiply; height:100px"></div>
