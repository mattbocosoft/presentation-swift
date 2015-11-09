#Collections  

Collections are built on top of a powerful set of [generic](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Generics.html#//apple_ref/doc/uid/TP40014097-CH26-ID179) functionality, and so can be initialized and manipulated as either generic or type-specific collections.  

Swift collections can be either mutable or immutable depending on whether the collection instance is assigned to a constant (let) or a variable (var). It's easy to add, remove or modify values in a mutable collection. There are many redundant methods of accessing, modifying and removing values from collections which are covered below.  

All the Collections below conform to the following operations:  
```
collection.isEmpty // Check if collection is empty
collection.count   // Return number of items in collection
collection.sort()  // Return the items in the collection (as an array) after sorting using the < operator"
```

##Array  

####Creation  
```
var myArray = [a, b, c, d] // Create a generic array and fill it with objects
var otherArray: [Int] = [] // Create an empty array that only holds Int's
var otherArray = [Int]()   // Create an empty array that only holds Int's
```

####Retrieving values  
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

####Modifying or adding values  
```
myArray.append(e)      // Add a variable 'e' to the array
myArray += e           // Add a variable 'e' to the array
myArray += otherArray  // Append all elements of 'otherArray' to myArray
myArray[0...2] = ["Hello", "Cheese", "Cake"] // Replace items at 0, 1, 2, 3 with new values
myArray.insert("Pie" atIndex: 0) // Insert "Torta" at index 0
```

####Removing values  
```
myArray.removeAtIndex(0) // Remove item at index 0
myArray.removeLast()     // Remove last item from array
```

You can append two arrays by using the addition operator '+':  
```
let bigArray = firstArray + secondArray
```

##Dictionary  

####Creation  
```
var myDictionary = [a : 0, b : 1, c : 2]    // Create a generic dictionary  
var otherDictionary: [String: Int] = [:]  // Create an empty dictionary of type [String: Int]
var otherDictionary = [String: Int]()       // Create an empty dictionary of type [String: Int]
```

Note that it is also possible to use other types besides Strings as a key in the dictionary. For example:  
```
var business = Business()
myDictionary[business] = [customer1, customer2, customer3]
```

####Retrieving values  
```
myDictionary[a] // Returns the value associated with the key a
```

Note that dictionaries do not have any explicit ordering, so you cannot depend on an ordering when iterating over key-value pairs unless you iterate over keys or values and sort the items using sort().
```
for (key, value) in myDictionary {
   // Iterate over all key-value pairs in dictionary
   print("\(key): \(value)")
}

for key in myDictionary.keys {
   // Iterate over all keys in dictionary
   print("Key: \(key)")
}

for value in myDictionary.values {
   // Iterate over all keys in dictionary
   print("Value: \(value)")
}
```

####Modifying or adding values  
```
myDictionary["cheese"] = 4   // Add or update the value 4 with key "cheese"
myDictionary.updateValue("cake", forKey: "cheese") // Update value "cake" for key "cheese"
```

####Removing values  
```
myDictionary["cake"] = nil               // Remove the key-value pair with key "cake"
myDictionary.removeValueForKey["cheese"] // Remove the key-value pair with key "cheese"
```

##Set  

####Creation  
```
var names = Set<String>() // Create an empty Set of type String
var otherNames: Set = []  // Create an empty generic Set
```

####Retrieving values  
```
names.contains("Amy") // Returns true if Set contains "Amy", otherwise returns false

for names in names {
   // Iterate over all items in the Set
   print("\(name)")
}
```

Set collections also do not conform to a specific ordering, so make sure to use sort() if you need to iterate over the elements in a specific order.  

####Modifying or adding values  
```
names.insert("Sami")  // Inserts value "Sami" into Set
```

####Removing values  
```
names.remove("Jacob")
```

####Set Operations  

The Set collection also provides a specialized Set of operations for Set manipulation which should be familiar.  

#####Creation  
```
a.intersect(b)   // Create new set by intersecting a and b
a.exclusiveOr(b) // Create new set by applying exclusive-or on a and b
a.union(b)       // Create new set containing all elements from a and b
a.subtract(b)    // Create new set by subtracting elements of b from a
```

#####Membership and Equality  
```
==
a.isSubsetOf(b)         // Return true if a is subset of (or equal to) b
a.isSupersetOf(b)       // Return true if a is superset of (or equal to) b
a.isStrictSubsetOf(b)   // Return true if a is subset of (but not equal to) b
a.isStrictSupersetOf(b) // Return true if a is superset of (but not equal to) b
a.isDisjointWith(b)     // Return true if a shares no values with b
```

##Tuple  
