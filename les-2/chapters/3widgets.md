---
parent: Les 2 - Eerste Flutter project
title: Widgets
nav_order: 3
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
We hebben de text "Hello world" toegevoegd aan de body.

## Tweede stap: Centreren
Als we de text in de body willen centreren dan moeten we een Center widget gebruiken.
```dart
  body:Center(
    child: Text("Hello world"),
  )
  
```

## Einde les 2
Dit is het einde van les 2. Volgende week aan de slag met Layout en verder met Widgets.