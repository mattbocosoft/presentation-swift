#Classes  

Classes help developers abstract away complexity and expose a simplified interface on top of potentially complex logic. Swift uses a single implementation file (*classname.swift*) instead of two separate files (header and implementation).  

###Set-up  

Classes are declared with the `class` keyword. They contain a set of stored properties and methods and follow a standard structure:  
```
class Person {
  var name: String
  var age: Int?
  var position: Job

  init() {
  }

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

Stored properties can also be initialized with a **default property value** when initially declared.  

```
class Person {
  var name: String
  var age: Int? = 0

  ...
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

Initializers can accept parameters, which are commonly used to set the values of the stored properties. These parameters can be provided with an external name which preceeds the parameter name or can opt-out of the external name by using an underscore ('_') instead.    

```
class Person {
  var name: String
  var age: Int?
  var position: Job

  init(_ name: String, personJob job: Job) {
    self.name = name
    self.position = job
  }
}
```

###Functions and Methods  

Functions are made of a name, optional parameters, and an optional return type. Below is the structure of a Swift function:  

```
func otherFun(personName: String) -> Bool {
  // Function with Bool return type and one parameter called 'personName' of type String
  return true
}
```

The return value can be left out and the parameters are optional.  

```
func myFunc() {
  // Function with no return type and no parameters
}
```

Swift Functions can even return multiple values at once using Tuples.  

```
func nameAge(person: Person) -> (name: String, age: Int) {
  return (person.name, person.age)
}

let retVal = nameAge(person)

// The tuple values can be referenced by name
print("Name: \(retVal.name)")
print("Age: \(retVal.age)")
```

**External parameter names** can be used to make the function more expressive when used. By default, the first parameter does not use an external name and the second and subsequent parameters use their local name as their external name, however you can use a different external name for each parameter:  
```
func printName(of person: Person and otherPerson: Person) {
  print("Hello \(person.name) and \(otherPerson.name)")
}

// External parameters names must *always* be used when calling the function
printName(of: Fred and: Bob)
```

**Variadic parameters** can be used to accept a dynamic number of parameters that function like an array:  
```
func sumAll(numbers: Int...) -> Int {
  var sum: Int = 0
  for number in numbers {
    sum += number
  }
  return sum
}

// Call a function with variadic parameters by separating parameters with commas
sum(1, 2, 3, 5, 8)
```

**Variable parameters** are copied into a variable to that they can be modified in the body of the function, as opposed to the standard constant parameters which cannot:  
```
func addQuotes(var string: String) -> String {
  string = "\"" + string + "\""
  return string
}
```

**Inout parameters** can be used to modify values outside the scope of a function's body without requiring a return value. The function needs to mark the parameter as inout and the caller needs to explicitly give the function permission to modify the variable by adding an ampersand before the passed-in variable. Note that only variables and not constants can be passed in as inout parameters.  
```
var count: Int = 2

func multiplyByTwo(inout a: Int) {
  a *= 2
}

multiplyByTwo(&count)
// Count is now 4
```

All Swift Functions have types so they can be passed around as parameters.  
```
// This function's type is (String) -> String
func hello(name: String) -> String {
  return "Hello \(name)"
}

func printResult(stringFunction: (String) -> String, name: String) {
  print(stringFunction(name))
}

printResult(hello, "Roger")
// "Hello Roger" will be printed out on the Console
```

**Function Types** can even be returned as value by other functions:  
```
func greetEnglish(name: String) -> String {
  return "Hello \(name)"
}

func greetChinese(name: String) -> String {
  return "你好\(name)"
}

func chooseGreetingFunction(english: Bool) -> (String) -> String {
  if english {
    return greetEnglish
  } else {
    return greetChinese
  }
}
```

Lastly, functions can be nested within each other. Below uses the same example as above but using nested functions:  
```
func chooseGreetingFunction(english: Bool) -> (String) -> String {

  func greetEnglish(name: String) -> String { return "Hello \(name)" }
  func greetChinese(name: String) -> String { return "你好\(name)" }

  if english {
    return greetEnglish
  } else {
    return greetChinese
  }
}
```

###Inheritance and Subclassing  
Subclassing in Swift is similar to Objective-C. Use a colon and the name of the class you'd like to subclass:
```
class Language {
  // Base class
  var name: String
  var languageFamily: String
}

class Chinese: Language {
  // Subclass
}
```

Subclasses inherit characteristics such as properties, methods, and conformed protocols from the base class. A subclass can override functions from its base class, but the subclass must explicitly declare the override intention using the 'override' keyword in front of the function name.  
```
class Language {
  // Base class
  var name: String
  var languageFamily: String
  
  func helloWorld() {
    print("Override me!")
  }
}

class Chinese: Language {

  override func helloWorld() {
    print("你好世界")
  }
}
```

Subclasses can call the base-class implementation of a overriden method by calling 'super' just like in Objective-C.  
```
class Chinese: Language {

  override func helloWorld() {
    super.helloWorld()
    print("你好世界")

    // This method prints out two lines:
    // "Override me!"
    // "你好世界"
  }
```

If characteristics of the base class such as properties or method should *not* be overriden, then use the **final modifier**.
```
class Language {
  // Base class
  var name: String
  var languageFamily: String
  
  func helloWorld() {
    print("Override me!")
  }
  
  final func universalGreeting() {
    print("Hi!")
  }
}
```

###Structures  

In Swift, Classes and Structures are almost identical. They both can contain properties, methods, conform to protocols and define initializers. Probably the most important difference between classe and structures is that class instances are passsed around by reference whereas structures are copied each time they are assigned. Also importantly, Classes support inheritance while structures are unable to inherit from other structures.  

Structures can also use "memberwise initializers" when creating structure instances.  


**Previous**: [Flow of Control](control-flow.md)  
**Next**: [Extensions](extensions.md)  
Return to the [homepage](README.md).
