### Quiz on Kotlin Exceptions

1. **True or False**: In Kotlin, all exceptions are unchecked by default.
   - A) True
   - B) False

2. **What keyword is used to manually throw an exception in Kotlin?**
   - A) catch
   - B) throw
   - C) try
   - D) finally

3. **Which function would you use to check if an input argument meets a specific condition before proceeding?**
   - A) require()
   - B) check()
   - C) error()
   - D) validate()

4. **What exception does `require()` throw if the condition is not met?**
   - A) IllegalStateException
   - B) NullPointerException
   - C) IllegalArgumentException
   - D) IndexOutOfBoundsException

5. **What is the purpose of the `finally` block in Kotlin exception handling?**
   - A) To catch additional exceptions
   - B) To throw a new exception
   - C) To execute code regardless of exception occurrence
   - D) To log the exception

6. **In a `try-catch` block, how should multiple catch blocks be ordered?**
   - A) From least specific to most specific
   - B) From most specific to least specific
   - C) Randomly
   - D) Only one `catch` block is allowed

7. **Which function would be best to use if you need to validate an object’s state within Kotlin?**
   - A) require()
   - B) check()
   - C) validate()
   - D) error()

8. **What exception type is thrown by `check()` if the condition is false?**
   - A) IllegalStateException
   - B) IllegalArgumentException
   - C) NullPointerException
   - D) AssertionError

9. **Which function would you use in Kotlin to signal a state that logically should not occur?**
   - A) require()
   - B) check()
   - C) error()
   - D) throw

10. **What is the base class of all exception classes in Kotlin?**
    - A) Throwable
    - B) RuntimeException
    - C) Exception
    - D) Error
-----
Here’s a Kotlin code-focused quiz on exceptions, aimed at assessing practical understanding and application of Kotlin’s exception handling features:

### Code Quiz on Kotlin Exceptions

1. **What will be the output of the following code?**
   ```kotlin
   fun main() {
       val result = try {
           val num = "abc".toInt()
           "Success"
       } catch (e: NumberFormatException) {
           "Failed with NumberFormatException"
       } finally {
           println("This will always print")
       }
       println(result)
   }
   ```
   - A) This will always print, Success
   - B) This will always print, Failed with NumberFormatException
   - C) Success
   - D) Failed with NumberFormatException

2. **What exception type is thrown by the `require()` function in the following code?**
   ```kotlin
   fun main() {
       val age = -5
       require(age > 0) { "Age must be positive" }
   }
   ```
   - A) IllegalStateException
   - B) IllegalArgumentException
   - C) RuntimeException
   - D) NullPointerException

3. **Fill in the blank:** Complete the code to handle `NullPointerException`.
   ```kotlin
   fun main() {
       val name: String? = null
       try {
           println(name!!.length)
       } catch (e: ____) {
           println("Caught a NullPointerException")
       }
   }
   ```
   - A) Exception
   - B) NullPointerException
   - C) IllegalArgumentException
   - D) Throwable

4. **What will be printed by the following code?**
   ```kotlin
   fun main() {
       try {
           check(false) { "Check failed!" }
       } catch (e: IllegalStateException) {
           println(e.message)
       }
   }
   ```
   - A) No output
   - B) Check failed!
   - C) IllegalArgumentException
   - D) IllegalStateException

5. **Which line should you add to complete the code below to throw an `IllegalStateException` when a condition isn’t met?**
   ```kotlin
   fun validateStatus(status: String) {
       if (status != "ACTIVE") {
           // Add code here
       }
   }
   ```
   - A) throw Exception("Invalid status")
   - B) check(status == "ACTIVE") { "Invalid status" }
   - C) require(status == "ACTIVE") { "Invalid status" }
   - D) throw IllegalStateException("Invalid status")

6. **Given this function, what exception will be thrown when `division(5, 0)` is called?**
   ```kotlin
   fun division(a: Int, b: Int): Int {
       require(b != 0) { "b cannot be zero" }
       return a / b
   }
   ```
   - A) ArithmeticException
   - B) IllegalStateException
   - C) IllegalArgumentException
   - D) NullPointerException

7. **What will be printed when the following code is executed?**
   ```kotlin
   fun main() {
       try {
           val result = divide(10, 0)
           println("Result: $result")
       } catch (e: Exception) {
           println("Caught an exception: ${e.message}")
       }
   }

   fun divide(a: Int, b: Int): Int {
       return a / b
   }
   ```
   - A) Result: 0
   - B) Caught an exception: b cannot be zero
   - C) Caught an exception: / by zero
   - D) Result: Exception

8. **Identify the missing code to catch multiple types of exceptions:**
   ```kotlin
   fun main() {
       try {
           val list = listOf(1, 2, 3)
           println(list[5])
       } catch (e: IndexOutOfBoundsException) {
           println("Index out of bounds!")
       } catch (e: ____ ) {
           println("Caught an exception")
       }
   }
   ```
   - A) Throwable
   - B) Exception
   - C) RuntimeException
   - D) ArrayIndexOutOfBoundsException

9. **Which function call would you use to signify an error that should never occur logically?**
   ```kotlin
   fun unexpectedCase() {
       // Fill in the blank
       ____("Unexpected case encountered")
   }
   ```
   - A) throw IllegalStateException
   - B) require
   - C) check
   - D) error

10. **What will happen when this code is run?**
    ```kotlin
    fun main() {
        try {
            val data = listOf(1, 2, 3)
            data[10]
        } finally {
            println("Cleanup done")
        }
    }
    ```
    - A) Cleanup done, then ArrayIndexOutOfBoundsException
    - B) ArrayIndexOutOfBoundsException, then Cleanup done
    - C) Cleanup done only
    - D) No output
