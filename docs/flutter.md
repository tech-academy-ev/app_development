# Introduction to Flutter

Flutter is an open source UI development kit from Google. Flutter can be used to develop cross-platform apps in the Dart programming language. A Flutter program should be able to run on the following target platforms without major adjustments: WebApp, Android, iOS, Windows, Linux, macOS, and Google Fuchsia. Flutter itself is written in C++ and uses the Dart Virtual Machine (Dart VM), as well as the Skia graphics library.

## Differentiation from other frameworks

One of the ways Flutter differs from other frameworks is that it does not use WebView or OEM widgets, which are pre-installed on the end device. When a Native App interacts with the platform to create a widget, it typically accesses the OEM (Original Equipment Manufacturer) widgets on the smartphone or tablet. Flutter eliminates this intermediate step. Instead, the framework uses its own high-performance render engine, Skia, to create the necessary widgets. The open source graphics library for creating 2D graphics connects via interfaces with the respective existing, operating system-dependent, native software development kits.

Flutter is executed using ahead-of-time compilers (AOT compilers). Only in the development phase, just-in-time compilers (JIT compilers) are used for faster testing processes. Each app based on Flutter is composed of container, text, image, icon and other widgets, which are individually interpreted and displayed on a canvas element powered by the Skia graphics library. The platform then analyzes the widgets constructed in this way and forwards the events provoked by the end user's interaction to the app.

## Architecture

The framework is essentially constructed from three process units. 

<figure markdown>
  ![Flutter Architecture](./images/archdiagram.png){ width="auto" }
  <figcaption><small>Source: https://docs.flutter.dev/resources/architectural-overview</small></figcaption>
</figure>

### Embedder
At the lowest level and at the heart of the engine, platform-specific embedders are defined. Their job is to connect the rendering with the native screen information, input events, etc. For this purpose, the embedders interact with the engine layer via simple C/C++ APIs. However, these APIs are only mapped internally. This layer is composed of a shell, a human-machine interface, that hosts Dart's virtual machine (DartVM). This shell is platform-specific and provides access to the associated native APIs. They implement OS-specific code, such as communication with the app's Input Method Editor (IME) and lifecycle events. The actual architecture, however, consists of two elements: the engine and the framework.

### Engine
Flutter's middle layer, written in C/C++, contains a variety of components that are crucial to the functionality of the framework and its basic operation. These include the Skia graphics engine and shells, which are accessed through APIs represented by the dart:ul library. Using the defined classes in this library, such as Canvas, Paint and TextBox, it is possible to visually design an app.

### Framework
This is the most important layer that hosts all the libraries and packages necessary to develop an app. The framework is the component that is programmed in Dart and which you need to know. In this section, the operations for creating widgets, for instance, are located. You, as a developer, do not need to know much about the embedder and engine unit. To develop fast and beautiful apps, you only need to know the framework. In the FLutter framework, everything is a widget. A widget is a basic component in a Futter app, which in turn can itself consist of other widgets. A widget bundles logic, interaction, and presentation within an object.There are a number of pre-built widgets that map familiar and often needed interactions, such as buttons, lists, checkboxes, tabs, and so on. Flutter does not use the widgets of the respective platform, but implements them itself. Before we dive deeper into the flutter framework and its syntax, let us consider the programming language dart and its syntax.

## Dart Syntax

​​Dart is an open-source, general-purpose, object-oriented programming language with C-style syntax developed by Google in 2011. The purpose of Dart programming is to create a frontend user interface for the web and mobile apps. It is inspired by other programming languages such as Java, JavaScript, C#, and is Strongly Typed. Since Dart is a compiled language so you cannot execute your code directly; instead, the compiler parses it and transfers it into machine code. If you know javascript, dart is very easy to learn. Dart supports most of the common concepts of programming languages like classes, interfaces, and functions. 

You do not need to know dart in detail to build a flutter app. Actually, you can even pick up dart while learning flutter and you do not have to learn dart before. However, knowledge of the programming language will help you develop apps.

### Variables and Constants
``` dart linenums="1"
main() {
    var dog1 = "Max"; // this is a variable

    // a variable can be final, which means that it must be initialized. Once assigned a  value, a final variable's value cannot be changed.
    final maleDogs = ["Milo"]; // mutable single-assignment variable
    maleDogs.add("Cooper"); // ✅ this is allowed (you can add an element to the list)
    maleDogs = ["Cooper"]; // ❌ this is not allowed (you cannot reassign the variable)

    const femaleDogs = ["Luna", "Bella"]; // compile time constant
    femaleDogs.add("Winona"); // ❌ this is not allowed (you cannot change the variable)
    femaleDogs = ["Winona"]; // ❌ this is not allowed  
}
```
### Null and Conditions
In Dart, undefined values are null. Expressions in conditionals may only be boolean.
``` dart linenums="1"
main() {
    var collar = false,
    toys = null,
    amountOfMeals = 0 / 0, // NaN
    owner = "",
    age = 0,
    breed;

    if (!collar) print('bark'); // bark (means: if not false → if true)
    // same as: 
    if (!collar) {print('bark');} // bark 

    if (toys == null) print('bark'); // bark (checks if toys is null)
    if (amountOfMeals.isNaN) print('bark'); // bark
    if (owner.isEmpty) print('bark'); // bark (the string is empty)
    if (age == 0) print('bark'); // bark (checks if age is zero)
    if (breed == null) print('bark'); // bark (checks if breed is null) 
}
```
### Collection literals
An Array in Javascript is a List in Dart. An Object in Javascript is a Map in Dart.
``` dart linenums="1"
main() {
    var dogList = ["Lucy", "Cooper", "Zeus"];
    var dogMap = {
        'first': "Lucy",
        'second': "Cooper"
    }; // could use #first symbol instead
    var dogSet = {"Lucy", "Cooper", "Zeus"};

    print(dogList.length); // 3
    print(dogMap.length); // 2
    print(dogSet.length); // 3  
}
```
### Object-oriented Classes
An Array in Javascript is a List in Dart. An Object in Javascript is a Map in Dart.
``` dart linenums="1"
class Dog { // Class “Dog”
    final String name; // variable name of type String
    final int phone; // variable phone of type integer
    Dog(this.name, {this.phone}); // example of unnamed and named parameter

    tag() => "${name}\nIf you found me please call ${phone}!";
}

main() {
    print(Dog('Luna', phone: 6198887421).tag());
    // Luna
    // If you found me please call 6198887421!
}
```
## Flutter Syntax
As soon as you create a new flutter project, the flutter “Hello-world” project will be displayed. The Flutter hello-world project is a very simple counter app. You can press a button to increase the counter and the current count is displayed in the middle of the screen. We added the source code and our own comments to the guide to help you understand the minimum-viable app source code. Please read the comments carefully.
``` dart linenums="1"
// import flutter component
import 'package:flutter/material.dart';

// when run code, trigger the function main()
// main runs the widget “MyApp”
void main() => runApp(MyApp());

// 1. Widget is stateless (can only have one state, cannot change state)
class MyApp extends StatelessWidget {
    // Widget contains "build()" method
    @override
    Widget build(BuildContext context) {
        // the build method returns the widget MaterialApp
        // MaterialApp is only used once in a flutter application
        // you should always add this widget at the beginning of the application
        // as it provides many useful features, such as theming
        return MaterialApp(
            // title of the app
            title: 'Flutter Demo',
    
            // do not show a debug banner
            debugShowCheckedModeBanner: false,

            // defining the color of the theme
            theme: ThemeData(
                primarySwatch: Colors.blue,
            ),

            // the widget MaterialApp contains the app “MyHomePage”
            home: const MyHomePage(),
        );
    }
}

// 2. Widget is stateful (it can have multiple states)
class MyHomePage extends StatefulWidget {
    // this is the constructor
    // you can provide a key to the MyHomePage widget if you use this widget multiple 
    // times across your app. If you do that, the framework knows, that it is
    // the same widget and has not to create a new “MyHomePage”-Widget
    // however, you do not need to provide a key.
    const MyHomePage({
        // type “Key”. The “?” indicates that it is nullable
        Key? Key,
        // this is the super constructor. If a key is provided to the widget, the 
        // the super constructor will transfer the key to the widget “Stateful”
    }) : super(key: key);

    // we override the state of the widget “StateFulWidget”
    // we create an own state for our stateful widget “MyHomePage”
    @override
    _MyHomePageState createState() => _MyHomePageState();
}

// this part of the widget describes the state of the widget
class _MyHomePageState extends State<MyHomePage> {

    // initially, the variable “_counter” is 0.
    int _counter = 0;

    // this is a method that does not return anything (=void)
    void _incrementCounter() {

        // when the method is called: we tell the widget to update the state
        setState(() {
            // the variable _counter is increased by one
            _counter = _counter + 1;
        });
    }



    @override
    Widget build(BuildContext context) {
        // this build method returns the “Scaffold” widget
        // the scaffold widget should only be used once per page
        return Scaffold(
            // it provides a scaffold, in which we can easily add an Appbar
            appBar: AppBar(
            title: const Text('Flutter Demo Home Page'),
        ),
        // the center widget
        body: Center(
            // contains a column. A column can have multiple widgets below each other
            child: Column(
                // we want to have the text widgets within the column widget
                // centered horizontally
                mainAxisAlignment: MainAxisAlignment.center,
                children: [
                    // displaying a text widget
                    const Text(
                        'You have pushed the button this many times:',
                    ),
                    // displaying another text widget
                    Text(
                        // this is the variable as string
                        '$_counter',
                        // we can define a style here. This uses the default text theme of      headline 6
                        style: Theme.of(context).textTheme.headline4,
                    ),
                ],
            ),
        ),
            // the scaffold widget can (!) also have a floating action button
            floatingActionButton: FloatingActionButton(
            
                // when the button is pressed, the method _incrementCounter is triggered
                onPressed: _incrementCounter,
            
                // the button contains an icon with the iconData “Icon.add”
                child: const Icon(Icons.add),
            ),
        );
    }
}
```
