---
parent: Les 1 - Installeren en Dart
title: CLI Quiz
nav_order: 3
---

# Opdracht: Command line Interface (CLI) Quiz
Maak een CLI quiz met 5 vragen. In de cmd/terminal komt een vraag te staan, en geef de gebruiker feedback als deze een juist of onjuist antwoord invult.

Hieronder een voorbeeld hoe je input kan gebruiken.

```dart
import 'dart:io';
void main(){
    String inp1 = stdin.readLineSync()!;
    if (inp1.toUpperCase() != "D") {
        print("Wrong answer");
    } else {
        print("Correct!");
    }
}
```

Hieronder een voorbeeld van de output.

```cmd
Who's your favorite teacher?
A: Jasper 
B: Martijn 
C: Bart
D: Silvan
d
Correct!
```

Maak een quiz met 5 vragen en antwoorden. 

---

## Dit is het einde van de les
Volgende les gaan we aan de slag met onze eerste flutter project.
