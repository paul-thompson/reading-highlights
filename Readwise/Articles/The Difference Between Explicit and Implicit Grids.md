# The Difference Between Explicit and Implicit Grids

**Author:** Manuel Matuzovic  
**Full title:** The Difference Between Explicit and Implicit Grids  
**URL:** https://css-tricks.com/difference-explicit-implicit-grids/  
**Source:** #articles #reader #readwise

- [Grid Layout](https://www.w3.org/TR/css-grid-1/) finally gives us the ability to define grids in CSS and place items into grid cells 
   
- Grids are flexible enough to adapt to their items 
   
- We can define a fixed number of lines and tracks that form a grid by using the properties `grid-template-rows`, `grid-template-columns`, and `grid-template-areas` 
   
- manually defined grid is called *the explicit grid*. 
   
- An explicit grid with 4 vertical tracks (columns) and 2 horizontal tracks (rows) 
   
- Instead of setting a fixed number of repetitions we can use the `auto-fill` and `auto-fit` keywords. 
   
- `auto-fill` keyword creates as many tracks as fit into the grid container without causing the grid to overflow it 
   
- Note that `repeat(auto-fill, 1fr);` will only create one track because a single track with a width of `1fr` already fills the whole grid container is an invalid declaration *(maybe it changed? I dunno)* 
   
   - Note: Check this
   
- The `auto-fit` keyword behaves the same way as `auto-fill`, except that after grid item placement it will only create as many tracks as needed and any empty repeated track collapses 
   
- items placed outside of the explicit grid causing the creation of implicit lines and tracks 
   
- The widths and heights of the implicit tracks are set automatically. They are only big enough to fit the placed grid items, but it’s possible to change this default behavior 
   
