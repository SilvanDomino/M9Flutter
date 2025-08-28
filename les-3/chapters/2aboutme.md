---
parent: Les 3 - Layouts en Widgets
title: About Me Widget
nav_order: 2
---

# Eerste Widget
We gaan onze eerste widget maken, en het wordt weer een 'AboutMe' widget. 
![](../images/aboutme.png)

# Stap 1: Lege widget
We maken eerst een nieuw bestand aan genaamd `AboutMe.dart`, dit zetten we naast de `main.dart` in de **lib** map.
```dart
import 'package:flutter/material.dart';
class AboutMe extends StatelessWidget {
  const AboutMe({super.key});

  @override
  Widget build(BuildContext context) {
    return Container(
        child: Text("About Me!")
    );
```