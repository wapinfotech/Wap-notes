### JavaScript Notes: Comments, Operators, and Conditional Statements

#### 1. **Comments in JavaScript**
   - **Single-line Comment:**  
     Use `//` to comment out a single line of code.
     ```javascript
     // This is a single-line comment
     let x = 10;  // This is also a comment
     ```
   - **Multi-line Comment:**  
     Use `/* ... */` to comment out multiple lines of code.
     ```javascript
     /*
      This is a 
      multi-line comment
     */
     let y = 20;
     ```

#### 2. **Operators in JavaScript**
   Operators are symbols that perform operations on variables and values.

   **Types of Operators:**
   1. **Arithmetic Operators:**
      - Used for mathematical calculations.
      - **Examples:**
        ```javascript
        let a = 10;
        let b = 5;

        console.log(a + b); // Addition: 15
        console.log(a - b); // Subtraction: 5
        console.log(a * b); // Multiplication: 50
        console.log(a / b); // Division: 2
        console.log(a % b); // Modulus: 0 (remainder)
        ```

   2. **Assignment Operators:**
      - Used to assign values to variables.
      - **Examples:**
        ```javascript
        let x = 10;  // Assign 10 to x
        x += 5;      // x = x + 5 (x becomes 15)
        x -= 2;      // x = x - 2 (x becomes 13)
        ```

   3. **Comparison Operators:**
      - Used to compare two values.
      - **Examples:**
        ```javascript
        let a = 10;
        let b = 20;

        console.log(a == b);  // Equal to: false
        console.log(a != b);  // Not equal to: true
        console.log(a > b);   // Greater than: false
        console.log(a < b);   // Less than: true
        ```

   4. **Logical Operators:**
      - Used to combine two or more conditions.
      - **Examples:**
        ```javascript
        let a = 10;
        let b = 20;

        console.log(a > 5 && b > 15);  // Logical AND: true
        console.log(a > 15 || b > 15); // Logical OR: true
        console.log(!(a > 15));        // Logical NOT: true
        ```

   5. **Increment/Decrement Operators:**
      - Used to increase or decrease the value of a variable by 1.
      - **Examples:**
        ```javascript
        let count = 5;
        count++;  // Increment: count becomes 6
        count--;  // Decrement: count becomes 5
        ```

   6. **Ternary Operator:**
      - A shorthand for if-else statements.
      - **Example:**
        ```javascript
        let age = 18;
        let result = (age >= 18) ? "Adult" : "Minor";
        console.log(result); // Output: "Adult"
        ```

#### 3. **Conditional Statements in JavaScript**
   Conditional statements are used to perform different actions based on different conditions.

   1. **`if` Statement:**
      - Executes a block of code if the specified condition is true.
      - **Example:**
        ```javascript
        let age = 18;
        if (age >= 18) {
            console.log("You are eligible to vote.");
        }
        ```
   
   2. **`if-else` Statement:**
      - Executes one block of code if the condition is true, and another if it is false.
      - **Example:**
        ```javascript
        let age = 16;
        if (age >= 18) {
            console.log("You are eligible to vote.");
        } else {
            console.log("You are not eligible to vote.");
        }
        ```

   3. **`if-else if-else` Statement:**
      - Executes multiple blocks of code depending on different conditions.
      - **Example:**
        ```javascript
        let marks = 85;

        if (marks >= 90) {
            console.log("Grade A");
        } else if (marks >= 75) {
            console.log("Grade B");
        } else if (marks >= 50) {
            console.log("Grade C");
        } else {
            console.log("Fail");
        }
        ```
