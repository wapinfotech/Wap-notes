
### **1. Media Query**
**Introduction:**
- Media queries are a feature of CSS that allow you to apply styles based on the characteristics of the user's device, such as screen width, height, resolution, and orientation.

**Basic Syntax:**
```css
@media (condition) {
  /* CSS rules */
}
```
**Common Conditions:**
- **Screen Width (`min-width` and `max-width`)**:
  - `@media (min-width: 600px)`: Applies styles if the screen is at least 600px wide.
  - `@media (max-width: 600px)`: Applies styles if the screen is no wider than 600px.
- **Orientation (`orientation`)**:
  - `@media (orientation: landscape)`: Applies styles if the device is in landscape mode.
  - `@media (orientation: portrait)`: Applies styles if the device is in portrait mode.
- **Resolution (`min-resolution` and `max-resolution`)**:
  - `@media (min-resolution: 300dpi)`: Applies styles if the screen resolution is at least 300dpi.

**Example:**
```css
/* Default styles */
body {
  background-color: white;
}

/* Styles for screens wider than 600px */
@media (min-width: 600px) {
  body {
    background-color: lightgray;
  }
}
```

**Use Cases:**
- Responsive design: Adjust layouts for different screen sizes (e.g., mobile, tablet, desktop).
- High-DPI displays: Serve higher-resolution images or adjust font sizes.

---

### **2. Transition**
**Introduction:**
- Transitions allow changes in CSS properties to occur smoothly over a specified duration, rather than happening instantly.

**Basic Syntax:**
```css
selector {
  transition: property duration timing-function delay;
}
```
**Components:**
- **Property:** The CSS property to animate (e.g., `opacity`, `transform`, `background-color`).
- **Duration:** How long the transition lasts (e.g., `2s` for 2 seconds).
- **Timing Function:** The speed curve of the transition (e.g., `ease`, `linear`, `ease-in`, `ease-out`).
- **Delay:** Time before the transition starts (optional).

**Example:**
```css
.button {
  background-color: blue;
  transition: background-color 0.3s ease-in-out;
}

.button:hover {
  background-color: green;
}
```

**Use Cases:**
- Hover effects: Smoothly change background colors, borders, or shadows.
- Animating position changes: Gradually move elements from one place to another.
- Opacity changes: Fade elements in or out.

---

### **3. Transform**
**Introduction:**
- The `transform` property in CSS allows you to apply 2D or 3D transformations to elements, such as rotating, scaling, translating, or skewing.

**Basic Syntax:**
```css
selector {
  transform: transformation-function(value);
}
```
**Common Transformation Functions:**
- **Translate:** Moves the element from its current position.
  - `transform: translateX(50px);` (Moves element 50px to the right)
  - `transform: translateY(50px);` (Moves element 50px down)
- **Rotate:** Rotates the element around its center.
  - `transform: rotate(45deg);` (Rotates element by 45 degrees)
- **Scale:** Scales the size of the element.
  - `transform: scale(1.5);` (Increases size by 1.5 times)
  - `transform: scaleX(2);` (Doubles the width)
- **Skew:** Skews the element along the X or Y axis.
  - `transform: skewX(20deg);` (Skews element 20 degrees along the X-axis)
  - `transform: skewY(20deg);` (Skews element 20 degrees along the Y-axis)

**Example:**
```css
.box {
  transform: scale(1.2) rotate(45deg);
}
```

**Use Cases:**
- Interactive elements: Add visual effects like enlarging or rotating on hover.
- Complex animations: Combine multiple transformations for dynamic effects.
- Visual emphasis: Draw attention to specific elements by skewing or rotating.

