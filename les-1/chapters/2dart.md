---
parent: Les 1 - Installeren en Dart
title: Dart
nav_order: 2
---

# Dart
Dart is een open-source programmeertaal die is ontwikkeld door Google. Het is vooral ontworpen om snelle, moderne apps te bouwen, zowel voor web, mobiel als desktop. De taal is objectgeoriënteerd, statisch getypeerd en voelt qua stijl aan als een mix van JavaScript, Java en TypeScript.

* Dart is ontwikkeld door Google, met de eerste versie gelanceerd in 2011.
* Oorspronkelijk bedoeld als vervanging/alternatief voor JavaScript in de browser.
* Sinds 2017 is Dart vooral bekend geworden als de taal achter Flutter, Google's UI framework voor cross-platform apps.
* Veilig en modern, met null safety en duidelijke types.
* Multiplatform: schrijf één codebase voor Android, iOS, web, desktop én zelfs backend.
* Eenvoudig te leren voor wie al bekend is met JavaScript, Java of C#.
* Dart wordt gecompiled naar native machine code (of javascript als je een webapp maakt), terwijl JS en PHP geinterpreteerde talen zijn. Dit houd wel in dat het een start punt nodig heeft (main())


## Variabelen
Dart is een *static typed* programmeertaal. Dat betekent dat elke variabel een **type** heeft.
```dart
    int age = 35;
```
We maken hier een variabele genaamd `age` aan, en geven deze de waarde van 35. We kunnen het datatype van age niet *aanpassen*. Wel overschrijven.
```dart
    int age = 35;
    age = "vijfendertig"; //Dit geeft een error
```

| Naam | Voorbeeld | Uitleg
| ---- | ----------- | ------- |
| integer  | `int leeftijd = 35;`    | Gehele getallen. Dit zijn getallen (positief of negatief) zonder een cijfer achter de komma (of punt). |
| String | `String naam = "Silvan"`     | Dit zijn lijsten van characters/tekens. Denk bijvoorbeeld aan woorden of zinnen. |
| boolean    | `bool isDocent = true`    | Booleans zijn true of false. Dit kan je eventueel ook binair weergeven |
| double | `double pi = 3.1` | Een double is een getal met een cijfer achter de komma. Lijkt op een float, maar is fundamenteel anders. Juda Hensen en Jelle Sjollema (en ChatGPT) kunnen dit uitleggen. |

### var

Dart kent ook het keyword `var`. Dan zeg je tegen de compiler *"zoek zelf maar uit welk datatype dit is"*. 

```dart
    var favZanger = "James Blunt"; 
```
Tijdens het compilen wordt favZanger een **string**. We kunnen van deze variabelen het datatype *niet meer veranderen*.

## Functies
Functies werken hetzelfde als in Java of C#, dus helaas heel anders dan in PHP of Javascript. Ze lijken eigenlijk ook een beetje op een variabelen. 

dart
{: .code-label }

```dart
int rollDice(){
  var rand = new Random();
  int dice = rand.nextInt(5)+1;
  return dice;
}
```
JavaScript
{: .code-label }
```js
function rollDice(){
    let dice = Math.ceil(Math.rand()*6);
    return dice;
}
let rollDice = (){
    let dice = Math.ceil(Math.rand()*6);
    return dice;
}
```


## Objecten
In dart kennen we de objecten die we uit Javascript kennen niet.
JavaScript
{: .code-label }
```js
let teacher = {name: "Silvan", age:35}
```


## If statements en loops

## Arrays en lists

## Null safety

## Quiz applicatie
