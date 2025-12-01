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

<div style="margin:10px 0; border-radius:12px; overflow:hidden; padding:16px; border:1px solid #ccc; max-width:500px;">
<form>
  <label for="username">Nazwa użytkownika:</label><br>
  <input type="text" id="username" name="username" style="width:100%; padding:6px; margin-bottom:0; border-radius:4px; border:1px solid #aaa;">

  <label for="password">Hasło:</label><br>
  <input type="password" id="password" name="password" style="width:100%; padding:6px; margin-bottom:0; border-radius:4px; border:1px solid #aaa;">

  <label for="email">E-mail:</label><br>
  <input type="email" id="email" name="email" style="width:100%; padding:6px; margin-bottom:0; border-radius:4px; border:1px solid #aaa;">

  <label for="age">Wiek:</label><br>
  <input type="number" id="age" name="age" style="width:100%; padding:6px; margin-bottom:0; border-radius:4px; border:1px solid #aaa;">

  <label>Płeć:</label><br>
  <input type="radio" name="gender" value="male"> Mężczyzna
  <input type="radio" name="gender" value="female"> Kobieta
  <br><br>

  <label for="subscribe">Subskrybuj newsletter:</label><br>
  <input type="checkbox" id="subscribe" name="subscribe">
  <br><br>

  <label for="favcolor">Ulubiony kolor:</label><br>
  <input type="color" id="favcolor" name="favcolor" style="margin-bottom:0;">
  <br>

  <label for="bio">O sobie:</label><br>
  <textarea id="bio" name="bio" style="width:100%; padding:6px; margin-bottom:0; border-radius:4px; border:1px solid #aaa;"></textarea>

  <label for="country">Kraj:</label><br>
  <select id="country" name="country" style="width:100%; padding:6px; margin-bottom:0; border-radius:4px; border:1px solid #aaa;">
    <option value="pl">Polska</option>
    <option value="de">Niemcy</option>
    <option value="us">USA</option>
  </select>

  <label for="resume">Dołącz CV:</label><br>
  <input type="file" id="resume" name="resume" style="margin-bottom:0;">

  <input type="submit" value="Wyślij" style="padding:6px 12px; background:#4CAF50; color:white; border:none; border-radius:4px; cursor:pointer; margin-right:8px;">
  <input type="reset" value="Wyczyść" style="padding:6px 12px; background:#f44336; color:white; border:none; border-radius:4px; cursor:pointer;">
</form>
</div>



## `<select>` — lista rozwijana

- `<select>` – tworzy rozwijaną listę opcji
- `<option>` – pojedyncza opcja w liście
- `<optgroup>` – grupuje opcje w sekcje (opcjonalnie)
- Atrybuty `<select>`:
    - `name` – nazwa pola formularza
    - `id` – identyfikator do powiązania z `<label>`
    - `size` – liczba widocznych opcji (jeśli `multiple` lub bez rozwijania)

---

### Przykład `<select>`

```html
<label for="country">Wybierz kraj:</label>
<select id="country" name="country">
  <option value="pl">Polska</option>
  <option value="de">Niemcy</option>
  <option value="us">USA</option>
</select>
```


<select id="country" name="country">
  <option value="pl">Polska</option>
  <option value="de">Niemcy</option>
  <option value="us">USA</option>
</select>


---

## Co to jest `placeholder`?

- Tekst podpowiedzi w polu formularza, **widoczny tylko gdy pole jest puste**  
- Nie zastępuje wartości `value`  
- Znika po wpisaniu danych  

### Przykład
```html
<input type="text" placeholder="Wpisz nazwę użytkownika">
```

### Różnica między `placeholder` a `value`
- `placeholder` – podpowiedź dla użytkownika, nie jest wysyłana jako wartość pola, znika po wpisaniu danych  
- `value` – faktyczna wartość pola, wysyłana w formularzu  

```html
<input type="text" placeholder="Podpowiedź" value="Domyślna wartość">
```

<div style="margin:10px 0; border-radius:12px; overflow:hidden; padding:16px; border:1px solid #ccc; max-width:400px;">
<label>Nazwa użytkownika z placeholder:</label><br>
<input type="text" placeholder="Wpisz nazwę"style="width:100%; padding:6px; border-radius:4px; border:1px solid #aaa;">
</div>

<div style="margin:10px 0; border-radius:12px; overflow:hidden; padding:16px; border:1px solid #ccc; max-width:400px;">
<label>Nazwa użytkownika z value:</label><br>
<input type="text" value="Wpisz nazwę"style="width:100%; padding:6px; border-radius:4px; border:1px solid #aaa;">
</div>