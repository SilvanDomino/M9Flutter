---
parent: Les 1 - Installeren en Dart
title: Dart
nav_order: 2
---

# Dart

## Variabelen
Dart is een *static typed* programmeertaal. Dat betekent dat elke variabel een **type** heeft.
```dart
    int age = 35;
```
We maken hier een variabele genaamd `age` aan, en geven deze de waarde van 35. We kunnen het datatype van age niet *aanpassen*. Wel overschrijven.
```dart
    int age = 35;
    age = "vijfendertig" //Dit geeft een error
```

| Naam | Voorbeeld | Uitleg
| ---- | ----------- | ------- |
| integer  | `int leeftijd = 35;`    | Gehele getallen. Dit zijn getallen (positief of negatief) zonder een cijfer achter de komma (of punt). |
| String | `String naam = "Silvan"`     | Dit zijn lijsten van characters/tekens. Denk bijvoorbeeld aan woorden of zinnen. |
| boolean    | `bool isDocent = true`    | Booleans zijn true of false. Dit kan je eventueel ook binair weergeven |
| double | `double pi = 3.1` | Een double is een getal met een cijfer achter de komma. Lijkt op een float, maar is fundamenteel anders. Juda Hensen en Jelle Sjollema (en ChatGPT) kunnen dit uitleggen. |

### 

## Functies
In Dart hebben functies dezelfde syntax als in de op C gebaseerde talen. C++, C#, Java en een heleboel andere talen hebben deze syntax.

```dart
int getRandomNumber(){
    return 4;
}
```
Als eerst wordt verteld wat voor datatype de functie terug geeft. Daarna komt de naam van de functie en uiteindelijk de argumenten. 

```dart
void main(){
    //code here
}
```
Deze functie returned een void. Dat wil zeggen dat de functie niks terug geeft.

## Objecten
In javascript hebben we de volgende objecten:
```js
let docent = {name: "Silvan", age: 35}
```
Dit heb je in Dart niet. Objecten in dart gaan we in een latere les behandelen.

## If statements
Zelfde als JS en PHP.

## Loops
Zelfde als JS en PHP, alleen dan met datatype.

## Arrays en lists
In Dart bestaan er geen arrays. Er wordt specifiek gebruik gemaakt van **Lists**.
```js
let numbers = [1, 2, 56, 9.0, "negentien"];
```
Dit is een array in javascript waar onder andere ook getallen in staan.

```dart
List<int> numbers = [1, 5, 0, 34];
```
We maken een List aan, en in deze list passen alleen *integers*. 

[Volgend hoofdstuk: CLI Quiz](3quiz)