---
parent: Les 7 - Dart
title: Dart Classes
nav_order: 1
---

# Dart
Dat heeft een paar belangrijke verschillen ten opzichte van Javascript.

## Classes
Als we in javascript een object willen aanmaken kunnen we dat op verschillende manieren doen.

```js
let car = {
    brand: "Honda",
    color: "Red",
    mileage: 200000
}
```
Of als we classes gaan gebruiken:
```js
class Car{
    constructor(brand, color, mileage){
        this.brand = brand;
        this.color = color;
        this.mileage = mileage;
    }
}
let car = new Car("Mazda", "Hotpink", 10000);
```

In Dart kan de eerste optie niet. Bij Dart *moet* alles een **datatype** hebben. Er is een workaround, dat is het gebruiken van een `Map<String, Object>`. Wat een map is wordt later uitgelegd.

```dart

class Car{
  String brand;
  String color;
  int mileage;
  Car(this.brand, this.color, this.mileage);
}
Car car = Car("Chrysler", "Green", 10000);
```

### Constructor
De constructor in Dart doet een hele boel automatisch. Deze heeft vaak niet eens een body nodig.

## Types
Er zijn heleboel speciale features voor Dart datatypes. De basis datatypes kennen we misschien wel.
```dart
    String name = "Silvan";
    int age = 35;
```

We kunnen nog meer eigenschappen meegeven aan een variabelen. 

### Type Safety
Datatypes kunnen niet van datatype veranderen na het compilen. `int age = "Silvan"` kan niet. Want int is een getal (int) geen string. 

* **Var**: Een variabele die als var wordt aangemaakt kan ieder datatype hebben, maar na het compilen staat het datatype vast. Daarna mag deze niet meer veranderen.
* **Dynamic**: Een variabele die als dynamic wordt aangemaakt kan iedere datatype hebben (net als react). Dit wordt vooral gebruikt voor als je van te voren niet weet wat voor data je hebt, zoals bijvoorbeeld bij JSON.

* **Null safety**: Variabelen kunnen in Dart standaard niet null zijn. Als je dat wel wilt doen moet je aangeven dat het *prima* is als een variabele null is. Dat doe je met `?`
```dart
String voornaam = "Silvan";
String? tussenvoegsel;
String achternaam = "Herrema";
```

### Onaanpasbaar keywords
* **final**: final kan maar 1x geset worden. Voor variabelen die niet veranderen wanneer ze geset worden.
* **const**: Deze variabelen zijn bekend bij het compilen. `const double pi = 3.14`.
* **late**: Met late geef je aan dat een variabele niet null is, maar deze later wordt geinitialiseerd. 


[Volgend hoofdstuk: Lists en maps](2listsenmap)