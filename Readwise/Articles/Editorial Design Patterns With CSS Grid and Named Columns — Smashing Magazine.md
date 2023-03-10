# Editorial Design Patterns With CSS Grid and Named Columns — Smashing Magazine

**Author:** Rachel Andrew  
**Full title:** Editorial Design Patterns With CSS Grid and Named Columns — Smashing Magazine  
**URL:** https://www.smashingmagazine.com/2019/10/editorial-design-patterns-css-grid-subgrid-naming/  
**Source:** #articles #reader #readwise

- Naming Things In CSS Grid Layout 
   
- When using CSS Grid Layout, you can name lines and areas 
   
- Defining naming conventions for things in your layout can be useful when working with your team; it is much easier to understand where anything placed with `grid-area: content` will end up than having something placed from `column-line: 3 / 9` 
   
- When using the `grid-template-areas` approach, you give the items that you want to place on the grid a name by using the `grid-area` property and then placing them around the grid. 
   
- This works well for components where you have one item to go into one area; however, if you want to place multiple things into the content area (one below the other), using `grid-area` is the wrong approach. Instead, you might define names for the column lines and place the item from the start to end line. 
   
- We Can Name Lines 
   
- we can name lines on the grid that can be pretty much anything we like — other than the word `span`. 
   
- We name our lines inside square brackets. Lines can (and often need to) have multiple names. 
   
- When placing the items using line-based positioning, you can pick any name for the line to do the placement. 
   
- With our named lines in place, we could place our items using `grid-column` by specifying the start and end line name. This pattern is just the same as using line numbers, so the name before the slash is the start line and the name after is the end line. 
   
