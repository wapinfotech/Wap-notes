## Links

### Basic Link
A link is created using the `<a>` tag, which stands for "anchor." The `href` attribute specifies the destination URL.

**Syntax:**
```html
<a href="https://www.example.com">Visit Example</a>
```
This creates a hyperlink that, when clicked, directs the user to "https://www.example.com".

### Open Link in a New Tab
To open a link in a new tab, use the `target="_blank"` attribute.

**Syntax:**
```html
<a href="https://www.example.com" target="_blank">Visit Example</a>
```
This will open "https://www.example.com" in a new browser tab when clicked.

## Tables

### Basic Table
A table is created using the `<table>` tag, with rows defined by `<tr>`, headers by `<th>`, and data cells by `<td>`.

**Syntax:**
```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>
```
This creates a simple table with one row of headers and one row of data.

### Table Attributes

- **`border`**: Adds a border around the table and its cells.
  ```html
  <table border="1">
      <!-- Table content -->
  </table>
  ```

- **`cellpadding`**: Adds padding inside each cell.
  ```html
  <table cellpadding="10">
      <!-- Table content -->
  </table>
  ```

- **`cellspacing`**: Sets the space between cells.
  ```html
  <table cellspacing="5">
      <!-- Table content -->
  </table>
  ```

- **`width`**: Sets the width of the table.
  ```html
  <table width="100%">
      <!-- Table content -->
  </table>
  ```

- **`align`**: Aligns the table on the page.
  ```html
  <table align="center">
      <!-- Table content -->
  </table>
  ```

- **`colspan`**: Spans a cell across multiple columns.
  ```html
  <tr>
      <td colspan="2">Spanning two columns</td>
  </tr>
  ```

- **`rowspan`**: Spans a cell across multiple rows.
  ```html
  <tr>
      <td rowspan="2">Spanning two rows</td>
  </tr>
  ```

## Input Elements

### Text Input
Used to create a single-line text input field.

**Syntax:**
```html
<input type="text" name="username">
```

### Password Input
Used to create a password field where the input is masked.

**Syntax:**
```html
<input type="password" name="password">
```

### Radio Button
Used to create a set of mutually exclusive options.

**Syntax:**
```html
<input type="radio" name="gender" value="male"> Male
<input type="radio" name="gender" value="female"> Female
```

### Checkbox
Used to create a checkbox, allowing multiple selections.

**Syntax:**
```html
<input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter
```

### Dropdown (Select)
Used to create a dropdown list.

**Syntax:**
```html
<select name="cars">
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
    <option value="fiat">Fiat</option>
    <option value="audi">Audi</option>
</select>
```

### Submit Button
Used to submit a form.

**Syntax:**
```html
<input type="submit" value="Submit">
```

### Reset Button
Used to reset form fields to their default values.

**Syntax:**
```html
<input type="reset" value="Reset">
```

## Forms

Forms are used to collect user input and send it to a server for processing.

### Basic Form
A form is created using the `<form>` tag, with various input elements nested inside.

**Syntax:**
```html
<form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name"><br><br>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br><br>
    
    <input type="submit" value="Submit">
</form>
```

### Form Attributes

- **`action`**: Specifies the URL where the form data will be sent.
  ```html
  <form action="/submit">
      <!-- Form content -->
  </form>
  ```

- **`method`**: Specifies the HTTP method to use when sending form data (`get` or `post`).
  ```html
  <form method="post">
      <!-- Form content -->
  </form>
  ```

- **`enctype`**: Specifies how form data should be encoded when submitted (for file uploads, use `multipart/form-data`).
  ```html
  <form enctype="multipart/form-data">
      <!-- Form content -->
  </form>
  ```

### Creating a Complete Form

**Example:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Sample Form</title>
</head>
<body>

<h2>Sample Form</h2>
<form action="/submit" method="post">
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="firstname"><br><br>
    
    <label for="lname">Last Name:</label>
    <input type="text" id="lname" name="lastname"><br><br>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br><br>
    
    <label for="gender">Gender:</label><br>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label><br>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label><br><br>
    
    <label for="cars">Choose a car:</label>
    <select id="cars" name="cars">
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="fiat">Fiat</option>
        <option value="audi">Audi</option>
    </select><br><br>
    
    <input type="checkbox" id="subscribe" name="subscribe" value="wapInfotech">
    <label for="subscribe"> Subscribe</label><br><br>
    
    <input type="submit" value="Submit">
    <input type="reset" value="Reset">
</form>

</body>
</html>
```
This example creates a form with fields for first name, last name, email, gender selection, car selection, and a subscription checkbox, along with submit and reset buttons.

## Audio

### Basic Audio Element
The `<audio>` tag is used to embed audio content in a web page. You can specify multiple sources for different audio formats using the `<source>` tag.

**Syntax:**
```html
<audio controls>
    <source src="audiofile.mp3" type="audio/mpeg">
    <source src="audiofile.ogg" type="audio/ogg">
    .
</audio>
```
The `controls` attribute adds play, pause, and volume controls to the audio player.

## Video

### Basic Video Element
The `<video>` tag is used to embed video content in a web page. Like the `<audio>` tag, you can specify multiple sources for different video formats using the `<source>` tag.

**Syntax:**
```html
<video width="320" height="240" controls>
    <source src="videofile.mp4" type="video/mp4">
    <source src="videofile.ogg" type="video/ogg">
</video>
```
The `width` and `height` attributes specify the dimensions of the video player, and the `controls` attribute adds play, pause, and volume controls.

## Iframes

### Basic Iframe
The `<iframe>` tag is used to embed another HTML document within the current document.

**Syntax:**
```html
<iframe src="https://www.example.com" width="600" height="400">
</iframe>
```
The `src` attribute specifies the URL of the page to embed, while the `width` and `height` attributes set the dimensions of the iframe.

### Iframe Attributes

- **`frameborder`**: Specifies whether or not to display a border around the iframe.
  ```html
  <iframe src="https://www.example.com" frameborder="0"></iframe>
  ```

- **`scrolling`**: Specifies whether or not to add scrollbars to the iframe.
  ```html
  <iframe src="https://www.example.com" scrolling="no"></iframe>
  ```

- **`name`**: Assigns a name to the iframe for targeting links.
  ```html
  <iframe src="https://www.example.com" name
