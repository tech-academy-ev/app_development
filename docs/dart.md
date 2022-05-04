# Introduction to Dart

The Dart language is present at the core of the Flutter framework and is used to code the Flutter applications. Dart is an open-source general-purpose programming language. It is originally developed by Google and later approved as a standard by ECMA. Dart is one of the very few programming languages that support both Just-In-Time (JIT) and Ahead-Of-Time (AOT) compiling, which makes it ideal for Flutter's development pruposes. Dart’s Just-in-Time (JIT) Compilation loads the source code and converts it to the native machine code using the Dart’s VM on the fly. 

JIT compilation enables important features, like, hot reload/restart/debugging feature that helps us to quickly and efficiently experiment with UIs and bug fixes without losing application state. This compilation process increases the speed and runtime of the application. The JIT compiler also speeds up the Flutter app development process.

Ahead-of-Time (AOT) compilation comes into the picture when the flutter app is ready for production. When the app loads on the device the AOT compiles the flutter libraries to native ARM or X64 Machine code. The AOT Compiled app runs the app smoothly, provides better performance, minimum size, and removes dependencies needed for the development environment.


## Dart Syntax

​​Dart is an open-source, general-purpose, object-oriented programming language with C-style syntax developed by Google in 2011. The purpose of Dart programming is to create a frontend user interface for the web and mobile apps. It is inspired by other programming languages such as Java, JavaScript, C#, and is Strongly Typed. Since Dart is a compiled language so you cannot execute your code directly; instead, the compiler parses it and transfers it into machine code. If you know javascript, dart is very easy to learn. Dart supports most of the common concepts of programming languages like classes, interfaces, and functions. 

You do not need to know dart in detail to build a flutter app. Actually, you can even pick up dart while learning flutter and you do not have to learn dart before. However, knowledge of the programming language will help you develop apps.

### Variables and Data Types
``` dart linenums="1"
main() {
    var dog1 = "Max"; // this is a variable
    String dog1 = "Max"; // declare a string --> try to always declare the type of your variable
    int dogAge = 12;
    double dogFoodPrice = 12.99;

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

