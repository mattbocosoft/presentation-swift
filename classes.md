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

Unlike in Objective-C, Swift initializers do not return a value. All stored non-optional properties must be initialized before the initializer chain is complete, otherwise a compile-time error will be generated. So for the example above, name and position must be initialized in init.  

```
class Person {
  var name: String
  var age: Int?
  var position: Job

  init() {
    name = "Tom"
    position = Job.Developer
  }
}
```

Swift classes can also implement deinitializers whose job is the exact opposite of initializers; to tear down an object after it's no longer needed.  

```
class ShopKeeper {
  init() {
    shop.Open()
  }
  deinit() {
    shop.CloseUp()
  }
}
```

###Inheritance  



###Structures  

In Swift, Classes and Structures are almost identical. They both can contain properties, methods, conform to protocols and define initializers. Probably the most important difference between classe and structures is that class instances are passsed around by reference whereas structures are copied each time they are assigned. Also importantly, Classes support inheritance while structures are unable to inherit from other structures.  
