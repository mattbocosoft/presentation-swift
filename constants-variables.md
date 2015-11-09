#Constants and Variables  

**Constants** and **Variables** divide values into either mutable or immutable:  
```
let myImmutableNumber = 42 // Cannot be modified
var myMutableNumber = 24   // Can be modified
```

If you do not need to modify a variable after it is first set, then use a constant instead of a variable. The helps to ensure code-safety as well as removed unnecessary overheard associated with mutable variables.  

One unique feature of Swift is that constant and variable names can even contain unicode characters, opening up the door to Unicode:  

```
let π = 3.14159
let 你好世界 = "Hello World"
let 🌲 = "Evergreen"
```

**Optionals** are one of the most powerful features of Swift and contribute to the language's safety features. An optional can either say that there *is a value and it's x* or that the is no value present. Optional are similar to nillable pointers in Objective-C except that they apply to all Types, not just classes.

Declaring a constant or variable looks much like any other language:  
```
let name = "George"
var age = 7
```

Declare an *optional* constant or variable by a question mark (?) after the variable name:  
```
let name? = "George"
var possibleAge?
```

When the optional is referenced later in the code, it's important to handle the optionality using optional binding to determine where the option value is present:  
```
if let actualAge = possibleAge {
  // The age value is present
} else {
  // No age has been set
}
```

Optionals can be set back to nil `possibleAge = nil` while non-optionals *cannot be set to nil*.  

To read more about Optionals, check out the chapter on [Swift: The Basics](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID309) in Apple's book on Swift.  