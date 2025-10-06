---
parent: Les 7 - Dart
title: Async
nav_order: 3
---

# Async

{: .note}
Bij Asynchroon programmeren ben je code aan het schrijven maar je weet niet (exact) hoe lang je op iets moet wachten, of meerdere dingen moeten tegelijk gebeuren. De code loopt dan niet meer *synchroon*.

We gaan hier behandelen
* Future
* Async
* Await

{: .small-note}
tl;dr: Futures zijn hetzelfde als Promises in javascript. Functies zijn alleen een beetje anders

In javascript gebruiken we Promises bij het asynchroon programmeren, in Dart heet een Promise een Future.

{: .code-label}
javascript voorbeeld

```js
async function PrintDelayed(){
    await new Promise(resolve => setTimeout(resolve, 2000));
    console.log("Hello world");
}
PrintDelayed();
```

In Dart is het als eerste belangrijk dat bij de functie gaat vertellen welk datatype de functie moet gaan returnen.
Een gewone functie die niks returned is
```dart
void PrintSomething(){
    //Code
}
```

Als we dit asynchroon willen maken, dan moeten we dit aanpassen. We gaan geen `void` returnen, maar iets wat **toekomstig** een void is. En we geven aan dat de functie async is.

```dart
Future<void> PrintDelayed() async{
    await Future.delayed(Duration(seconds: 2));
    print("Hello world");
}
```

## Then
Met de `then` functie van een *Future* kunnen we afwachten.

```dart
Future<int> DelayedInteger() async {
  await Future.delayed(Duration(seconds: 2));
  return Random().nextInt(255);
}

void main() {
  DelayedInteger()
  .then((returnedVal) {
    print(returnedVal);
  });
}
```

Maar je kan `then` ook niet gebruiken als je van leesbaardere code houdt. Daar gebruik je het await keyword voor om de gereturnde waarde op te wachten.

```dart
Future<int> DelayedInteger() async {
  await Future.delayed(Duration(seconds: 2));
  return Random().nextInt(255);
}

void main() async{
  int returnedVal = await DelayedInteger()
  print(returnedVal);
}

```
[Volgend hoofdstuk: HTTP request maken](4http)