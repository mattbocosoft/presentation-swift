#Collections  

Collections are built on top of a powerful set of [generic](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID179) functionality, and so can be initialized and manipulated as either generic or type-specific collections.  

Swift collections are mutable by default, so it's easy to add, remove or modify values in the collection.  

###Array  

*Creation*  
```
let myArray = [a, b, c, d] // Create a generic array and fill it with objects
let otherArray: [Int] = [] // Create an empty array that only holds Int's
```

*Retrieving values*  
```
myArray[3] // Returns the third item in the array
```

*Modifying or adding values*  
```
myArray.append(e)      // Add a variable 'e' to the array
myArray += e           // Add a variable 'e' to the array
myArray += otherArray  // Append all elements of 'otherArray' to myArray
myArray[0...2] = ["Hello", "Cheese", "Cake"] // Replace items at 0, 1, 2, 3 with new values
```

*Removing values*
```
myArray.removeAtIndex(0) // Remove item at index 0
```

You can append two arrays by using the addition operator '+':  
```
let bigArray = firstArray + secondArray
```

###Dictionary  

*Creation*  
```
let myDictionary = [a : 0, b : 1, c : 2]  
```

*Retrieving values*  
```
myArray[a] // Returns the value associated with the key a
```

*Modifying or adding values*  
```
myDictionary["cheese"] = 4   // Add or update the value 4 with key "cheese"
myDictionary["cake"] = nil // Remove the key-value pair with key "cake"
```

Note that it is also possible to use other types besides Strings as a key in the dictionary. For example:  
```
let business = Business()
myDictionary[business] = [customer1, customer2, customer3]
```

###Set  

###Tuple  
