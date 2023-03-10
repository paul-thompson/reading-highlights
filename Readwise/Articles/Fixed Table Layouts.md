# Fixed Table Layouts

**Author:** Chris Coyier  
**Full title:** Fixed Table Layouts  
**URL:** https://css-tricks.com/fixing-tables-long-strings/  
**Source:** #articles #reader #readwise

- The layout is fixed based on the first row. Set the width of those, and the rest of the table follows. 
   
- know that you can use the `<col>` element to set column widths too, because those effect the first row of cells and it’s all about that first row of cells setting the basis for the rest of the table. 
   
- I’ve heard that this style of table layout is *faster* as well, which stands to reason because the contents of the entire table don’t need to be analyzed to know how big column widths are going to be. I don’t have any data on that though 
   
