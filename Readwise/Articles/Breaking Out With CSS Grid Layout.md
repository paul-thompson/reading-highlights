# Breaking Out With CSS Grid Layout

**Author:** Tyler Sticka  
**Full title:** Breaking Out With CSS Grid Layout  
**URL:** https://cloudfour.com/thinks/breaking-out-with-css-grid-layout/  
**Source:** #articles #reader #readwise

- .Prose { display: grid; grid-template-columns: [full-start] minmax(1em, 1fr) [main-start] minmax(0, 40em) [main-end] minmax(1em, 1fr) [full-end]; } 
   
- Here we’ve defined three columns. The first and last are our gutters, with a minimum size of `1em` but the ability to stretch to fill one unit of available space. Between them is our main content column, which can stretch to a maximum width of `40em` 
   
- We’ve also assigned names (in brackets) to [the dividing lines between columns](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines). These are entirely optional, but they’ll make the rest of our styles easier to read, write and maintain. 
   
- .Prose > * { grid-column: main; } 
   
- .Prose-splash { grid-column: full; } 
   
- no `overflow-x` or negative margins required 
   
- While this technique has some really promising qualities, there are also some drawbacks to consider 
   
- You can’t `float` immediate children of an element with `display: grid`. 
   
