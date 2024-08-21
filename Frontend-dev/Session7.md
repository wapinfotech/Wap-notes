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
  *Note:* Make sure the `script.js` file is in the same directory as your HTML file or specify the correct path.

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
  *Note:* It's a good practice to place JavaScript at the end of the body for better performance unless it's necessary to run the script early.

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

#### 4. Objects: How to Create and Access Them
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
