# Auto-Placement in Grid Layout - CSS&colon; Cascading Style Sheets   MDN

**Author:** mozilla.org  
**Full title:** Auto-Placement in Grid Layout - CSS&colon; Cascading Style Sheets | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Auto-placement_in_CSS_Grid_Layout  
**Source:** #articles #reader #readwise

- The default for automatically created rows in the implicit grid is for them to be auto-sized. 
   
- You can however control the size of these rows with the property `grid-auto-rows` 
   
- You can use [`minmax()`](https://developer.mozilla.org/en-US/docs/Web/CSS/minmax) in your value for [`grid-auto-rows`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-rows) enabling the creation of rows that are a minimum size but then grow to fit content if it is taller 
   
- grid-auto-rows: minmax(100px, auto); 
   
- You can also pass in a track listing, this will repeat 
   
- You can also ask grid to auto-place items by column. Using the property [`grid-auto-flow`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-flow) with a value of `column` 
   
