# Kaszanka.scss 
Celem projektu jest stworzenie biblioteki która zgodnie z zasadą DRY pozwala automatycznie generować niezbędę klasy na potrzeby projektu. Jednak by nie zwiększać niepotrzebnie pliku CSS będą generowane tylko i wyłącznie klasy potrzebne w danym projekcie.

## Spis funkcjonalności:
1. Aromatyczne generowanie ikonek mediów społecznościowych.
2. Dodanie do projektu klasa fixed-left/right analogicznych do tych występujących w bootstrapie.
3. Grid

### Komponenty 

#### Social Icon

Zmienna aktywacyjna - nadanie tej zmiennej wartości true aktywuję klasę (domyślnie false):
```
$social-icon-xxx: true;
```
##### Klasa w CSS:
```
btn-xxx
```
W miejsce xxx wstaw nazwę skrót medium społecznościowego z poniższej tabelki:

| lp | Skrót | Nazwa medium | 
| :---: | :-: | :-: | 
| 1 | fb | Facebook | 
| 2 | insta | Instagram | 
| 3 | yt | YouTube | 

Zmienna dodatkowa - Wielkość przycisku (z domyślną wartością 2rem):
```
$social-icons-size: 2rem;
```

#### Fixed

Zmienna aktywacyjna - nadanie tej zmiennej wartości true aktywuje klasę (domyślnie false):
```
$kasza-fixed: true;
```
##### Klasy w CSS:
```
.fixed-left
.fixed-right 
```
Zmienna dodatkowa - Z-index fixed (z domyślną wartością 1030):
```
$kasza-zindex-fixed: 1030;
```


#### Grid

Zmienna aktywacyjna - nadanie tej zmiennej wartości true aktywuje klasę (domyślnie false):
```
$kasza-grid: true;
```
Zmienna wprowadzająca ilość kolumn w grid:
```
$kasza-grid-column: 12;
```
Zmienna wprowadzająca breakpointy (wartość domyślna: sm: 576px, md: 768px, lg: 992px, xl: 1200px)
```
$kasza-grid-breakpoint: (
    sm: 576px,
    md: 768px,
    lg: 992px,
    xl: 1200px
);
```
Zmienne wprowadzające padding:
```
$kasza-grid-padding: 3%;
$kasza-grid-padding-col: $kasza-grid-padding/10;
```

##### Klasa w CSS:
Kontenery:
```
.container // wyśrodkowany kontener o szerokości zgodnej z breakpointem 
.container-full // kontener o szerokości strony 
```
Wiersze:
```
.row // wiersz z ułorzeniem elemntów w kolejność zgodnej z treścią 
.row-reverse // wiersz z odwrotnym ułorzeniem elemntów w kolejność zgodnej z treścią 
```
Kolumny (#{$i} - ilość kolumn z których składa się block, #{$name} - nazwa użyta w breakpointcie):
```
.col-#{$i}   //Kolumny nie zależne od użycia breakpointu np. col-2 
.col-#{$name}-#{$i}    //Kolumny których wyświetlanie ma się zmienić powyżej danego breakpointu
```

