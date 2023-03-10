# Another Collection of Interesting Facts About CSS Grid   CSS-Tricks

**Author:** @matuzo  
**Full title:** Another Collection of Interesting Facts About CSS Grid | CSS-Tricks  
**URL:** https://css-tricks.com/another-collection-of-interesting-facts-about-css-grid/  
**Source:** #articles #instapaper #readwise

- Understanding how the `grid` shortcut works 
   
- <‘grid-template’> | <‘grid-template-rows’> / [ auto-flow && dense? ] <‘grid-auto-columns’>? | [ auto-flow && dense? ] <‘grid-autwo-rows’>? / <‘grid-template-columns’> 
   
- Note that you can only specify the explicit or the implicit grid properties in a single grid declaration. 
   
- Using `grid` in favor of `grid-template` 
   
- The grid-template property is a shorthand for setting grid-template-columns, grid-template-rows, and grid-template-areas in a single declaration 
   
- grid: "one one" 200px 
  "two four" 
  "three four" 
  / 1fr 2fr; 
   
- This shorthand creates three rows and two columns, with four named grid areas. The first row has an explicit height of 200px, while the second and the third have an implicit height of auto. The first column has a width of 1fr and the second a width of 2fr. 
   
- grid-template-rows: 100px 300px;
  grid-template-columns: 3fr 1fr;
  grid: 100px 300px / 3fr 1fr; 
   
- Handling implicit rows and columns 
   
- It’s possible to use the grid shorthand to specify grid-auto-flow as well 
   
- If it’s to the left of the slash, the shorthand sets grid-auto-flow to row and creates explicit columns. 
   
- grid: auto-flow / 200px 
   
- If it’s to the right of the slash, the shorthand sets grid-auto-flow to column and creates explicit rows. 
   
- grid: 100px 300px / auto 
   
- We can also set the size of implicit tracks together with the auto-flow keyword, which respectively sets grid-auto-rows or grid-auto-columns to the specified value. 
   
- grid: 100px 300px / auto-flow 200px; 
   
- Feature queries in Edge 
   
- all browsers that support Grid also understand feature queries 
   
- we can check if a browser supports the old or the new spec, or both. Both, you ask? Starting with Edge 16, Edge does not just support the new spec, but the old one as well. 
   
- As a side note, you shouldn’t go overboard with (mis)using feature queries for browser sniffing, because browser detection is bad. 
   
- Specifying the exact number of items per column 
   
- By default, it fills in each row, in turn, adding new rows as necessary. If we set grid-auto-flow to column, grid will fill each column in turn instead, which is what we want. The last thing we have to do is specify the number of items per column. This is possible by defining as many explicit rows as needed using the grid-template-rows property 
   
- Sticky footers with CSS Grid 
   
- html {
  height: 100%;
  }
  body {
  min-height: 100%;
  display: grid;
  grid-template-rows: auto 1fr auto;
  } 
   
- Automatic minimum size of grid items 
   
- Broadly speaking, this happens, because a grid item can’t be smaller than its children. The default min-width of a grid-item (or flex-item) is set to auto 
   
- …applies an automatic minimum size in the specified axis to grid items whose overflow is visible and which span at least one track whose min track sizing function is auto 
   
