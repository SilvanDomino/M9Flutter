---
parent: Les 7 - Dart
title: HTTP
nav_order: 4
---

# HTTP
Willen we een HTTP request maken (bijvoorbeeld zoals de Fetch in javascript) moeten we de HTTP module downloaden. Daarvoor moeten we eerst een `pubspec.yaml` aanmaken.
```yaml
name: dartproj

environment:
  sdk: ^3.8.1
dependencies:

dev_dependencies:
```
Dit is een lege pubspec voor dart. Nu kunnen we modules downloaden.


```
dart pub add http
```

## Maken van de request
Om een HTTP request te maken moeten we eerst een **Uri** maken
```dart
void main() async {
  Uri url = Uri.parse("https://api.jikan.moe/v4/anime/170");
  final response = await http.read(url);
}
```

