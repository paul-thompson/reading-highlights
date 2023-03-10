# Naming Things in CSS Grid Layout

**Author:** Rachel Andrew  
**Full title:** Naming Things in CSS Grid Layout  
**URL:** https://www.smashingmagazine.com/2017/10/naming-things-css-grid-layout/  
**Source:** #articles #reader #readwise

- If we want to name the lines, we do so inside square brackets in the track listing. The key thing here is to **remember that you are naming the line, not the track that follows** 
   
- it is a good idea to name them with the suffix `-start` for start lines (whether row or column and `-end` for end lines). You might have `main-start` and `main-end`, or `sidebar-start` and `sidebar-end`. 
   
- Quite often the end line of one part of your grid and the start line of another coincide, and this is not a problem as lines can have multiple names. Create multiple names by adding them separated by a space — inside the square brackets 
   
- Lines With The Same Name 
   
- We have seen how lines can have multiple names, but you can also have multiple lines with the same name. This will happen if you use repeat notation and include named lines in the track listing 
   
- [The specification](https://www.w3.org/TR/css-grid-1/#common-uses-named-lines) describes this behaviour as “creating a named set of grid lines” which can be a helpful way of looking at the grid you have created with multiple lines of the same name. By adding the number you are then selecting which line of the set you wish to target 
   
- Maintaining Line Names While Redefining A Responsive Grid 
   
- Whether you choose to use line numbers or named lines is completely down to you. In general, lines can be useful where you wish to change the grid definition within media queries 
   
- Named Areas 
   
- A grid area is a rectangular area consisting of one or more grid cells. The area is defined by four grid lines marking out the start and end lines for columns and rows. 
   
- We name areas of the grid using the `grid-template-areas` property. This property takes a somewhat unusual value (a set of strings, one for each row) which describe our layout in ascii-art style 
   
- The names we use in the strings for `grid-template-areas` are assigned to the direct child elements of the grid using the `grid-area` property. The value of this property when used to assign a name is what is known as a *custom identifier*, so it should not be quoted 
   
- Whenever we describe our layout as the value of `grid-template-areas`, it will cause an area to cover more than one cell of the grid we repeat the ident along the row or down the columns. The area created must be a complete rectangle 
   
- When creating our grid description, we also need to create a complete representation of our grid, otherwise the whole declaration is thrown away as invalid. That means that every cell of the grid needs to be filled 
   
- From Named Lines Come Areas 
   
