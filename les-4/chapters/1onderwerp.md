---
parent: Les 4 - Stateful Widgets
title: Stateful Widgets
nav_order: 1
---

# Stateless Widgets
Wanneer je een eigen widgets maakt, zijn er twee verschillende soorten widgets die je kan gebruiken. 

* Stateless Widgets
* Stateful Widgets

## Stateless Widgets
Stateless widgets zijn simpel. Ze hebben geen state, alleen een build functie. Soms een constructor als het nodig is.
```dart
class Greeting extends StatelessWidget {
  final String name; // like a "prop"

  const Greeting({super.key, required this.name}); //Consrtuctor

  @override
  Widget build(BuildContext context) {
    return Text("Hello $name");
  }
}
```

## Stateful Widgets
Deze widgets zijn veel complexer. Ze zijn te vergelijken met een React component met een state. De syntax voor deze widgets is wel echt een stuk complexer.

```dart
class Counter extends StatefulWidget {
  const Counter({super.key});

  @override
  State<Counter> createState() => _CounterState();
}


class _CounterState extends State<Counter> {
  int _count = 0;

  void _increment() {
    setState(() {
      _count++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Column(
      mainAxisSize: MainAxisSize.min,
      children: [
        Text("Count: $_count"),
        ElevatedButton(
          onPressed: _increment,
          child: const Text("Increment"),
        ),
      ],
    );
  }
}
```

De statefull widget bestaat uit 2 delen:
* De widget
* De state

Alleen Flutter is een beetje raar, de state heeft de build functie.
Verder lijkt de flutter state erg op de react state. SetState zorgt voor een rebuild. 

[Volgend hoofdstuk: React project aanmaken](2opdracht)