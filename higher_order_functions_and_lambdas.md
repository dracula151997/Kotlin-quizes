### 10 Multiple Choice Questions (MCQ)

1. What is a lambda expression in Kotlin?
   - A) A named function
   - B) A function literal with no name
   - C) A variable type
   - D) A control structure
   
2. Which of the following is the correct syntax for a lambda expression in Kotlin that adds two integers?
   - A) `{a, b -> a + b}`
   - B) `(a + b) -> a, b`
   - C) `fun(a, b) { a + b }`
   - D) `{(a, b) => a + b}`
   
3. What is the type of `val multiply: (Int, Int) -> Int = { a, b -> a * b }`?
   - A) `Int`
   - B) `String`
   - C) A function type `(Int, Int) -> Int`
   - D) A list of Integers
   
4. How can a lambda expression access variables declared outside its scope?
   - A) By explicitly declaring them as global
   - B) By declaring them as constants
   - C) By capturing them (closures)
   - D) By using them as arguments
   
5. What is the output of the following code?
   ```kotlin
   val printHello = { println("Hello!") }
   printHello()
   ```
   - A) No output
   - B) Error
   - C) "Hello!"
   - D) "println(\"Hello!\")"
   
6. Which higher-order function can you use to transform elements of a collection using a lambda?
   - A) `map`
   - B) `reduce`
   - C) `filter`
   - D) `forEach`
   
7. How do you specify the type of parameters in a lambda expression?
   - A) `val lambda = { a: Int, b: Int -> a + b }`
   - B) `val lambda = { (a: Int, b: Int) -> a + b }`
   - C) `val lambda: (a, b) -> Int = { a + b }`
   - D) `val lambda: Int -> (Int, Int) = { a + b }`
   
8. Which function applies a given lambda to each element of a collection but does not produce a new list?
   - A) `map`
   - B) `forEach`
   - C) `filter`
   - D) `sortedBy`
   
9. Given the following code, what is the result?
   ```kotlin
   val numbers = listOf(1, 2, 3, 4)
   val result = numbers.filter { it % 2 == 0 }
   println(result)
   ```
   - A) `[1, 2, 3, 4]`
   - B) `[2, 4]`
   - C) `[1, 3]`
   - D) Error
   
10. What is a higher-order function in Kotlin?
    - A) A function that calls itself
    - B) A function that can only return a string
    - C) A function that takes another function as a parameter or returns one
    - D) A function that is declared using `fun`
    
---

### 10 Code Quiz Questions

1. Write a lambda that takes two integers and returns their sum.
   ```kotlin
   // Your code here
   ```

2. Convert the following function to a lambda expression:
   ```kotlin
   fun greet() { println("Hello, World!") }
   // Your lambda here
   ```

3. What will the following code output?
   ```kotlin
   val nums = listOf(1, 2, 3)
   val result = nums.map { it * it }
   println(result)
   ```
   - A) `[1, 2, 3]`
   - B) `[1, 4, 9]`
   - C) `1, 4, 9`
   - D) Error

4. Create a lambda that filters a list of strings to only include strings with more than three characters.
   ```kotlin
   // Your code here
   ```

5. What will happen when executing the following code?
   ```kotlin
   val greet = { name: String -> "Hello, $name!" }
   println(greet("Kotlin"))
   ```
   - A) Prints "Hello, Kotlin!"
   - B) Error
   - C) Prints "Kotlin"
   - D) No output

6. Create a lambda that takes a list of integers and returns the sum of all even numbers.
   ```kotlin
   // Your code here
   ```

7. Transform this anonymous function into a lambda:
   ```kotlin
   val multiply = fun(a: Int, b: Int): Int {
       return a * b
   }
   // Your lambda here
   ```

8. What does this code output?
   ```kotlin
   val words = listOf("one", "two", "three")
   val lengths = words.map { it.length }
   println(lengths)
   ```
   - A) `[1, 2, 3]`
   - B) `[3, 3, 5]`
   - C) `[one, two, three]`
   - D) Error

9. Write a lambda that returns true if the input integer is a prime number.
   ```kotlin
   // Your code here
   ```

10. Use a lambda expression to reverse each string in a list.
    ```kotlin
    // Your code here
    ```

---

### Code Challenges

1. **Challenge**: Implement a lambda to find the maximum element in a list of integers.
   
   **Hint:** Consider using a `reduce` function.

2. **Challenge**: Create a lambda that takes a list of integers and returns a list of their squares, sorted in descending order.
   
   **Hint:** Use `map` followed by `sortedDescending`.

3. **Challenge**: Write a lambda that removes all null values from a list.
   
   **Hint:** Use the `filterNotNull` function.

4. **Challenge**: Use a lambda to combine elements from two lists element-wise into pairs.
   
   **Hint:** You can use `zip`.

5. **Challenge**: Create a lambda function that checks if a given string is a palindrome.
   
   **Hint:** Compare the string to its reverse using `reversed()`.

6. **Challenge**: Implement a lambda to convert a list of integers to their binary string representations.
   
   **Hint:** Use `toString(2)` for binary conversion.

7. **Challenge**: Write a lambda that takes a number and returns a list of its factors.
   
   **Hint:** Iterate up to the square root of the number.

8. **Challenge**: Create a lambda function that finds the longest word in a list of strings.
    
   **Hint:** Use `maxByOrNull` with the string length property.
