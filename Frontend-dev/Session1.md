
---

## Introduction to HTML

### Overview of HTML and Its Importance

**HTML (HyperText Markup Language)** is the standard language used to create and design web pages. It provides the fundamental structure for web content, allowing browsers to interpret and display text, images, links, and other elements in a readable format. HTML is essential for building websites and web applications because it defines the layout and organization of content.

### Basic Structure of an HTML Document

An HTML document is structured with several key components. Here is a basic example of an HTML document structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
    <style>
        /* CSS styles can be included here */
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
    </header>
    <main>
        <section>
            <h2>About Us</h2>
            <p>This is a brief description about us.</p>
        </section>
        <section>
            <h2>Our Services</h2>
            <p>Details about the services we offer.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Your Company</p>
    </footer>
</body>
</html>
```

**Description**:
- `<!DOCTYPE html>`: Declaration defining the document type and HTML version.
- `<html>`: Root element of the document.
- `<head>`: Contains meta-information about the document such as title and links to CSS.
- `<body>`: Contains the content of the document, including text, images, and other elements.
- `<header>`, `<main>`, `<section>`, `<footer>`: Structural elements defining different parts of the page.

### HTML Elements, Tags, and Attributes

**Elements** are the building blocks of HTML. They are defined by tags, which can be paired (opening and closing) or self-contained.

- **Tags**: HTML tags are used to create elements. Tags are enclosed in angle brackets, e.g., `<tag>`.
- **Attributes**: Provide additional information about an element. They are specified within the opening tag, e.g., `<tag attribute="value">`.

### Common HTML Elements

**Heading Tags**:
- **`<h1>` to `<h6>`**: Define headings with varying levels of importance.
  ```html
  <h1>Main Heading</h1>
  <h2>Subheading</h2>
  ```

**Paragraph Tag**:
- **`<p>`**: Defines a paragraph.
  ```html
  <p>This is a paragraph of text.</p>
  ```

**Line Break**:
- **`<br>`**: Inserts a line break, forcing the following content to start on a new line.
  ```html
  <p>Line one.<br>Line two.</p>
  ```

**Horizontal Rule**:
- **`<hr>`**: Inserts a horizontal line, often used to separate content.
  ```html
  <hr>
  ```

**Bold Text**:
- **`<b>`**: Makes text bold without implying any additional importance.
  ```html
  <p>This is <b>bold</b> text.</p>
  ```

**Italic Text**:
- **`<i>`**: Makes text italicized, often used for emphasis or titles.
  ```html
  <p>This is <i>italic</i> text.</p>
  ```

**Underlined Text**:
- **`<u>`**: Underlines text.
  ```html
  <p>This is <u>underlined</u> text.</p>
  ```

**Anchor Tag**:
- **`<a>`**: Creates a hyperlink to another page or location.
  ```html
  <a href="https://www.example.com">Visit Example</a>
  ```

**Image Tag**:
- **`<img>`**: Embeds an image. Use `src` for the image URL and `width`/`height` to specify dimensions.
  ```html
  <img src="image.jpg" alt="Description of image" width="300" height="200">
  ```

**Button Tag**:
- **`<button>`**: Creates a clickable button.
  ```html
  <button type="button">Click Me!</button>
  ```

---
