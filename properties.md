### Kotlin Properties Quiz

1. **True or False**: Properties in Kotlin can only be mutable.

2. Which keyword is used to declare a read-only property?
   - a) `var`
   - b) `val`
   - c) `const`
   - d) `let`

3. What is the default parameter name used in a custom setter in Kotlin?
   - a) `newValue`
   - b) `data`
   - c) `field`
   - d) `value`

4. How can you access the backing field of a property in a custom accessor?
   - a) Using the property name
   - b) Using `this`
   - c) Using `field`
   - d) Using `backingField`

5. **Which keyword must be used with the `lateinit` modifier in Kotlin?**
   - a) `val`
   - b) `const`
   - c) `var`
   - d) `let`
     
6. When is a compile-time constant (`const`) property allowed?
   - a) As a top-level or companion object property
   - b) With a custom getter
   - c) As a mutable property
   - d) Inside a function

7. **True or False**: Accessing a `lateinit` property before initialization will throw an exception.

8. What method checks if a `lateinit` property has been initialized?
   - a) `::isSet`
   - b) `.isInitialized`
   - c) `.isLateinit`
   - d) `::isReady`

9. **Multiple Choice**: Delegated properties are commonly used for:
   - a) Lazy initialization
   - b) Storing immutable data only
   - c) Checking null values
   - d) None of the above

10. **True or False**: A property in Kotlin can have a custom getter without a backing field.
---------

### Kotlin Properties Code Quiz

1. **What will the following code output?**
   ```kotlin
   class Person {
       val name: String = "Alice"
       var age: Int = 25
           get() = field + 1
   }

   fun main() {
       val person = Person()
       println(person.age)
   }
   ```
   - a) 24
   - b) 25
   - c) 26
   - d) Compilation error

2. **What does the following code do when accessing `name`?**
   ```kotlin
   class User {
       lateinit var name: String
   }

   fun main() {
       val user = User()
       println(user.name)
   }
   ```
   - a) Prints `null`
   - b) Throws an `UninitializedPropertyAccessException`
   - c) Prints an empty string
   - d) Compiles without an error

3. **Given this code, what will `greeting` return?**
   ```kotlin
   class Greeting {
       val greeting: String
           get() = "Hello, Kotlin!"
   }

   fun main() {
       val greet = Greeting()
       println(greet.greeting)
   }
   ```
   - a) "Hello"
   - b) Compilation error
   - c) "Hello, Kotlin!"
   - d) "Kotlin"

4. **What will the following code print?**
   ```kotlin
   class Example {
       var counter = 0
           set(value) {
               if (value >= 0) field = value
           }
   }

   fun main() {
       val example = Example()
       example.counter = -10
       println(example.counter)
   }
   ```
   - a) -10
   - b) 0
   - c) Compilation error
   - d) None of the above

5. **What will this code output?**
   ```kotlin
   class Student {
       val grade: String = "A"
       init {
           println("Grade is $grade")
       }
   }

   fun main() {
       val student = Student()
   }
   ```
   - a) "Grade is A"
   - b) "Grade is"
   - c) "Compilation error"
   - d) Nothing

6. **What is the output of this code?**
   ```kotlin
   class Sample {
       var text: String = "Kotlin"
           private set
   }

   fun main() {
       val sample = Sample()
       sample.text = "Java"
       println(sample.text)
   }
   ```
   - a) "Java"
   - b) "Kotlin"
   - c) Compilation error
   - d) Null

7. **What will the following code print?**
   ```kotlin
   class Counter {
       var count: Int by lazy {
           println("Initializing count")
           10
       }
   }

   fun main() {
       val counter = Counter()
       println(counter.count)
       println(counter.count)
   }
   ```
   - a) "Initializing count\n10\n10"
   - b) "10\n10"
   - c) "Initializing count\nInitializing count\n10\n10"
   - d) Compilation error
