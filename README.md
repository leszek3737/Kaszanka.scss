# Kaszanka.scss
Celem projektu jest stworzenie biblioteki która z godnie z zasadą DIR pozwoli automatycznie generować nie zbędę klasy na potrzeby projektu. Jednak by nie zwiększać nie potrzebnie pliku CSS będą generowane tylko i wyłącznie klasy potrzebne w danym projekcie.

## Spis funkcji:
1. Aromatyczne generowanie ikonek mediów społecznościowych.
2. Dodanie do projektu klasa fixed-left/rigcht analogicznych do tych występujących w boostrapie.

### Komponenty 

#### Social Icon

Zmienna aktywacyjne - nadanie tej zmiennej wartości true aktywuję klasę (domyślnie false):
```
$social-icon-xxx: true;
```
klasa w CSS:
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

Zmienna aktywacyjne - nadanie tej zmiennej wartości true aktywuje klasę (domyślnie false):
```
$kasza-fixed: true;
```
klasy w CSS:
```
.fixed-left
.fixed-right 
```
Zmienna dodatkowa - Z-index fixed (z domyślną wartością 1030):
```
$kasza-zindex-fixed: 1030;
```