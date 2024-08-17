### CSS Positions

CSS positions are used to control the layout of elements on a webpage. There are several types of positioning available in CSS:

#### 1. Static Positioning

- *position: static;*
  - This is the default position for all HTML elements.
  - Elements are positioned according to the normal flow of the document.
  - They are not affected by top, bottom, left, and right properties.
  - Example:
    css
    .static-element {
        position: static;
    }
    

#### 2. Relative Positioning

- *position: relative;*
  - The element is positioned relative to its normal position.
  - The top, right, bottom, and left properties will offset the element from its normal position.
  - Example:
    css
    .relative-element {
        position: relative;
        top: 10px; /* Moves the element down by 10 pixels */
        left: 20px; /* Moves the element right by 20 pixels */
    }
    

#### 3. Absolute Positioning

- *position: absolute;*
  - The element is positioned relative to the nearest positioned ancestor (an element with a position other than static).
  - If there is no positioned ancestor, it uses the document body, and moves along with page scrolling.
  - Example:
    css
    .absolute-element {
        position: absolute;
        top: 50px;
        left: 100px;
    }
    

#### 4. Fixed Positioning

- *position: fixed;*
  - The element is positioned relative to the viewport, which means it stays in the same place even if the page is scrolled.
  - Example:
    css
    .fixed-element {
        position: fixed;
        top: 0;
        right: 0;
    }
    

#### 5. Sticky Positioning

- *position: sticky;*
  - The element is treated as relative until it crosses a specified point, then it is treated as fixed.
  - Useful for creating elements that stay fixed at the top of the page when scrolling.
  - Example:
    css
    .sticky-element {
        position: sticky;
        top: 0;
        background-color: yellow;
    }
    

### Flexbox

Flexbox is a one-dimensional layout method for arranging items in rows or columns. It is great for aligning items within a container.

#### Flex Container Properties

- *display: flex;* or *display: inline-flex;*
  - Defines a flex container and enables a flex context for all its direct children.
  - Example:
    css
    .flex-container {
        display: flex;
    }
    

- *flex-direction*
  - Defines the direction of the flex items in the flex container.
  - Values: row (default), row-reverse, column, column-reverse.
  - Example:
    css
    .flex-container {
        display: flex;
        flex-direction: row;
    }
    

- *justify-content*
  - Aligns flex items along the main axis.
  - Values: flex-start (default), flex-end, center, space-between, space-around, space-evenly.
  - Example:
    css
    .flex-container {
        display: flex;
        justify-content: center;
    }
    

- *align-items*
  - Aligns flex items along the cross axis.
  - Values: stretch (default), flex-start, flex-end, center, baseline.
  - Example:
    css
    .flex-container {
        display: flex;
        align-items: center;
    }
    

- *align-content*
  - Aligns flex lines when there is extra space in the cross axis.
  - Values: stretch (default), flex-start, flex-end, center, space-between, space-around.
  - Example:
    css
    .flex-container {
        display: flex;
        flex-wrap: wrap;
        align-content: space-between;
    }
    

- *flex-wrap*
  - Specifies whether the flex items should wrap or not.
  - Values: nowrap (default), wrap, wrap-reverse.
  - Example:
    css
    .flex-container {
        display: flex;
        flex-wrap: wrap;
    }
    

#### Flex Item Properties

- *order*
  - Defines the order of the flex items.
  - Example:
    css
    .flex-item {
        order: 2;
    }
    

- *flex-grow*
  - Defines the ability for a flex item to grow if necessary.
  - Default value is 0.
  - Example:
    css
    .flex-item {
        flex-grow: 1;
    }
    

- *flex-shrink*
  - Defines the ability for a flex item to shrink if necessary.
  - Default value is 1.
  - Example:
    css
    .flex-item {
        flex-shrink: 1;
    }
    

- *flex-basis*
  - Defines the default size of an element before the remaining space is distributed.
  - Example:
    css
    .flex-item {
        flex-basis: 100px;
    }
    

- *align-self*
  - Allows the default alignment to be overridden for individual flex items.
  - Example:
    css
    .flex-item {
        align-self: flex-end;
    }
    
