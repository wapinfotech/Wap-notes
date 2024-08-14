

---

## HTML Tags Overview

### 1. Structural HTML Tags

**`<sup>`**: 
- **Description**: Represents superscript text. Text within this tag appears slightly above the normal text line.
- **Usage Example**: `<p>H<sub>2</sub>O</p>` (renders as H₂O)

**`<sub>`**: 
- **Description**: Represents subscript text. Text within this tag appears slightly below the normal text line.
- **Usage Example**: `<p>E = mc<sup>2</sup></p>` (renders as E = mc²)

**`<pre>`**: 
- **Description**: Represents preformatted text. It maintains both whitespace and line breaks as typed in the HTML file.
- **Usage Example**:
  ```html
  <pre>
  This is preformatted text.
      It preserves spaces and new lines.
  </pre>
  ```

**`<div>`**: 
- **Description**: Defines a division or section in an HTML document. It is a block-level container that groups together other elements.
- **Usage Example**:
  ```html
  <div class="container">
    <h1>Header</h1>
    <p>Paragraph inside a div.</p>
  </div>
  ```

**`<section>`**: 
- **Description**: Represents a standalone section of content that is thematically related. It usually includes a heading.
- **Usage Example**:
  ```html
  <section>
    <h2>About Us</h2>
    <p>Information about us.</p>
  </section>
  ```

**`<nav>`**: 
- **Description**: Defines navigation links. It is used to enclose links to other pages or sections of the same page.
- **Usage Example**:
  ```html
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
  ```

**`<footer>`**: 
- **Description**: Represents the footer of a page or section. It typically contains information about the author, copyright, or related documents.
- **Usage Example**:
  ```html
  <footer>
    <p>&copy; 2024 Your Company</p>
  </footer>
  ```

### 2. Block-Level vs. Inline Elements

**Block-Level Elements**:
- **Description**: These elements start on a new line and take up the full width available. They stack vertically.
- **Examples**: `<div>`, `<p>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<nav>`

**Inline Elements**:
- **Description**: These elements do not start on a new line. They only take up as much width as necessary and flow within the surrounding text.
- **Examples**: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<sup>`, `<sub>`

### 3. Lists in HTML

**`<ul>`** (Unordered List):
- **Description**: Creates a list of items with bullet points.
- **Usage Example**:
  ```html
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
  ```

**`<ol>`** (Ordered List):
- **Description**: Creates a list of items with numbered points.
- **Usage Example**:
  ```html
  <ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
  </ol>
  ```

**`<dl>`** (Description List):
- **Description**: Creates a list of terms and their descriptions.
- **Usage Example**:
  ```html
  <dl>
    <dt>Term 1</dt>
    <dd>Description for term 1</dd>
    <dt>Term 2</dt>
    <dd>Description for term 2</dd>
  </dl>
  ```

### 4. Styling Notes

**`style` Attribute**:
- **Description**: Allows inline CSS styling directly within HTML tags.
- **Usage Example**: `<p style="color: blue; font-size: 16px;">This is a styled paragraph.</p>`

**Background Color**:
- **Description**: Sets the background color of an element.
- **Usage Example**: 
  ```html
  <div style="background-color: lightgrey;">
    Content with a light grey background.
  </div>
  ```

**Text Color**:
- **Description**: Sets the color of the text within an element.
- **Usage Example**:
  ```html
  <p style="color: #F26A23;">This is orange text.</p>
  ```

**Text Alignment**:
- **Description**: Aligns the text within an element.
- **Usage Example**:
  ```html
  <p style="text-align: center;">This text is centered.</p>
  <p style="text-align: right;">This text is aligned to the right.</p>
  ```

---
