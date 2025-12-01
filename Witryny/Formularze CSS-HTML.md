# 📝 Formularze HTML — wszystkie podstawowe typy pól i tagi

---

## Podstawowe tagi formularzy

- `<form>` – kontener formularza  
- `<label>` – etykieta dla pola formularza (powinna mieć `for="id_pola"`)  
- `<input>` – różne typy pól wprowadzania danych  
- `<textarea>` – pole wieloliniowe  
- `<select>` – lista rozwijana  
- `<option>` – element listy w `<select>`  
- `<button>` – przycisk formularza  
- `<fieldset>` – grupa powiązanych pól  
- `<legend>` – tytuł grupy `<fieldset>`  
- `<datalist>` – lista podpowiedzi dla `<input>`  

---

## Typy `<input>` i przykłady

| Typ              | Przykład                                               | Opis                             |
| ---------------- | ------------------------------------------------------ | -------------------------------- |
| `text`           | `<input type="text" name="username">`                  | Pole tekstowe (jednolinijkowe)   |
| `password`       | `<input type="password" name="pwd">`                   | Pole do hasła, znaki ukryte      |
| `email`          | `<input type="email" name="email">`                    | Walidacja e‑mail                 |
| `number`         | `<input type="number" name="age" min="0" max="100">`   | Pole liczbowe z ograniczeniem    |
| `tel`            | `<input type="tel" name="phone">`                      | Numer telefonu                   |
| `url`            | `<input type="url" name="website">`                    | Walidacja URL                    |
| `search`         | `<input type="search" name="search">`                  | Pole wyszukiwania                |
| `date`           | `<input type="date" name="birthday">`                  | Wybór daty                       |
| `time`           | `<input type="time" name="time">`                      | Wybór godziny                    |
| `datetime-local` | `<input type="datetime-local" name="meeting">`         | Data i godzina lokalna           |
| `month`          | `<input type="month" name="month">`                    | Miesiąc i rok                    |
| `week`           | `<input type="week" name="week">`                      | Tydzień i rok                    |
| `color`          | `<input type="color" name="favcolor">`                 | Wybór koloru                     |
| `checkbox`       | `<input type="checkbox" name="subscribe">`             | Zaznaczenie opcji                |
| `radio`          | `<input type="radio" name="gender" value="male">`      | Wybór jednej opcji z grupy       |
| `file`           | `<input type="file" name="resume">`                    | Wybór pliku                      |
| `range`          | `<input type="range" name="volume" min="0" max="100">` | Suwak liczbowy                   |
| `hidden`         | `<input type="hidden" name="userid" value="12345">`    | Pole niewidoczne dla użytkownika |
| `submit`         | `<input type="submit" value="Wyślij">`                 | Przycisk wysyłania formularza    |
| `reset`          | `<input type="reset" value="Wyczyść">`                 | Resetuje formularz               |
| `button`         | `<input type="button" value="Kliknij">`                | Przycisk niereagujący domyślnie  |

---

## Przykładowy formularz z większością typów
```html
<form action="#" method="post">
  <label for="username">Nazwa użytkownika:</label>
  <input type="text" id="username" name="username">

  <label for="password">Hasło:</label>
  <input type="password" id="password" name="password">

  <label for="email">E-mail:</label>
  <input type="email" id="email" name="email">

  <label for="age">Wiek:</label>
  <input type="number" id="age" name="age" min="0" max="120">

  <label>Płeć:</label>
  <input type="radio" name="gender" value="male"> Mężczyzna
  <input type="radio" name="gender" value="female"> Kobieta

  <label for="subscribe">Subskrybuj newsletter:</label>
  <input type="checkbox" id="subscribe" name="subscribe">

  <label for="favcolor">Ulubiony kolor:</label>
  <input type="color" id="favcolor" name="favcolor">

  <label for="bio">O sobie:</label>
  <textarea id="bio" name="bio"></textarea>

  <label for="country">Kraj:</label>
  <select id="country" name="country">
    <option value="pl">Polska</option>
    <option value="de">Niemcy</option>
    <option value="us">USA</option>
  </select>

  <label for="resume">Dołącz CV:</label>
  <input type="file" id="resume" name="resume">

  <br><br>
  <input type="submit" value="Wyślij">
  <input type="reset" value="Wyczyść">
</form>
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden; padding:16px; max-width:500px;">
<form style="display:flex; flex-direction:column; gap:8px;">
  <label for="username">Nazwa użytkownika:</label>
  <input type="text" id="username" name="username" style="padding:6px; border-radius:4px; border:1px solid #aaa;">

  <label for="password">Hasło:</label>
  <input type="password" id="password" name="password" style="padding:6px; border-radius:4px; border:1px solid #aaa;">

  <label for="email">E-mail:</label>
  <input type="email" id="email" name="email" style="padding:6px; border-radius:4px; border:1px solid #aaa;">

  <label for="age">Wiek:</label>
  <input type="number" id="age" name="age" style="padding:6px; border-radius:4px; border:1px solid #aaa;">

  <label>Płeć:</label>
  <div>
    <input type="radio" name="gender" value="male"> Mężczyzna
    <input type="radio" name="gender" value="female"> Kobieta
  </div>

  <label for="subscribe">Subskrybuj newsletter:</label>
  <input type="checkbox" id="subscribe" name="subscribe">

  <label for="favcolor">Ulubiony kolor:</label>
  <input type="color" id="favcolor" name="favcolor">

  <label for="bio">O sobie:</label>
  <textarea id="bio" name="bio" style="padding:6px; border-radius:4px; border:1px solid #aaa;"></textarea>

  <label for="country">Kraj:</label>
  <select id="country" name="country" style="padding:6px; border-radius:4px; border:1px solid #aaa;">
    <option value="pl">Polska</option>
    <option value="de">Niemcy</option>
    <option value="us">USA</option>
  </select>

  <label for="resume">Dołącz CV:</label>
  <input type="file" id="resume" name="resume">

  <div style="display:flex; gap:8px; margin-top:8px;">
    <input type="submit" value="Wyślij" style="padding:6px 12px; background:#4CAF50; color:white; border:none; border-radius:4px; cursor:pointer;">
    <input type="reset" value="Wyczyść" style="padding:6px 12px; background:#f44336; color:white; border:none; border-radius:4px; cursor:pointer;">
  </div>
</form>
</div>
