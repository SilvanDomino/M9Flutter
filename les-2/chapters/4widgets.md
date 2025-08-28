---
parent: Les 2 - Eerste Flutter project
title: Widgets
nav_order: 4
---

# Widget

Een widget is in flutter een onderdeel van de app. *Elk* onderdeel van de app is een widget om precies te zijn.

## Twee soorten Widgets
Er zijn 2 soorten widgets: 
* Stateless widgets
    Deze worden gebruikt voor onderdelen die niet veranderen in hun eigen lifecycle.
* Stateful Widgets
    Deze worden gebruikt voor onderdelen van een applicatie die wel veranderen in zijn lifecycle.


---

## Eigen 
Laten we beginnen met het bouwen van onze eigen statische app. Kopieer de onderstaande code

main.dart
{: .code-label}

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
      ),
      home: const MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}

class MyHomePage extends StatelessWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(title),
        //Hier komt straks de body
      ), 
    );
  }
}
```
## Eerste stap: Hello World
Laten we als eerst iets toevoegen aan de body.

```dart
  body:Text("Hello world"),
```
We hebben de text "Hello world" toegevoegd aan de body. **Text** is een Widget die text weergeeft.

## Tweede stap: Centreren
Als we de text in de body willen centreren dan moeten we een Center widget gebruiken.
```dart
  body:Center(
    child: Text("Hello world"),
  )
```
**Center** is een widget wat zijn child widget centreert.

## Stap C: Tekst opmaken.
We hebben nu de tekst in onze app. Maar de kans is groot dat we de text willen aanpassen. Misschien willen we grotere tekst, of in een andere kleur.
Naast de **string** die het *text widget* laat weergeven, kunnen we ook nog meer argumenten mee geven. Wij gaan een style widget gebruiken om onze text te stylen.

```dart
child: Text(
  "Hello world",
  style: TextStyle(
    fontSize: 94, 
    color: Color(0xFF6200EE)),
),

```

### Kleur
Ik gebruik hier de Color class om de kleur mee te geven aan de stijl. Er zijn verschillende manieren om Color te gebruiken in Flutter. Hier gebruik ik de hex waardes om een kleur mee de geven. 

* `0x` : Deze waardes zijn hexadecimaal.
* `FF` : De Opacity.
* `6200EE` : De rgb waardes. Of de RRGGBB waardes, om het duidelijk te maken.

Bij deze Flutter/Dart kleuren kan je spreken van `0xFFRRGGBB`.

Een andere manier van kleur gebruiken is de voorgedefinieerde kleuren van Flutter te gebruiken.

```dart
Color ourColor = Colors.green;
Color ourShade = Colors.green[300];
```
Met de tweede kunnen we een verschillende soort groen gebruiken.

## Box
Om een mooie box te maken maken we gebruik van een *Container*.
<iframe width="600" height="400" src="http://www.youtube.com/embed/c1xLMaTUWCY" frameborder="0"></iframe>

```dart
  body:Center(          //we centreren de inhoud van de body
    child: Container(   //Daar komt een container
      child: Text("Hello world"),
    )
  )
```

Als we de container willen versieren, voegen we een de decoration toe.

```dart
child: Container(   //Daar komt een container
  child: Text("Hello world"),
  decoration: BoxDecoration(
    color: Colors.amber,
  ),
)
```

# Opdracht: Container versieren
Ga nu zelf de container versieren. Ik wil zien:
* **Border radius:** De randen worden mooi rond.
* **Padding:** Er moet afstand zijn tussen de text en de rand van de container.
* **Background:** Een gradient is wel een leuke achtergrond. 


## Einde les 2
Dit is het einde van les 2. Volgende week aan de slag met Layout en verder met Widgets en gaan we onze `AboutMe` widget maken.