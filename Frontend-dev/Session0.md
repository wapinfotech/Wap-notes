JavaScript loops and string concatenation:

### 1. **`for` Loop**
   - The `for` loop is used when the number of iterations is known beforehand.
   - **Syntax:**
     ```javascript
     for (initialization; condition; increment/decrement) {
         // code to be executed
     }
     ```
   - **Example:**
     ```javascript
     for (let i = 0; i < 5; i++) {
         console.log("Iteration: " + i);
     }
     ```
   - **Explanation:**  
     The loop starts with initialization, checks the condition, and executes the block if the condition is true. Then it performs the increment/decrement operation and repeats the process.

### 2. **`for/in` Loop**
   - The `for/in` loop is used to iterate over the properties (keys) of an object.
   - **Syntax:**
     ```javascript
     for (key in object) {
         // code to be executed
     }
     ```
   - **Example:**
     ```javascript
     const person = {name: "Alice", age: 25, city: "New York"};
     for (let key in person) {
         console.log(key + ": " + person[key]);
     }
     ```
   - **Explanation:**  
     This loop iterates over each property in the `person` object and prints the key-value pairs.

### 3. **`for/of` Loop**
   - The `for/of` loop is used to iterate over iterable objects like arrays, strings, or other collection types.
   - **Syntax:**
     ```javascript
     for (variable of iterable) {
         // code to be executed
     }
     ```
   - **Example:**
     ```javascript
     const fruits = ["apple", "banana", "cherry"];
     for (let fruit of fruits) {
         console.log(fruit);
     }
     ```
   - **Explanation:**  
     This loop iterates over each element in the `fruits` array and prints the element.

### 4. **`while` Loop**
   - The `while` loop is used when the number of iterations is not known, and the loop continues as long as the condition is true.
   - **Syntax:**
     ```javascript
     while (condition) {
         // code to be executed
     }
     ```
   - **Example:**
     ```javascript
     let i = 0;
     while (i < 5) {
         console.log("Iteration: " + i);
         i++;
     }
     ```
   - **Explanation:**  
     The loop checks the condition before executing the block. If the condition is true, the code is executed, and the process is repeated until the condition becomes false.

### 5. **`do/while` Loop**
   - The `do/while` loop is similar to the `while` loop, but it guarantees that the code block is executed at least once.
   - **Syntax:**
     ```javascript
     do {
         // code to be executed
     } while (condition);
     ```
   - **Example:**
     ```javascript
     let i = 0;
     do {
         console.log("Iteration: " + i);
         i++;
     } while (i < 5);
     ```
   - **Explanation:**  
     The code block is executed first, and then the condition is checked. If the condition is true, the loop continues.

### 6. **String and Variable Concatenation**
   - **Using `console.log`:**
     - You can concatenate strings and variables using the `+` operator.
     - **Example:**
       ```javascript
       let name = "Alice";
       console.log("Hello, " + name + "!");
       ```
   - **Using Template Literals (Backticks):**
     - Template literals allow embedding variables and expressions within strings using `${}` inside backticks (`` ` ``).
     - **Example:**
       ```javascript
       let name = "Alice";
       console.log(`Hello, ${name}!`);
       ```
   - **Explanation:**  
     Template literals provide a more readable way to concatenate strings and variables, especially when dealing with multiple variables or expressions.

---
