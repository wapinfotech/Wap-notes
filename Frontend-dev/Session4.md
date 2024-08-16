# CSS Notes

## Introduction to CSS

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a web page. It allows you to control the layout, colors, fonts, and overall appearance of your website, making it visually appealing and user-friendly. CSS separates content from design, enabling you to maintain and update styles across multiple web pages efficiently.

## Inline, Style Tag, and .css File with Basic Syntax

### Inline CSS
Inline CSS is used to apply a unique style to a single HTML element. It is added directly within the HTML element's `style` attribute, making it convenient for quick changes but not ideal for maintaining large-scale websites.

**Syntax:**
```html
<p style="color: blue; text-align: center;">This is an inline CSS example.</p>
```

### Internal CSS (Style Tag)
Internal CSS is used to define styles for a single HTML document. It is placed within the `<style>` tag in the `<head>` section of the HTML file. This method is useful for applying styles to a single page without affecting other pages.

**Syntax:**
```html
<head>
    <style>
        p {
            color: blue;
            text-align: center;
        }
    </style>
</head>
```

### External CSS (.css File)
External CSS is used to apply styles to multiple HTML documents. It is stored in a separate `.css` file, which is linked to the HTML file using the `<link>` tag. This method is best for maintaining consistent styles across a large website.

**Syntax:**
```html
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
```

**styles.css:**
```css
p {
    color: blue;
    text-align: center;
}
```

## Selectors

CSS selectors are used to select HTML elements to apply styles. They can target elements based on their name, class, ID, attributes, and more.

- **Element Selector:** Selects all elements of a given type.
  ```css
  p {
      color: blue;
  }
  ```
  This selector applies styles to all `<p>` elements.

- **ID Selector:** Selects an element with a specific ID. Prefix with `#`.
  ```css
  #uniqueElement {
      color: green;
  }
  ```
  This selector applies styles to the element with the ID `uniqueElement`.

- **Class Selector:** Selects all elements with a specific class. Prefix with `.`.
  ```css
  .myClass {
      color: red;
  }
  ```
  This selector applies styles to all elements with the class `myClass`.

- **Attribute Selector:** Selects elements based on the presence of an attribute.
  ```css
  [type] {
      border: 1px solid black;
  }
  ```
  This selector applies styles to all elements that have a `type` attribute.

- **Descendant Selector:** Selects elements that are descendants of another element.
  ```css
  div p {
      color: purple;
  }
  ```
  This selector applies styles to all `<p>` elements that are within a `<div>` element.

## Text Properties

### Text Align
Controls the alignment of text within an element.
```css
p {
    text-align: center; /* options: left, right, center, justify */
}
```
This property aligns the text inside the `<p>` element to the center.

### Text Decoration
Adds decoration to text.
```css
p {
    text-decoration: underline; /* options: none, underline, overline, line-through */
}
```
This property adds an underline to the text inside the `<p>` element.

### Font Weight
Specifies the weight (boldness) of the font.
```css
p {
    font-weight: bold; /* options: normal, bold, bolder, lighter, 100-900 */
}
```
This property makes the text inside the `<p>` element bold.

### Font Family
Sets the font family for text.
```css
p {
    font-family: Arial, sans-serif;
}
```
This property sets the font of the text inside the `<p>` element to Arial, with sans-serif as a fallback.

### Font Size
Defines the size of the text.
```css
p {
    font-size: 16px; /* options: px, em, rem, %, etc. */
}
```
This property sets the font size of the text inside the `<p>` element to 16 pixels.

### Text Transform
Controls the capitalization of text.
```css
p {
    text-transform: uppercase; /* options: none, capitalize, uppercase, lowercase */
}
```
This property transforms the text inside the `<p>` element to uppercase letters.

## Box Model

### Height and Width
Sets the height and width of an element.
```css
div {
    height: 200px;
    width: 300px;
}
```
These properties set the height to 200 pixels and the width to 300 pixels for the `<div>` element.

### Border
Defines the border around an element.
```css
div {
    border: 1px solid black;
}
```
This property adds a 1-pixel solid black border around the `<div>` element.

### Margin
Creates space around elements, outside of any defined borders.
```css
div {
    margin: 10px;
}
```
This property adds a 10-pixel margin outside the `<div>` element.

### Padding
Creates space around content, inside of any defined borders.
```css
div {
    padding: 10px;
}
```
This property adds a 10-pixel padding inside the `<div>` element, around the content.

## Position

### Static
Default positioning of elements.
```css
div {
    position: static;
}
```
This is the default position for elements, placing them in the normal document flow.

### Fixed
Positions the element relative to the browser window.
```css
div {
    position: fixed;
    top: 10px;
    right: 10px;
}
```
This property positions the `<div>` element 10 pixels from the top and right of the browser window, and it stays fixed during scrolling.

### Relative
Positions the element relative to its normal position.
```css
div {
    position: relative;
    top: 10px;
    left: 10px;
}
```
This property moves the `<div>` element 10 pixels down and 10 pixels to the right from its normal position.

### Absolute
Positions the element relative to the nearest positioned ancestor.
```css
div {
    position: absolute;
    top: 10px;
    right: 10px;
}
```
This property positions the `<div>` element 10 pixels from the top and right of its nearest positioned ancestor.

### Sticky
Switches between relative and fixed positioning based on the user's scroll position.
```css
div {
    position: sticky;
    top: 0;
}
```
This property makes the `<div>` element stick to the top of the page when you scroll past it.

## Display

### Inline
Displays an element as an inline element (like `<span>`).
```css
div {
    display: inline;
}
```
This property makes the `<div>` element behave like an inline element, allowing other elements to flow around it.

### Block
Displays an element as a block element (like `<div>`).
```css
div {
    display: block;
}
```
This property makes the `<div>` element behave like a block element, starting on a new line and taking up the full width available.

### Inline-block
Displays an element as an inline-level block container.
```css
div {
    display: inline-block;
}
```
This property makes the `<div>` element behave like an inline element but allows you to set a width and height.

### None
Hides an element.
```css
div {
    display: none;
}
```
This property completely hides the `<div>` element, removing it from the document flow.
