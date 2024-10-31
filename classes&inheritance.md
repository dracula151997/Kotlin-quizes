Here’s a quiz based on the Kotlin documentation on classes and inheritance.

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

