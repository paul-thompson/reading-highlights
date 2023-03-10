# Placing  Spanning  and Density in CSS Grid   DigitalOcean

**Author:** digitalocean.com  
**Full title:** Placing, Spanning, and Density in CSS Grid | DigitalOcean  
**URL:** https://www.digitalocean.com/community/tutorials/placing-spanning-and-density-in-css-grid  
**Source:** #articles #reader #readwise

- A generic grid definition applied to the grid container is enough for a basic layout structure. However, when you need more control over the contents of the grid, the grid container is limited its uses. 
   
- Placing Grid Items: Start Here, End There 
   
- When you have a grid, the grid items have placement values defined by `grid-[x]-start` and `grid-[x]-end` (where `x` can be `column` or `row`). The value is auto. 
   
- • To start at **line** one, `grid-column-start: 1;`
  • And end at **line** 5, `grid-column-end: 5;` 
   
- .item:nth-child(22) { grid-row-start: 1; grid-row-end: 4; } 
   
- `grid-row-[x]` will reset the grid item default placement to start at column line 1 and row line 1, then the placement spanning will occur 
   
- If you want it to stay at its original column track, then you have to explicitly state that 
   
- The tricky thing to watch out for is that if you change only the value of `grid-[x]-start`, the grid item will start at the **line**, not the track 
   
- if you specify `end` only, it will start from the specified end value and span the grid inversely. For example, if you tell item `10` to end at `3`, it will start from the nearest next line `2` and draw to line `3` 
   
