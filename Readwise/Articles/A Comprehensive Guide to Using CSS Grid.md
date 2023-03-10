# A Comprehensive Guide to Using CSS Grid

**Author:** Ahmed Abuelgasim  
**Full title:** A Comprehensive Guide to Using CSS Grid  
**URL:** https://www.creativebloq.com/advice/a-comprehensive-guide-to-using-css-grid  
**Source:** #articles #reader #readwise

- CSS Grid enables us to achieve extremely diverse and device-specific layouts from the same exact HTML markup. 
   
- **grid-template-columns: 10px auto** leads to a 10px column followed by a second column that fills all available space. 
   
- Grid also uses a 'fractional' unit **fr** that causes any remaining space to be distributed to columns or rows based on the ratios of these units 
   
- Once a grid is created, grid lines, represented by dotted lines in the images, are automatically numbered from the top for rows or from the left for columns. The lines are also given a second, negative number relative to their index from the bottom for rows or from the right for columns. 
   
- Similar to [Flexbox](https://www.creativebloq.com/advice/the-web-designer-s-guide-to-flexbox), the horizontal and vertical position of items placed in the grid can be controlled by setting **justify-items** and **align-items** respectively, to **start**, **center**, **end** or **stretch**. 
   
- Positioning items using line number 
   
- To place an item in the grid we can set its **grid-column-start** and **grid-column-end** properties to the vertical line numbers between which the item should be stretched. For rows, the properties are **grid-row-start** and **grid-row-end** – and of course the numbers refer to the horizontal lines 
   
- Use the span keyword to determine the number of columns or rows you would like an item to span 
   
- the property **grid-area**, which is a shorthand for **grid-row-start**, **grid-column-start**, **grid-row-end** and **grid-column-end** in that order 
   
- #item1 { grid-area: 2 / 1 / span 2 / span 3; } #item2 { grid-area: 4 / 4; } 
   
- Positioning items using area names 
   
- Although using grid line numbers and the **span** keyword is a great way of positioning items, there is an even more intuitive and easy way to place items in the grid. It involves using the **grid-area** and **grid-template-areas** properties. 
   
- Empty cells are symbolised by a full stop (**.**) and spaces signify vertical grid lines. The rows can be placed on new lines to provide a visual representation of the grid 
   
- the number of grid columns and rows can even be changed to make allowances for certain screen sizes, if this is desired, by redefining **grid-template-columns** and/or **grid-template-rows** within the media queries 
   
- CSS Grid fallbacks for older browsers 
   
- We can alternatively add a basic fallback layout using **@supports**, a query that applies rules based on browser support for a specific CSS feature 
   
- If for some reason you need this fallback to be shown for Internet Explorer 10 and 11, which don’t support Grid nor, ironically, the **@supports** query, you can use a well-known query that applies styles only in IE10 and 11 
   
- @media (min-width: 721px) and (-ms-high-contrast: none), (-ms-high-contrast: active) { .header, .extra { float: left; width: 50%; } } 
   
- If you require IE9 and older support, load an additional stylesheet in the HTML with the relevant styles using:
  <!--[if IE]><link rel="stylesheet" href="ie.css" /><![endif]--> 
   
