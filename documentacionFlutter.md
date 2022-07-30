# Seccion 6: Componentes de Flutter
## 60. Introduccion a la seccion
## 61. Temas puntuales de la seccion

En esta sección tocaremos temas sobre:
- Listviews
- ListTiles
- Listas y map
- Rutas
- Json hacia mapas
- Future Builder
- Lectura de archivos JSON
- Iconos
- Imágenes
- Avatars
- Loadings
- InfiniteScroll
- Pull to refresh
- Cards
- Sliders
- Y mucho más

El objetivo de esta sección, es comprender cómo se usa la documentación de Flutter y crear una aplicación que use muchos componentes de Flutter, los cuales te ayudarán cuando tengas que implementarlos en un futuro en tus aplicaciones.

## 62. Demostracion de la aplicacion - Componentes
## 63. Inicio de proyecto - Componentes
- Al crear un proyecto, podemos borrar todo el codigo por defecto ya que este contiene componentes inutilizables y podemos agregar cofigo suficiente con mateapp
- Con flutter select device podemos seleccionar el dispositivo para correr o ejecutar la aplicacion
```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false, // Se borra el debug, marca o etiqueta que aparece en la esquina del celular
      title: 'Material App',
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Material App Bar'),
        ),
        body: const Center(
          child: Text('Hello World'),
        ),
      ),
    );
  }
}
```
## 64. Listview - Mostrar una lista de elementos
- Con importM importamos el paquete de material
- Con fl-screen podemos agregar un codigo predeterminado ya que es un snipper

```dart
import 'package:fl_components/screens/listview1_screen.dart';
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
        debugShowCheckedModeBanner: false,
        title: 'Material App',
        home: Listview1Screen());
  }
}
```

```dart
import 'package:flutter/material.dart';

class Listview1Screen extends StatelessWidget {
  const Listview1Screen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: const Text('Listview Tipo 1'),
        ),
        body: ListView(
          children: const [
            Text('Hola Mundo'),
            Text('Hola Mundo'),
            Text('Hola Mundo'),
          ],
        ));
  }
}
```