### JavaScript Notes

#### 1. How to Add JavaScript to an HTML File

- **Inline Script:**
  You can write JavaScript code directly inside the HTML file using the `<script>` tag.
  ```html
  <html>
    <body>
      <h1>My Web Page</h1>
      <script>
        console.log("Hello, World!");
      </script>
    </body>
  </html>
  ```

- **External JavaScript File:**
  You can also write JavaScript in a separate file and link it to your HTML using the `src` attribute in the `<script>` tag.
  ```html
  <html>
    <body>
      <h1>My Web Page</h1>
      <script src="script.js"></script>
    </body>
  </html>
  ```
  *Note:* Ensure the `script.js` file is in the same directory as your HTML file, or specify the correct path.

- **In the Head Section:**
  You can place the `<script>` tag inside the `<head>` section of your HTML file.
  ```html
  <html>
    <head>
      <script>
        console.log("Hello from the head section!");
      </script>
    </head>
    <body>
      <h1>My Web Page</h1>
    </body>
  </html>
  ```
  *Note:* It's generally a good practice to place JavaScript at the end of the body for better performance unless it needs to run early.

#### 2. `console.log`, `prompt`, and `alert`

- **`console.log`:** 
  This function is used to print or log messages to the browser's console (useful for debugging).
  ```javascript
  console.log("This is a log message!");
  ```

- **`prompt`:** 
  This function displays a dialog box that prompts the user for input.
  ```javascript
  let userInput = prompt("Enter your name:");
  console.log("User's name is " + userInput);
  ```

- **`alert`:** 
  This function displays a simple message in a dialog box.
  ```javascript
  alert("This is an alert message!");
  ```

#### 3. Variables and How to Declare Them

- **`var`:** 
  Older way of declaring variables. It has function scope and can be redeclared.
  ```javascript
  var name = "John";
  console.log(name);
  ```

- **`let`:** 
  Modern way of declaring variables. It has block scope and cannot be redeclared in the same block.
  ```javascript
  let age = 25;
  console.log(age);
  ```

- **`const`:** 
  Declares a constant variable that cannot be reassigned after its initial assignment. It also has block scope.
  ```javascript
  const pi = 3.14;
  console.log(pi);
  ```

  *Note:* Use `let` and `const` for variable declarations in modern JavaScript, as they provide better scoping and prevent errors.

#### 4. Data Types in JavaScript

JavaScript has different data types, which can be categorized into two main types: **Primitive** and **Non-Primitive (Reference)**.

- **Primitive Data Types:**
  1. **String:** A sequence of characters used to represent text.
     ```javascript
     let greeting = "Hello, World!";
     ```

  2. **Number:** Represents both integer and floating-point numbers.
     ```javascript
     let age = 30;
     let price = 9.99;
     ```

  3. **Boolean:** Represents logical values: `true` or `false`.
     ```javascript
     let isAvailable = true;
     ```

  4. **Undefined:** A variable that has been declared but not assigned a value.
     ```javascript
     let name;
     console.log(name); // Output: undefined
     ```

  5. **Null:** Represents an intentionally empty value.
     ```javascript
     let value = null;
     ```

  6. **Symbol:** Represents a unique identifier.
     ```javascript
     let sym = Symbol("id");
     ```

  7. **BigInt:** Represents large integers beyond the safe integer limit.
     ```javascript
     let bigNumber = BigInt(9007199254740991);
     ```

- **Non-Primitive Data Types:**
  1. **Object:** Used to store collections of data or more complex entities.
     ```javascript
     let person = {
       name: "John",
       age: 30
     };
     ```

  2. **Array:** A special type of object used to store ordered lists of items.
     ```javascript
     let fruits = ["Apple", "Banana", "Mango"];
     ```

  3. **Function:** A block of code designed to perform a particular task.
     ```javascript
     function greet() {
       console.log("Hello, World!");
     }
     ```

#### 5. Objects: How to Create and Access Them

- **Creating an Object:**
  An object is a collection of properties, where each property has a key and a value.
  ```javascript
  let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30
  };
  ```

- **Accessing Object Properties:**
  You can access properties using dot notation or bracket notation.
  ```javascript
  console.log(person.firstName); // Dot notation
  console.log(person["lastName"]); // Bracket notation
  ```

- **Adding or Modifying Properties:**
  You can add or modify properties of an object.
  ```javascript
  person.job = "Developer"; // Adding a new property
  person.age = 31; // Modifying an existing property
  console.log(person);
  ```

- **Deleting Properties:**
  You can delete properties from an object using the `delete` keyword.
  ```javascript
  delete person.age;
  console.log(person);
  ```
