1. **What is the primary purpose of sealed classes and interfaces in Kotlin?**

   - a) To allow multiple inheritance
   - b) To restrict class hierarchies
   - c) To enable dynamic typing
   - d) To facilitate reflection

2. **Can a sealed class be instantiated directly?**

   - a) Yes
   - b) No

3. **Where must direct subclasses of a sealed class be declared?**

   - a) In any package
   - b) In the same package and module
   - c) In a different module
   - d) In a different package


4. **When using a sealed class with a `when` expression, is an `else` clause required if all possible subclasses are covered?**

   - a) Yes
   - b) No

5. **What is the default visibility of a sealed class's constructor?**

   - a) Public
   - b) Private
   - c) Protected
   - d) Internal

6. **Can an enum class extend a sealed class in Kotlin?**

   - a) Yes
   - b) No

7. **In a multiplatform project, where must direct subclasses of a sealed class reside?**

   - a) In the same source set
   - b) In any source set
   - c) In a different module
   - d) In a different package

8. **What keyword is used to declare a sealed class or interface in Kotlin?**

   - a) `abstract`
   - b) `final`
   - c) `sealed`
   - d) `data`

9. **Can a sealed class have abstract members?**

   - a) Yes
   - b) No

10. **Is it possible to add new subclasses to a sealed class after its compilation?**

    - a) Yes
    - b) No
----
1. **What is the output of the following code?**

   ```kotlin
   sealed class Animal {
       class Dog : Animal()
       class Cat : Animal()
       object Fish : Animal()
   }

   fun printAnimalType(animal: Animal) {
       when (animal) {
           is Animal.Dog -> println("It's a Dog")
           is Animal.Cat -> println("It's a Cat")
           is Animal.Fish -> println("It's a Fish")
       }
   }

   fun main() {
       val dog = Animal.Dog()
       val cat = Animal.Cat()
       val fish = Animal.Fish

       printAnimalType(dog)
       printAnimalType(cat)
       printAnimalType(fish)
   }
   ```
   - a) Compilation error
   - b) It's a Dog  
      It's a Cat  
      It's a Fish
   - c) It's a Dog  
      It's a Cat  
      Runtime error


2. **Which statement correctly defines a sealed class in Kotlin?**

   - a) `sealed data class User(val name: String)`
   - b) `open sealed class User`
   - c) `sealed class User`
   - d) `sealed object User`


3. **What is the result of the following code?**

   ```kotlin
   sealed class Result {
       data class Success(val data: String) : Result()
       data class Error(val message: String) : Result()
   }

   fun handleResult(result: Result): String {
       return when (result) {
           is Result.Success -> "Success with data: ${result.data}"
           is Result.Error -> "Error: ${result.message}"
       }
   }

   fun main() {
       val result = Result.Success("Operation completed")
       println(handleResult(result))
   }
   ```
   - a) Compilation error
   - b) Success with data: Operation completed
   - c) Error: Operation completed
   - d) No output


4. **Given the following code, how can you extend `Vehicle`?**

   ```kotlin
   sealed class Vehicle {
       class Car(val brand: String) : Vehicle()
   }
   ```

   - a) `class Bike : Vehicle()`
   - b) `sealed class Bike : Vehicle()`
   - c) Add `Bike` as a nested class in the same file
   - d) All of the above


5. **What does the following code do?**

   ```kotlin
   sealed class Shape {
       data class Circle(val radius: Double) : Shape()
       data class Rectangle(val height: Double, val width: Double) : Shape()
   }

   fun area(shape: Shape): Double = when (shape) {
       is Shape.Circle -> 3.14 * shape.radius * shape.radius
       is Shape.Rectangle -> shape.height * shape.width
   }

   fun main() {
       val circle = Shape.Circle(3.0)
       val rectangle = Shape.Rectangle(4.0, 5.0)
       println(area(circle))
       println(area(rectangle))
   }
   ```
   - a) Prints the area of a circle and rectangle.
   - b) Compilation error due to the `when` expression.
   - c) Only calculates the area of a circle.
   - d) No output.


6. **Fill in the missing code to declare a sealed class with a subclass:**

   ```kotlin
   _______ class Operation {
       class Add(val x: Int, val y: Int) : Operation()
   }
   ```
   - a) `abstract`
   - b) `sealed`
   - c) `final`
   - d) `open`


7. **What happens if you try to define a subclass of a sealed class in a different file?**

   - a) The subclass will work normally.
   - b) The compiler will throw an error.
   - c) The subclass will be treated as an open class.
   - d) The sealed class becomes abstract.


8. **Given this code, what happens during compilation?**

   ```kotlin
   sealed class Response
   class Success : Response()
   class Failure : Response()
   ```

   - a) Compilation is successful.
   - b) Compilation error due to subclass definitions.
   - c) Requires `Response` subclasses to be nested.
   - d) Success and Failure classes must use `object`.


9. **Which of these is a valid use case for sealed classes?**

   - a) Representing multiple UI states in an app.
   - b) Replacing traditional enums.
   - c) Creating instances of classes at runtime.
   - d) Extending classes across modules.

10. **What is the purpose of the `object` keyword in sealed classes?**

   - a) To create a singleton instance as a subclass of a sealed class.
   - b) To enforce immutability.
   - c) To mark it as a parent sealed class.
   - d) To prevent subclassing.
----

### Challenge 1: Basic Sealed Class Implementation

Create a sealed class called `Weather` with subclasses `Sunny`, `Rainy`, and `Cloudy`. Each subclass should have properties relevant to the weather condition, such as `temperature` (in Celsius) for `Sunny` and `precipitation` (in mm) for `Rainy`. Write a function that takes a `Weather` object and prints a weather report based on its type.

---

### Challenge 2: Sealed Class with `when` Expression

Create a sealed class called `Operation` with subclasses `Addition`, `Subtraction`, and `Multiplication`. Each subclass should take two integer values. Implement a function `performOperation(operation: Operation): Int` that uses a `when` expression to perform the corresponding mathematical operation.

**Example Input/Output:**

```kotlin
val addition = Operation.Addition(4, 5)
println(performOperation(addition)) // Output: 9
```

---

### Challenge 3: Sealed Class for UI State

Create a sealed class called `UiState` with subclasses `Loading`, `Success`, and `Error`. Each subclass should carry appropriate data; for example, `Success` can carry a `String` message, while `Error` can have an error code and a message. Create a function that takes an instance of `UiState` and prints a corresponding message.

**Example Usage:**

```kotlin
val loading = UiState.Loading
val success = UiState.Success("Data loaded successfully.")
val error = UiState.Error(404, "Data not found.")
```

---

### Challenge 4: Serialization Challenge

Create a sealed class hierarchy called `Shape` with subclasses `Circle` (property `radius: Double`), `Rectangle` (properties `width: Double` and `height: Double`), and `Triangle` (properties `base: Double` and `height: Double`). Create a function `serializeShape(shape: Shape): String` that serializes the shape's properties to a JSON-like string (you can use string interpolation).

**Example:**

```kotlin
val circle = Shape.Circle(5.0)
println(serializeShape(circle)) // Output: { "type": "Circle", "radius": 5.0 }
```

---

### Challenge 5: Modeling Commands

Create a sealed class `Command` with subclasses `Start`, `Stop`, and `Pause`. The `Start` class should have a property `startTime`, `Stop` should have a `stopTime`, and `Pause` should have a `duration`. Implement a function that takes a list of `Command` objects and prints a log of commands executed.

---

### Challenge 6: Sealed Class with Generics

Create a sealed class `ApiResponse<T>` with subclasses `Success<T>`, `Loading`, and `Failure`. The `Success` class should contain a `data: T` property, and `Failure` should have an `error: String`. Write a function that handles an `ApiResponse<String>` instance, printing the data if it's successful, or the error message if it fails.

---

### Challenge 7: Representing a File System

Design a sealed class `FileSystemEntity` with subclasses `File` and `Directory`. The `File` subclass should have a `name` and `size`, while `Directory` should contain a list of `FileSystemEntity` objects. Write a function that calculates the total size of all files in a directory, including files in any nested directories.

---

### Challenge 8: Traffic Light Simulation

Create a sealed class `TrafficLight` with subclasses `Red`, `Green`, and `Yellow`. Each subclass should have a `duration` property (representing how many seconds the light stays on). Write a function to simulate a traffic light cycle, printing each light and its duration in sequence.

---

