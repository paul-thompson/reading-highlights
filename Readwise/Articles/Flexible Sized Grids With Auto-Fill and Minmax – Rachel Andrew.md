# Flexible Sized Grids With Auto-Fill and Minmax – Rachel Andrew

**Author:** rachelandrew.co.uk  
**Full title:** Flexible Sized Grids With Auto-Fill and Minmax – Rachel Andrew  
**URL:** https://rachelandrew.co.uk/archives/2016/04/12/flexible-sized-grids-with-auto-fill-and-minmax/  
**Source:** #articles #reader #readwise

- To create a grid with as many 100 pixel tracks as will fit in the container we can use the auto-fill keyword rather than a number. 
   
- “ the number of repetitions is the largest possible positive integer that does not cause the grid to overflow its grid container (treating each track as its max track sizing function if that is definite or as its minimum track sizing function otherwise, and taking grid-gap into account)” 
   
- minmax() 
   
- To achieve a truly flexible grid – flexible both in size of tracks and number – we need an additional piece of the puzzle – [minmax()](https://drafts.csswg.org/css-grid/#valdef-grid-template-columns-minmax). We can give this function a minimum and maximum size that we want our track to be. 
   
- we could use the fraction unit as our maximum value. This would result in tracks of a minimum of 100 pixels and a maximum of 1 fraction unit of the available space. After as many 100 pixel tracks are assigned, we then have the remaining space to distribute 
   
