---
parent: Les 7 - Dart
title: Lists en Maps
nav_order: 1
---

# Lists en Maps

## Lists
Een list is een array. Bij de Dart Lists moet je wel specifiek vertellen wat voor datatype er in de array zit.
```dart
List<String> names = ["Silvan", "Milos", "Bart", "Jasper"];
List<int> fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55];
var mixedList = ['Blink 182', 182, true]; // dit wordt gelezen als List<Object>
```

Of als we onze eigen classes gaan gebruiken:
```dart
class Car{
    constructor(brand, color, mileage){
        this.brand = brand;
        this.color = color;
        this.mileage = mileage;
    }
}
List<Car> cars = [Car("Honda", "red", 100), Car("Seat", "Orange", 2000), Car("Kia", "blue", 2321)];
```

### List functies
De List object heeft een heleboel functies die je kan gebruiken.
```dart
List<String> favoriteSongs = ['What\'s My Age Again?', 'Adam\'s Song', 'All the Small Things'];
// Access the first element
print(favoriteSongs[0]); // Output: What's My Age Again?
// Access the last element
print(favoriteSongs.last); // Output: All the Small Things
// Check if a list is empty
print(favoriteSongs.isEmpty); // Output: false
```

### List aanpassen
```dart
List<String> bandMembers = ['Tom', 'Mark', 'Scott'];
bandMembers.remove('Scott');
bandMembers.add('Travis');
print(bandMembers); // Output: [Tom, Mark, Travis, Matt]
bandMembers[0] = 'Matt';
print(bandMembers); // Output: [Tim, Mark, Travis]
```

### Loops
```dart
List<String> albums = ['Cheshire Cat', 'Dude Ranch', 'Blink-182', 'Neighborhoods'];
//Using a for-loop
for(int i = 0; i < albums.length; i++){
    print(albums[i]);
}
// Using a for-in loop
for (String album in albums) {
  print(album);
}
// Using forEach
instruments.forEach((item) => print(item));
```

## Maps
Een **Map** is een verzameling van *key-value* pairs, waarbij de key uniek is. De 'key' value **wijst** naar een specifieke value. Een Map lijkt eigenlijk heel veel op een object in Javascript.

### Aanmaken van een Map
```dart
// A Map where keys are strings and values are strings
Map<String, String> capitalCities = {
  'USA': 'Washington D.C.',
  'Japan': 'Tokyo',
  'France': 'Paris',
};

// A Map with different data types
Map<String, dynamic> user = {
  'name': 'Silvan',
  'age': 35,
  'isInstructor': true,
};
```