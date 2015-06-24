# eldil-lang
A programming language that I might develop if I have time. Similar to Apple's Swift. But fixing some of the things I don't like about it.

Some examples:

```
import module Math // Import module requires you to refer to the module by its name.
                   // You can also do: import module some.long.mod.name as shorterName.

class Person {
    var name: String, age: Int, profession: String
    
    // Long initializer syntax. 
    initialize(name: String, age: Int, profession: String) {
      self.name = name
      self.age = age
      self.profession = profession
    }
    
    // Or you could do it as:
    // initialize(self.name, self.age, self.profession)
    // without having to write the extra code.
    
    func getOlder(byYears incr: Int = 1) {
      self.age += incr
    }
    
    func doWork() {
      print("\(name) is working as a \(profession)")
    }
}

let bob = Person(name: "Bob", age: 45, profession: "Plumber")
bob.doWork() // prints "Bob is working as a Plumber."

let squareRootOfTwo = Math.sqrt(2)

func modifyArrayElements(inout array: [Int], modifier: (Int) -> Int) -> [Int] {
  for (i, val) in array.enumerate() {
    array[i] = modifier(val)
  }
  return array
}
```

And, yeah.
