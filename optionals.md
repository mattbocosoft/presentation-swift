#Optionals and Optional Chaining  

Optionals are one of the most powerful and safe features of Swift. An optional value means that the value may or may not be present.  

> Optionals say either “there is a value, and it equals x” or “there isn’t a value at all”.  
> Using optionals is similar to using nil with pointers in Objective-C, but they work for any type, not just classes.  
\- [Swift: The Basics](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID309)  

Constants and Variables divide values into either mutable or immutable:  
```
let myImmutableNumber = 42 // Cannot be modified
var myMutableNumber = 24   // Can be modified
```

If you do not need to modify a variable after it is first set, then use a constant instead of a variable. The helps to ensure code-safety as well as removed unnecessary overheard associated with mutable variables.  
