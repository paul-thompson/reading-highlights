# Should I Use Grid or Flexbox – Rachel Andrew

**Author:** @rachelandrew  
**Full title:** Should I Use Grid or Flexbox? – Rachel Andrew  
**URL:** https://rachelandrew.co.uk/archives/2016/03/30/should-i-use-grid-or-flexbox/  
**Source:** #articles #instapaper #readwise

- Major layouts vs. UI elements 
   
- When people first encounter CSS Grid Layout, they tend to think of Grid as being the controller of the major page layout 
   
- However once flex items wrap, each row (or column if working with flex-direction: column), becomes a flex container itself 
   
- Space distribution happens across that row or column, you lose the ability to line things up with items in rows above. 
   
- Flexbox is essentially for laying out items in a single dimension – in a row OR a column. Grid is for layout of items in two dimensions – rows AND columns. 
   
- One dimensional vs. Two dimensional 
   
- most of the flexbox problems I am asked about are due to developers trying to make flexbox do layout in two dimensions. This is where you need Grid Layout 
   
- In the Grid version we define our grid on the wrapper element, the Grid Items then just drop into the Grid Cells already defined 
   
- Working from the content out vs. working from the Grid definition in 
   
- Do you want to let your content control the way it is displayed, on a row by row or column by column basis? That’s flexbox 
   
- do you want to define a grid, and either allow items to be auto-placed into the cells defined by that grid, or control their positioning using line-based positioning or grid template areas. That’s grid. 
   
