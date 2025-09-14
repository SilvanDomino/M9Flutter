---
parent: Les 3 - Layouts en Widgets
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

## Opdracht: AboutMe constructor
Geef jouw AboutMe widget een constructor. De parameters voor de aboutMe worden:
* Naam
* Text
* Link naar afbeelding
* Achtergrond kleur

---

## Einde les 3
Dit is het einde van les 3. Volgende week aan de slag met Statefull widgets.