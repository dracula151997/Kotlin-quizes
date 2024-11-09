# Kotlin Functions Quizzes

## Quiz: Kotlin Functions and Default Arguments

### Multiple Choice Quiz

1. **What is a default argument in Kotlin?**
   - A) An argument with a fixed, unchangeable value
   - B) An argument with a specified default value that is used when no value is passed for that parameter
   - C) An argument that throws an error if a value is not provided
   - D) None of the above

2. **When a function has a default argument in Kotlin, what happens if you call the function without passing that argument?**
   - A) The compiler throws an error
   - B) The function call fails silently
   - C) The default value is used for the parameter
   - D) The function does not execute

3. **Which of the following correctly defines a Kotlin function with a default argument?**
   ```kotlin
   fun greet(name: String = "Guest") {
       println("Hello, $name!")
   }
   ```
   - A) Incorrect, functions cannot have default values in Kotlin
   - B) Correct, this defines a function `greet` with a default argument
   - C) Incorrect, `String` is not allowed as a default argument type
   - D) Incorrect, Kotlin requires all parameters to be explicitly passed

4. **Consider the function:**
   ```kotlin
   fun addNumbers(a: Int, b: Int = 5): Int {
       return a + b
   }
   ```
   What will be the result of calling `addNumbers(10)`?
   - A) 10
   - B) 5
   - C) 15
   - D) Compilation error

5. **True or False:** Default arguments can only be used with functions that have more than one parameter.

6. **How can you override the default argument value when calling a function?**
   - A) It is not possible to override default arguments
   - B) By passing a new value for the argument in the function call
   - C) By reassigning the parameter inside the function
   - D) By using a special `override` keyword

7. **Consider the function:**
   ```kotlin
   fun printMessage(message: String = "Welcome") {
       println(message)
   }
   ```
   What is the output of calling `printMessage("Hello, Kotlin!")`?
   - A) Welcome
   - B) Hello, Kotlin!
   - C) Compilation error
   - D) Nothing is printed

8. **Can default arguments be used in functions with both positional and named arguments?**
   - A) Yes
   - B) No


### Code-Based Questions

1. **What will be the output of the following code?**
   ```kotlin
   fun sayHello(name: String = "Kotlin") {
       println("Hello, $name!")
   }
   sayHello()
   ```
   - A) Hello, Kotlin!
   - B) Hello!
   - C) Compilation error
   - D) No output

2. **What is the result of calling `calculateArea(5)` in the code below?**
   ```kotlin
   fun calculateArea(length: Int, width: Int = 10): Int {
       return length * width
   }
   ```
   - A) 10
   - B) 50
   - C) Compilation error
   - D) None of the above

3. **Given the function:**
   ```kotlin
   fun greet(firstName: String, lastName: String = "Doe") {
       println("Hello, $firstName $lastName")
   }
   ```
   What will be printed when calling `greet("John")`?
   - A) Hello, John
   - B) Hello, John Doe
   - C) Hello, Doe
   - D) Compilation error

4. **Fill in the blanks to define a function that multiplies two numbers, with a default value for one of the numbers:**
   ```kotlin
   fun multiply(a: Int, b: Int = __): Int {
       return a * b
   }
   ```
   - A) `1`
   - B) `2`
   - C) `0`
   - D) `10`

5. **What will be the output of this code?**
   ```kotlin
   fun printMessage(message: String = "Hi", times: Int = 3) {
       repeat(times) {
           println(message)
       }
   }
   printMessage("Hello", 2)
   ```
   - A) Hi (repeated 3 times)
   - B) Hello (repeated 2 times)
   - C) Compilation error
   - D) No output

6. **Consider this function definition:**
   ```kotlin
   fun addNumbers(a: Int = 5, b: Int = 10): Int {
       return a + b
   }
   ```
   What will `addNumbers(b = 15)` return?
   - A) 5
   - B) 10
   - C) 20
   - D) 25

7. **True or False:** The following function call is valid in Kotlin:
   ```kotlin
   fun displayInfo(name: String = "Anonymous", age: Int = 18) {
       println("$name is $age years old")
   }
   displayInfo(age = 25)
   ```

8. **What will be the output of this code?**
   ```kotlin
   fun divide(a: Int, b: Int = 2): Int {
       return a / b
   }
   println(divide(8))
   ```
   - A) 4
   - B) 2
   - C) 8
   - D) Compilation error

9. **Given the function:**
   ```kotlin
   fun greetUser(greeting: String = "Welcome", name: String = "Guest") {
       println("$greeting, $name!")
   }
   ```
   What will be the result of `greetUser(name = "Alice")`?
   - A) Welcome, Alice!
   - B) Hello, Alice!
   - C) Greeting, Guest!
   - D) Compilation error

---

## Code Challenge: Kotlin Default Arguments

### Code Challenge 1: Calculate Price after tax and discount

**Create a function called `calculatePrice` that calculates the final price of a product based on the following parameters:**

- `basePrice`: The initial price of the product (mandatory).
- `discount`: The percentage discount applied to the product. Default value is 0% (no discount).
- `tax`: The percentage tax applied to the product. Default value is 5%.

**The function should:**
1. Calculate the discounted price by applying the `discount` to the `basePrice`.
2. Calculate the tax on the discounted price.
3. Return the final price after applying the discount and adding the tax.

### Example:

```kotlin
fun main() {
    println(calculatePrice(100.0)) // Output: 105.0
    println(calculatePrice(100.0, discount = 10.0)) // Output: 94.5
    println(calculatePrice(100.0, discount = 10.0, tax = 8.0)) // Output: 97.2
}
```
Here are additional code challenges focusing on Kotlin functions and different scenarios to test your skills:

---

### Code Challenge 2: String Formatter Function

**Description:**
Create a function `formatString` that takes a string `input` and two optional parameters:
- `prefix`: A string to be added at the start of `input`. Default value is an empty string.
- `suffix`: A string to be added at the end of `input`. Default value is an empty string.

The function should concatenate `prefix`, `input`, and `suffix` together and return the resulting string.

#### Example:

```kotlin
fun main() {
    println(formatString("Kotlin")) // Output: Kotlin
    println(formatString("Kotlin", prefix = "Hello, ")) // Output: Hello, Kotlin
    println(formatString("Kotlin", prefix = "Welcome to ", suffix = " World!")) // Output: Welcome to Kotlin World!
}
```

---

### Code Challenge 3: Sum of Variable Arguments

**Description:**
Create a function `sumNumbers` that takes a variable number of `Int` arguments and returns their sum. If no numbers are passed, return 0.

#### Example:

```kotlin
fun main() {
    println(sumNumbers()) // Output: 0
    println(sumNumbers(1, 2, 3, 4)) // Output: 10
    println(sumNumbers(10, -5, 5)) // Output: 10
}
```

---

### Code Challenge 4: Custom Greeting Function

**Description:**
Create a function `customGreet` that accepts the following parameters:
- `name`: String (mandatory)
- `greeting`: String with a default value of "Hello"
- `punctuation`: String with a default value of "!"

The function should print the greeting message in the format: "`<greeting>, <name><punctuation>`".

#### Example:

```kotlin
fun main() {
    customGreet("Alice") // Output: Hello, Alice!
    customGreet("Bob", greeting = "Hi") // Output: Hi, Bob!
    customGreet("Charlie", punctuation = ".") // Output: Hello, Charlie.
}
```
---
### Code Challenge 5: Temperature Conversion

**Description:**
Create a function `convertTemperature` that takes two parameters:
- `temperature`: Double (mandatory)
- `unit`: String with a default value of "C" (for Celsius). It can also accept "F" for Fahrenheit.

The function should convert the temperature to the other unit and return the converted value. If `unit` is "C", convert to Fahrenheit. If `unit` is "F", convert to Celsius.

Use the formulas:
- Celsius to Fahrenheit: `(temperature * 9/5) + 32`
- Fahrenheit to Celsius: `(temperature - 32) * 5/9`

#### Example:

```kotlin
fun main() {
    println(convertTemperature(0.0)) // Output: 32.0 (0°C to Fahrenheit)
    println(convertTemperature(32.0, "F")) // Output: 0.0 (32°F to Celsius)
    println(convertTemperature(100.0, "C")) // Output: 212.0
}
```

