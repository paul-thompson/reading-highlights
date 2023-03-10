# A Very  Very in-Depth Guide on CSS Grid - CoderPad

**Author:** Victor Ikechukwu  
**Full title:** A Very, Very in-Depth Guide on CSS Grid - CoderPad  
**URL:** https://coderpad.io/blog/development/a-very-very-in-depth-guide-on-css-grid/  
**Source:** #articles #reader #readwise

- Floats affect a web page’s SEO 
   
- Table-based layouts lead to non-semantic markup on our sites, compromising [accessibility](https://coderpad.io/blog/development/introduction-to-web-accessibility-a11y/) 
   
- CSS Grid is a layout system—a method of organizing elements on a webpage—used for building two-dimensional layouts 
   
- It is a structure made up of intersecting horizontal and vertical lines known as grid lines that divide the layout of an HTML element into rows and columns 
   
- **Grid container:** The HTML element on which the grid layout is applied 
   
- **Grid item(s)**: All direct child elements of the grid container. 
   
- **Grid line:** These are the horizontal and vertical dividing lines that make up the structure of the grid 
   
- **Grid cell**: The space between two column grid lines and two adjacent row grid lines, also known as grid tracks 
   
- single unit of a grid and the smallest unit possible. By default, all grid items are laid out one item per grid cell. 
   
- **Grid track**: The area between two adjacent grid lines. The gap between two grid row lines is a row track, and the gap between two grid column lines is a column track. The size of a grid track determines the width and height of our grid items 
   
- **Grid area**: A rectangular area on the grid made up of one or more grid cells. Grid areas are created when a grid item spans over one-to-many grid tracks. They must be rectangular; 
   
- The value `grid` makes the parent grid element act a bit like an un-styled `div`, making it span the full width of a page by default due to them being block-level elements. In contrast, the value `inline-grid` behaves much like an un-styled `span`, making it act like an inline element to its siblings 
   
- Setting an element to a grid container alone will not immediately affect how the child elements are displayed, as we still haven’t specified how the layout should look. Hence, CSS lays out the grid items in a single-column grid 
   
- To change the layout of the grid items within a grid, we must explicitly define the rows and columns we want our grid to have. To do that, we’ll use the CSS properties `grid-template-columns` and `grid-template-rows`. 
   
- The `grid-template-columns` property lets us specify the number of columns we want in a grid container and how wide each column should be 
   
- The `grid-template-columns` property accepts one or more non-negative [CSS length unit](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#lengths) values 
   
- The `grid-template-rows property` lets us specify the height of each row in a grid container. 
   
- a grid container will implicitly create a new row whenever grid items wrap into new lines. Hence, we can’t control the number of rows that should be present in a grid using the `grid-template-rows` property. 
   
- the heights of these implicitly created rows will not be determined by the `grid-template-rows` property but by the size of their content. 
   
- The `column-gap` property adds some spacing between columns by adjusting the width of the vertical grid lines in a grid container 
   
- Just like `column-gap`, the `row-gap` property adds some spacing between rows in a grid container by adjusting the height of all horizontal grid lines in a grid container. 
   
- CSS Grid exposes six properties that let us control the alignment of grid items along the [rows (inline axis) or columns (block axis)](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Axis) of a grid container 
   
- The `justify-items` property controls the alignment of all grid items along a grid container’s inline(column) axis 
   
- The `justify-content` property lets you set the horizontal alignment of the entire grid within the inline (row) axis of the grid container 
   
- justify-self
  This behavior of the `justify-items` property that controls the alignment of grid items along the inline (row) axis of a grid container can also be set on individual grid items via the `justify-self` property 
   
- The `align-items` property controls the alignment of all grid items along a grid container’s block(column) axis 
   
- The `align-content` property lets you set the vertical alignment of the entire grid within the block (column) axis of the grid container. 
   
- align-self
  This behavior of the `align-items` property that controls the alignment of grid items along the block (column) axis of a grid container can also be set on individual grid items via the `align-self` property 
   
- `fr` unit, short for “fractional,” is a length unit introduced with the CSS Grid layout. It represents a fraction of the free space available in a grid container 
   
- As the layout becomes more complex, using percentages or any [CSS math function](https://coderpad.io/blog/development/an-overview-of-five-css-math-functions/) becomes unsustainable. This is when the `fr` unit comes in handy 
   
- The `min-content` is a sizing keyword that sets the width of a grid track to its [intrinsic minimum width](https://developer.mozilla.org/en-US/docs/Glossary/Intrinsic_Size), which is usually the size of the smallest content or text within its grid items. It works similarly [to the CSS function `min`](https://coderpad.io/blog/development/an-overview-of-five-css-math-functions/#min), but is used as a spacing unit instead of a function 
   
- The `max-content` sizing keyword has the opposite effect of `min-content`; `max-content` behaves similarly to [a CSS function: `max()`](https://coderpad.io/blog/development/an-overview-of-five-css-math-functions/#max). When applied to either a column or row, the track becomes as wide as possible for all the content within the grid items to display in one long unbroken line. 
   
