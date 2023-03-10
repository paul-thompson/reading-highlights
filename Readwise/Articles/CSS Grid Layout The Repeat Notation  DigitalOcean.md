# CSS Grid Layout- The Repeat Notation   DigitalOcean

**Author:** digitalocean.com  
**Full title:** CSS Grid Layout: The Repeat Notation | DigitalOcean  
**URL:** https://www.digitalocean.com/community/tutorials/css-css-grid-layout-repeat-notation  
**Source:** #articles #reader #readwise

- Repeat() is a notation that you can use with the `grid-template-columns` and `grid-template-rows` properties to make your rules more concise and easier to understand when creating a large amount of columns or rows. 
   
- container { display: grid; grid-gap: 10px 15px; grid-template-columns: repeat(3, 1fr 2fr); grid-template-rows: repeat(2, 100px auto 20%); } 
   
- The first value passed to repeat() is the number of repetitions and the second value is the grid tracks to repeat 
   
- Repeat() with named lines 
   
- container { display: grid; grid-auto-flow: column dense; grid-template-columns: repeat(4, [col] 1fr); grid-template-rows: repeat(5, [row] 150px); } 
   
- Named grid lines at the end of repeat notations end up sharing the same line as the next starting name line 
   
