### JavaScript Functions

#### 1. **Introduction to Functions**
   - **Definition**: Functions are reusable blocks of code designed to perform a specific task. They help in reducing code repetition.
   - **Syntax**:
     ```javascript
     function functionName(parameters) {
       // Code to be executed
     }
     ```
   - **Example**:
     ```javascript
     function greet(name) {
       console.log("Hello, " + name + "!");
     }
     greet("Alice");
     ```

#### 2. **Function Expressions**
   - **Definition**: Functions can also be defined as expressions and assigned to variables.
   - **Syntax**:
     ```javascript
     const functionName = function(parameters) {
       // Code to be executed
     };
     ```
   - **Example**:
     ```javascript
     const greet = function(name) {
       console.log("Hello, " + name + "!");
     };
     greet("Bob");
     ```

#### 3. **Arrow Functions**
   - **Definition**: A shorter syntax for writing function expressions, introduced in ES6.
   - **Syntax**:
     ```javascript
     const functionName = (parameters) => {
       // Code to be executed
     };
     ```
   - **Example**:
     ```javascript
     const greet = (name) => {
       console.log("Hello, " + name + "!");
     };
     greet("Charlie");
     ```

#### 4. **Function Parameters and Arguments**
   - **Parameters**: Variables listed as part of the function definition.
   - **Arguments**: Values passed to the function when it is invoked.
   - **Default Parameters**: Functions can have default parameter values if no arguments are provided.
     ```javascript
     function greet(name = "Stranger") {
       console.log("Hello, " + name + "!");
     }
     greet(); // Output: Hello, Stranger!
     ```

#### 5. **Return Statement**
   - **Definition**: Functions can return a value using the `return` statement. The function execution stops when the `return` statement is reached.
   - **Example**:
     ```javascript
     function add(a, b) {
       return a + b;
     }
     const result = add(5, 3); // result = 8
     ```

### Callback Functions

#### 1. **Definition**
   - A callback function is a function passed as an argument to another function and is executed after the completion of that function.
   - **Example**:
     ```javascript
     function greet(name, callback) {
       console.log("Hello, " + name);
       callback();
     }

     function sayGoodbye() {
       console.log("Goodbye!");
     }

     greet("Alice", sayGoodbye); // Output: Hello, Alice \n Goodbye!
     ```

#### 2. **Asynchronous Callback**
   - Callbacks are often used in asynchronous operations, such as reading files, making network requests, or setting timers.
   - **Example**:
     ```javascript
     setTimeout(() => {
       console.log("This runs after 2 seconds");
     }, 2000);
     ```

### Array Functions

#### 1. **map()**
   - **Definition**: The `map()` method creates a new array by applying a function to each element of an array.
   - **Syntax**:
     ```javascript
     const newArray = array.map(function(currentValue, index, arr), thisValue);
     ```
   - **Example**:
     ```javascript
     const numbers = [1, 2, 3, 4];
     const squares = numbers.map(number => number * number);
     console.log(squares); // [1, 4, 9, 16]
     ```

#### 2. **filter()**
   - **Definition**: The `filter()` method creates a new array containing elements that pass a test provided by a function.
   - **Syntax**:
     ```javascript
     const newArray = array.filter(function(currentValue, index, arr), thisValue);
     ```
   - **Example**:
     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const evenNumbers = numbers.filter(number => number % 2 === 0);
     console.log(evenNumbers); // [2, 4]
     ```

#### 3. **reduce()**
   - **Definition**: The `reduce()` method executes a reducer function on each element of the array, resulting in a single output value.
   - **Syntax**:
     ```javascript
     const result = array.reduce(function(accumulator, currentValue, index, arr), initialValue);
     ```
   - **Example**:
     ```javascript
     const numbers = [1, 2, 3, 4];
     const sum = numbers.reduce((total, number) => total + number, 0);
     console.log(sum); // 10
     ```

