#Classes  

Classes help developers abstract away complexity and expose a simplified interface on top of potentially complex logic. Swift uses a single implementation file (*classname.swift*) instead of two separate files (header and implementation).  

###Set-up  

Classes are declared with the `class` keyword. They contain a set of stored properties and methods and follow a standard structure:  
```
class Person {
  var name: String
  var age: Int?
  var position: Job

  func eat() {
  }
  
  func drink() {
  }
}
```

###Initializers  

Unlike in Objective-C, Swift initializers do not return a value. All stored non-optional properties must be initialized before the initializer chain is complete, otherwise a compile-time error will be generated.  

###Inheritance  

###Structures  

In Swift, Classes and Structures are almost identical. They both can contain properties, methods, conform to protocols and define initializers. Probably the most important difference between classe and structures is that class instances are passsed around by reference whereas structures are copied each time they are assigned. Also importantly, Classes support inheritance while structures are unable to inherit from other structures.  
