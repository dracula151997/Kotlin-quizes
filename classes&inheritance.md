### Quiz on Kotlin Classes and Inheritance

1. **True or False**: In Kotlin, classes are final by default and cannot be inherited unless explicitly marked.
   - A) True
   - B) False

2. **What is the base class for all classes in Kotlin?**
   - A) Object
   - B) Any
   - C) Super
   - D) Base

3. **How do you make a class inheritable in Kotlin?**
   - A) Use the `open` keyword
   - B) Use the `inherit` keyword
   - C) Use the `extend` keyword
   - D) Classes are inheritable by default

4. **What will happen if you try to override a non-`open` function in a subclass?**
   - A) The function will override normally.
   - B) The compiler will throw an error.
   - C) The function will override but remain final.
   - D) The function will remain the same as in the superclass.

5. **Which modifier should be used to prevent further overriding of a function in subclasses?**
   - A) sealed
   - B) open
   - C) final
   - D) abstract

6. **Given the following code, what will be the output?**
   ```kotlin
   open class Animal {
       open fun sound() = "Some sound"
   }
   class Dog : Animal() {
       override fun sound() = "Bark"
   }
   fun main() {
       val animal: Animal = Dog()
       println(animal.sound())
   }
   ```
   - A) Some sound
   - B) Bark
   - C) Compilation error
   - D) Runtime error

7. **If a class has no `open` keyword, can its properties be overridden in subclasses?**
   - A) Yes, all properties can be overridden.
   - B) No, only properties marked with `open` can be overridden.
   - C) Yes, but only val properties.
   - D) No, properties can only be overridden if they are `abstract`.

8. **Which of the following options correctly overrides a property in a derived class?**
   ```kotlin
   open class Shape {
       open val sides: Int = 4
   }
   ```
   - A) `class Circle : Shape { override val sides: Int = 0 }`
   - B) `class Circle : Shape { override val sides: Double = 0.0 }`
   - C) `class Circle : Shape { var sides: Int = 0 }`
   - D) None of the above

9. **What will happen if you try to override a `val` property with a `var` property in a subclass?**
   - A) Compilation error
   - B) It is allowed, as `var` can replace `val`.
   - C) The `var` property will act as `val`.
   - D) The `val` property will remain final.

10. **Identify the correct way to call a superclass function in a subclass in Kotlin:**
    ```kotlin
    open class Vehicle {
        open fun start() = "Starting vehicle"
    }
    class Car : Vehicle() {
        override fun start(): String {
            // Add code here to call the superclass function
        }
    }
    ```
    - A) `return super.start()`
    - B) `return Vehicle.start()`
    - C) `return this@Vehicle.start()`
    - D) `return base.start()`
------
Here’s a code-focused quiz to test your understanding of Kotlin classes and inheritance concepts:

---

### Code Quiz on Kotlin Classes and Inheritance

1. **What will the following code output?**
   ```kotlin
   open class Person {
       open val profession = "Unknown"
       open fun introduce() = "I am a $profession."
   }
   
   class Teacher : Person() {
       override val profession = "Teacher"
   }
   
   fun main() {
       val person: Person = Teacher()
       println(person.introduce())
   }
   ```
   - A) I am a Teacher.
   - B) I am a Unknown.
   - C) Compilation error.
   - D) Runtime error.

2. **Fill in the blank to allow class `ElectricCar` to inherit from `Vehicle`:**
   ```kotlin
   open class Vehicle(val speed: Int)
   
   ____ class ElectricCar(speed: Int, val battery: Int) : Vehicle(speed)
   ```
   - A) extend
   - B) inherit
   - C) class
   - D) open

3. **What will be the result of executing this code?**
   ```kotlin
   open class Shape(val name: String) {
       open fun draw() = println("Drawing $name")
   }

   class Circle : Shape("Circle") {
       override fun draw() = println("Drawing a perfect $name")
   }

   fun main() {
       val shape: Shape = Circle()
       shape.draw()
   }
   ```
   - A) Drawing Circle
   - B) Drawing a perfect Circle
   - C) Compilation error
   - D) Runtime error

4. **In the following code, which keyword should replace `____` to make `sound` not overrideable in subclasses?**
   ```kotlin
   open class Animal {
       ____ fun sound() = "Some sound"
   }
   ```
   - A) open
   - B) final
   - C) override
   - D) abstract

5. **What will the following code print?**
   ```kotlin
   open class Book {
       open val genre = "Unknown"
   }

   class Fiction : Book() {
       override val genre = "Fiction"
   }

   class Mystery : Fiction() {
       override val genre = "Mystery"
   }

   fun main() {
       val book: Book = Mystery()
       println(book.genre)
   }
   ```
   - A) Fiction
   - B) Mystery
   - C) Unknown
   - D) Compilation error

6. **What is the output of the following code?**
   ```kotlin
   open class Appliance {
       open fun operate() = "Operating appliance"
   }

   class WashingMachine : Appliance() {
       override fun operate() = "Washing clothes"
   }

   fun main() {
       val appliance: Appliance = WashingMachine()
       println(appliance.operate())
   }
   ```
   - A) Operating appliance
   - B) Washing clothes
   - C) Compilation error
   - D) Runtime error

7. **How should you define `Teacher` to ensure `teach()` is only accessible within the `Teacher` class?**
   ```kotlin
   open class Employee {
       open fun work() = "Working"
   }

   class Teacher : Employee() {
       ____ fun teach() = "Teaching"
   }
   ```
   - A) open
   - B) private
   - C) protected
   - D) public

8. **What will the code output if `Person` has a non-`open` property?**
   ```kotlin
   open class Person(val name: String) {
       val age: Int = 25
   }

   class Student(name: String) : Person(name) {
       val age: Int = 18
   }

   fun main() {
       val person: Person = Student("Alice")
       println(person.age)
   }
   ```
   - A) 18
   - B) 25
   - C) Compilation error
   - D) Runtime error

9. **Fill in the blank to make `Manager` an abstract class:**
   ```kotlin
   ____ class Manager {
       abstract fun manage()
   }
   ```
   - A) open
   - B) final
   - C) sealed
   - D) abstract

10. **What will the following code output?**
    ```kotlin
    open class Device {
        open fun powerOn() = "Powering on device"
    }

    class Smartphone : Device() {
        override fun powerOn() = "Powering on smartphone"
    }

    fun main() {
        val device = Smartphone()
        println(device.powerOn())
    }
    ```
    - A) Powering on device
    - B) Powering on smartphone
    - C) Compilation error
    - D) Runtime error

