Na estrutura de pastas do flutter, utlizamos apenas a pasta lib para fazer as alterações no código, além dela, é importante ficar de olho no arquivo pubspec.yaml

O flutter utliza o dart como linguagem principal, e utiliza os widgets na sua estrutura e é equivalente a um componente do flutter, o que trás a clareza do desenvolvimento declarativo.
Tudo no flutter é Widgets
### Olá mundo no flutter

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    Container(
      child: Center(
        child: Text(
          "Olá mundo!",
          textDirection: TextDirection.ltr,
          style: TextStyle(color: Colors.black, fontSize: 50.0),
        ),
      ),
    ),
  );
}
```
