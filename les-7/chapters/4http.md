---
parent: Les 7 - Dart
title: HTTP
nav_order: 4
---

# HTTP
Willen we een HTTP request maken (bijvoorbeeld zoals de Fetch in javascript) moeten we de HTTP package downloaden. Daarvoor moeten we eerst een `pubspec.yaml` aanmaken. Zet deze in dezelfde map als jouw `.dart` bestand.
```yaml
name: dartproj

environment:
  sdk: ^3.8.1
dependencies:

dev_dependencies:
```
Dit is een lege pubspec voor dart. Nu kunnen we packages downloaden.

## HTTP package downloaden
```
dart pub add http
```

## Maken van de request
Om een HTTP request te maken moeten we eerst een **Uri** maken
```dart
import 'package:http/http.dart' as http;;

void main() async {
  Uri url = Uri.parse("https://api.jikan.moe/v4/top/anime?type=tv&sfw=true");
  final response = await http.read(url);
  print(response);
}
```

En zo krijgen we alle informatie van de website binnen! Een heel groot blok tekst.

## Parsen naar JSON
We hebben nu een groot blok tekst dat we kunnen parsen naar *json*. Dit doen we met de `convert` package en de `jsonDecode` functie.

``` dart
import 'dart:convert';
import 'package:http/http.dart' as http;

void main() async {
  Uri url = Uri.parse("https://api.jikan.moe/v4/top/anime?type=tv&sfw=true");
  final response = await http.read(url);
  Map<String, dynamic> jsonData = jsonDecode(response);
  print(jsonData["data"][0]);
}
```

