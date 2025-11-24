
## Podstawowe właściwości

- **background-color** – ustawia kolor tła elementu. 
<div style>
	Hello
</div>
    
- **background-image** – pozwala dodać obraz jako tło (np. `url("img.png")`).
    
- **background-repeat** – określa sposób powtarzania obrazu tła (`repeat`, `no-repeat`, `repeat-x`, `repeat-y`).
    
- **background-position** – definiuje pozycję tła (np. `center`, `top right`, wartości procentowe lub piksele).
    
- **background-size** – kontroluje rozmiar obrazu tła (`auto`, `cover`, `contain`, wartości jednostkowe).
    
- **background-attachment** – opisuje, czy tło ma przewijać się z treścią (`scroll`) czy być nieruchome (`fixed`, `local`).
    

## Właściwości zaawansowane

- **background-origin** – określa obszar, na podstawie którego ustawiana jest pozycja tła (`padding-box`, `border-box`, `content-box`).
    
- **background-clip** – określa obszar, w którym tło jest widoczne (`border-box`, `padding-box`, `content-box`, `text`).
    
- **background-blend-mode** – pozwala na łączenie warstw tła podobnie jak tryby mieszania w programach graficznych (np. `multiply`, `screen`).
    

## Skrótowa właściwość `background`

Można ustawić wiele właściwości jednocześnie:

```css
background: url("img.png") no-repeat center/cover fixed;
```

Kolejność parametrów:

1. background-color
    
2. background-image
    
3. background-repeat
    
4. background-attachment
    
5. background-position / background-size
    

## Tła wielowarstwowe

Możesz łączyć wiele obrazów tła:

```css
background-image: url("warstwa1.png"), url("warstwa2.svg");
background-position: center, top left;
background-size: cover, 50px;
```

Warstwy są renderowane od góry do dołu (pierwsza jest najwyżej).