---
parent: Les 4 - Listview en arguments
title: Parameters
nav_order: 2
---

# Constructor Parameters
Bij React hadden we props zodat een parent component gegevens kon doorgeven aan een child component. Bij andere programmertalen gebruiken we daar **Constructor parameters** voor. 
Constructors vind je terug in letterlijk elke programmeertaal met classes. Deze bepaald met welke eigenschappen een class aangemaakt wordt.

## Dart
```dart
class Vector2d{
    final int x;
    final int y;
    const Vector2d({required this.x, required this.y}); //Consrtuctor
}

void main(){
    Vector2d pos = Vector2d(x:10, y:10);
}
```

## Flutter
```dart
class Greeting extends StatelessWidget {
  final String name; // like a "prop"

  const Greeting({super.key, required this.name}); //Consrtuctor

  @override
  Widget build(BuildContext context) {
    return Text("Hello $name");
  }
}

//in een andere widget ofzo:
child:Greeting(name:"Silvan");
```

## Opdracht: Top10
Maak een **Top10 Widget** waarbij je jouw top 10 weergeeft. De top 10 kan van alles zijn. Favorite sporthelden, boeken, TV series, pokemon, video games, anime. Bedenk het zelf maar. 
Maak hier bij gebruik van een aparte widget voor ieder element zoals in het volgende voorbeeld: 
```dart
Widget build(BuildContext context) {
    return ListView(
      padding: const EdgeInsets.all(8),
      children: [
        Book(author: "Brandon Sanderson", title: "The Way of Kings"),
        Book(author: "Brian K. Vaughn", title: "Saga"),
        Book(author: "Natsume Akatsuki", title: "Konosuba Volume 4"),
        Book(author: "Patrick Rothfuss", title: "The Name of the Wind"),
        Book(author: "Hajime Isayama", title: "Attack on Titan, Vol. 1"),
        Book(author: "Terry Pratchett", title: "Guards! Guards!"),
        Book(author: "Hiromu Arakawa", title: "Fullmetal Alchemist, Vol. 1"),
        Book(author: "Naoko Takeuchi", title: "Sailor Moon, Vol. 1"),
        Book(author: "Neil Gaiman", title: "American Gods"),
        Book(author: "Kazu Kibuishi", title: "Amulet, Vol. 1"),
      ]
    );
  }
```

### Leerdoel
Leerdoel is het gebruiken van de listview widget en het maken van stateless widgets.

### Extra: Array
In plaats van alle onderdelen individueel te maken, ga kijken of je de auteurs en titels in een array kan zetten, zoals je ook in React hebt gedaan.

---

## Einde les 3
Dit is het einde van les 3. Volgende week aan de slag met Statefull widgets.