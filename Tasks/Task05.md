### Task: Creating and Accessing JavaScript Objects

**Objective:**  
In this task, you will create two objects with various properties. You will then access and display specific items (properties) from these objects using JavaScript.
Put any value of your choice to the properties of object


#### Step 1: Create Object 1

- Create an object named `student` with the following properties:
  - `name` (string)
  - `age` (number)
  - `grade` (string)
  - `rollNo` (number)

#### Step 2: Create Object 2

- Create another object named `book` with the following properties:
  - `title` (string)
  - `author` (string)
  - `pages` (number)
  - `isAvailable` (boolean)

#### Step 3: Access and Print Object Properties

- Access and print the following properties:
  - The `name` of the `student`.
  - The `grade` of the `student`.
  - The `title` of the `book`.
  - The `isAvailable` status of the `book`.

---

### Example Code Structure
Use the following structure as a guide:

```javascript
// Step 1: Create the student object
let student = {
    name: "Alice",
    age: 20,
    grade: "A",
    rollNo: 21
};
```

---

#### Step 4: Execute and Verify

1. Write the code in your JavaScript file or directly in the browser's developer console.
2. Execute the code to verify that the correct values are printed.

### Instructions to Run JavaScript with an External Script File

1. **Add Script File in HTML:**
   - Open your HTML file.
   - Inside the `<body>` tag, just before the closing `</body>` tag, add the following line to link your external JavaScript file:
     ```html
     <script src="script.js"></script>
     ```
   - Save the HTML file.

2. **Run the HTML File in a Live Server:**
   - If you are using an editor like VS Code, right-click on your HTML file and select "Open with Live Server" (you may need to install the Live Server extension).
   - This will launch your HTML file in the browser.

3. **Open Developer Tools:**
   - Once the webpage is loaded, right-click anywhere on the page and select "Inspect."
   - This will open the Developer Tools panel.

4. **Switch to the Console Tab:**
   - In the Developer Tools, click on the "Console" tab.
   - Here, you can see any output from your JavaScript code and also write and execute JavaScript directly in the console.
