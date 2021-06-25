Na estrutura de pastas do flutter, utlizamos apenas a pasta lib para fazer as alterações no código, além dela, é importante ficar de olho no arquivo pubspec.yaml

O flutter utliza o dart como linguagem principal, e utiliza os widgets na sua estrutura e é equivalente a um componente do flutter, o que trás a clareza do desenvolvimento declarativo.
Tudo no flutter é Widgets

#### Olá mundo no flutter

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

### Estados

#### StatelessWidget
Como o próprio nome diz, isso é um Widget sem estado, ou um Widget estático.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(AppWidget(title: "Stateless"));
}

class AppWidget extends StatelessWidget {
  final String title;

  const AppWidget({Key? key, required this.title}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Container(
      child: Center(
        child: Text(
          title,
          textDirection: TextDirection.ltr,
          style: TextStyle(color: Colors.black, fontSize: 50.0),
        ),
      ),
    );
  }
}
```

#### StatefulWidget

Diferente do StatelessWidget, utilizamos duas classes para compor um Widget Stateful, importante lembrar que para alterar o estado, deve-se utilizar a função setState

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(AppWidget(title: "Stateless"));
}

class AppWidget extends StatelessWidget {
  final String title;

  const AppWidget({Key? key, required this.title}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(primarySwatch: Colors.cyan),
      home: HomePage(),
    );
  }
}

class HomePage extends StatefulWidget {
  @override
  State<HomePage> createState() {
    return HomePageState();
  }
}

class HomePageState extends State<HomePage> {
  int counter = 0;

  @override
  Widget build(BuildContext context) {
    return Container(
      child: Center(
        child: GestureDetector(
          child: Text("Contador: $counter"),
          onTap: () {
            setState(() {
              counter++;
            });
          },
        ),
      ),
    );
  }
}
```
