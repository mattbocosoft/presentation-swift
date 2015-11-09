#Collections  

Collections are built on top of a powerful set of [generic](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID179) functionality, and so can be initialized and manipulated as either generic or type-specific collections.  

Swift collections can be either mutable or immutable depending on whether the collection instance is assigned to a constant (let) or a variable (var). It's easy to add, remove or modify values in a mutable collection. There are many redundant methods of accessing, modifying and removing values from collections which are covered below.  

###Array  

*Creation*  
```
let myArray = [a, b, c, d] // Create a generic array and fill it with objects
let otherArray: [Int] = [] // Create an empty array that only holds Int's
```

*Retrieving values*  
```
myArray[3] // Returns the third item in the array

for item in myArray {
   // Iterate over all items in array
}

for (index, item) in myArray {
   // Iterate over all items in array
   // and simultaneously access index of each item using
   // a tuple (tuple-type covered below)
}
```

*Modifying or adding values*  
```
myArray.append(e)      // Add a variable 'e' to the array
myArray += e           // Add a variable 'e' to the array
myArray += otherArray  // Append all elements of 'otherArray' to myArray
myArray[0...2] = ["Hello", "Cheese", "Cake"] // Replace items at 0, 1, 2, 3 with new values
myArray.insert("Pie" atIndex: 0) // Insert "Torta" at index 0
```

*Removing values*
```
myArray.removeAtIndex(0) // Remove item at index 0
myArray.removeLast()     // Remove last item from array
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
