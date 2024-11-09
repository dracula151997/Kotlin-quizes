Got it! Here is the refactored content with the hints section preserved as-is:

---

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

---

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

## Code Challenges

### Code Challenge 1: Calculate Price with Default Arguments

**Description:**
Create a function called `calculatePrice` that calculates the final price of a product based on:
- `basePrice`: Initial price (mandatory).
- `discount`: Percentage discount. Default is 0%.
- `tax`: Percentage tax. Default is 5%.

The function should:
1. Apply the discount.
2. Calculate and apply tax.
3. Return the final price.

#### Example:
```kotlin
fun main() {
    println(calculatePrice(100.0)) // Output: 105.0
    println(calculatePrice(100.0, discount = 10.0)) // Output: 94.5
    println(calculatePrice(100.0, discount = 10.0, tax = 8.0)) // Output: 97.2
}
```

---

### Code Challenge 2: String Formatter Function

**Description:**
Create a function `formatString` that takes:
- `input`: String (mandatory).
- `prefix`: String added to the start (default is empty).
- `suffix`: String added to the end (default is empty).

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
Create a function `sumNumbers` that accepts a variable number of `Int` arguments and returns their sum. If none, return 0.

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
Create a function `customGreet` with:
- `name`: String (mandatory).
- `greeting`: Default "Hello".
- `punctuation`: Default "!"

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
Create `convertTemperature` with:
- `temperature`: Double (mandatory).
- `unit`: Default "C" (Celsius), can accept "F" (Fahrenheit).

#### Conversion Formulas:
- Celsius to Fahrenheit: `(temperature * 9/5) + 32`
- Fahrenheit to Celsius: `(temperature - 32) * 5/9`

#### Example:
```kotlin
fun main() {
    println(convertTemperature(0.0)) // Output: 32.0
    println(convertTemperature(32.0, "F")) // Output: 0.0
    println(convertTemperature(100.0, "C")) // Output: 212.0
}
```

---

## Code Challenge Hints

### Code Challenge 1: Calculate Price with Default Arguments

**Hints:**

1. **Function Declaration Basics:**
   - Start by creating a function `calculatePrice` with three parameters: `basePrice` (mandatory), `discount` (optional with a default value of 0%), and `tax` (optional with a default value of 5%).

2. **Applying the Discount:**
   - Calculate the discounted price using this formula:
     ```kotlin
     val discountedPrice = basePrice - (basePrice * discount / 100)
     ```
   - This means you reduce the `basePrice` by the given `discount` percentage.

3. **Calculating Tax:**
   - Calculate the tax amount on the `discountedPrice` using:
     ```kotlin
     val taxAmount = discountedPrice * tax / 100
     ```
   - Add this `taxAmount` to the `discountedPrice` to get the final price.

4. **Returning the Final Price:**
   - Calculate the `finalPrice` by adding the `taxAmount` to the `discountedPrice`:
     ```kotlin
     val finalPrice = discountedPrice + taxAmount
     ```
   - Return `finalPrice` from the function.

5. **Testing Your Function:**
   - Test the function by calling it with just the `basePrice`.
   - Test with different values for `discount` and `tax` to ensure your calculations are working as expected.

---

### Code Challenge 2: String Formatter Function

**Hints**
- Start by creating a function that takes three parameters: `input`, `prefix`, and `suffix`.
- Use string concatenation (`+`) to add `prefix` before `input` and `suffix` after `input`.
- If `prefix` or `suffix` is not provided, use the default empty string value.

---

### Code Challenge 3: Sum of Variable Arguments

**Hints:**
- Use the `vararg` keyword in your function parameter list to accept a variable number of integers.
- Use a `for` loop or `array.sum()` to add all numbers together.
- If no numbers are passed, the sum should be zero by default.

---

### Code Challenge 4: Custom Greeting Function

**Hints:**
- Use string templates with the format `"Hello, $name!"` to easily create strings.
- Understand that you can pass different greetings or punctuation symbols, and if they are not provided, the default ones will be used.

---

### Code Challenge 5: Temperature Conversion

**Hints:**
- Use an `if-else` statement to check the `unit` parameter.
- For converting Celsius to Fahrenheit, use `(temperature * 9/5) + 32`.
- For converting Fahrenheit to Celsius, use `(temperature - 32) * 5/9`.
- Be sure to test with different inputs to see if your function works correctly.
