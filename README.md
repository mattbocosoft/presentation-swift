**CSCI 5828: Foundations of Software Engineering**  
*Fall 2015, Professor Kenneth Anderson*

Student: **Matthew Thomas**  
Presentation 4  

![swift-logo](images/swift-logo.png)  
# Swift Programming Language  

Swift is a relatively new programming language designed by [Chris Lattner](https://en.wikipedia.org/wiki/Chris_Lattner) and other developers at Apple. The language began to be developed in 2010 and was announced to the public in June 2014. Since then, the language has undergone many changes to harden its syntax and semantics through a series of public betas. Swift is the *eventual* replacement for Objective-C, the programming language that [NeXT](https://en.wikipedia.org/wiki/NeXT) began using it in the 1980s and Apple later began using when Apple acquired NeXT, however the two programming languages currently work hand in hand.    

Swift is multi-[paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) (e.g. Imperative, Functional, Object-Oriented, etc.) programming languages that has taken many of the best aspects of Objective-C and added safe programming patterns and modern features.  

One could write an entire book about the Swift programming language, and indeed Apple released *two* books on Swift available for free on the iBooks Store: [The Swift Programming Language](https://itunes.apple.com/us/book/the-swift-programming-language/id881256329?mt=11). This presentation is therefore not intended to cover every topic of Swift, but rather to serve as a quick reference guide on the basic syntax, semantics and high-level functionality of Swift aimed at those already well-versed in at least one other programming language. For developers who came from using Objective-C for their Xcode projects, the change will be easier than developers coming from other languages and environemnts. As mentioned previously, Swift borrows many of its core concepts from Objective-C.  

##The Basics of Swift  

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

**Optionals** are one of the most powerful features of Swift and contribute to the language's safety features:  

> Optionals say either “there is a value, and it equals x” or “there isn’t a value at all”.  
> Using optionals is similar to using nil with pointers in Objective-C, but they work for any type, not just classes.  
\- [Swift: The Basics](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID309)  

To read more about Optionals, check out the chapter on [Swift: The Basics](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID309) in Apple's book on Swift.  

###[Operators](operators.md)  

###[Collections](collections.md)  

###[Flow of Control](https://en.wikipedia.org/wiki/Control_flow)  

###Classes  

####Initializers  

Initializers do not return a value.
All stored non-optional properties must be initialized.

###Extensions  

###Protocols  

###Functions and Methods  

###Subclassing  

###Error Handling  

4 ways to handle errors
1. Propagating Errors Using Throwing Functions  
2. Handling Errors Using Do-Catch  
3. Converting Errors to Optional Values  
4. Disabling Error Propagation  

###Other Swift Tools  

To print out text, constants and variables to the console:  
`print("Hello there \(name)")`


##Resources  
[The Swift Programming Language](https://itunes.apple.com/us/book/the-swift-programming-language/id881256329?mt=11) [(*or View Online*)](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html#//apple_ref/doc/uid/TP40014097-CH18-ID203)  
[Using Swift with Cocoa and Objective-C](https://itunes.apple.com/us/book/using-swift-cocoa-objective/id888894773?mt=11)  
