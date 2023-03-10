# Using CSS Grid the Right Way

**Author:** Violet Peña  
**Full title:** Using CSS Grid the Right Way  
**URL:** https://vgpena.github.io/using-css-grid-the-right-way/  
**Source:** #articles #reader #readwise

- “Learning” CSS Grid requires developing working knowledge of many new properties that don’t just describe *one* aspect of appearance or behavior, but feed into a completely new layout system 
   
- system includes [around 18](https://css-tricks.com/snippets/css/complete-guide-grid/) properties which use paradigms and syntax rarely (or never) seen anywhere else in the CSS spec. 
   
- Grid columns and rows, at their most basic, are referred to by number 
   
- an amazing feature of Grid: you can give your rows and columns specific names. You should take advantage of this whenever possible 
   
- Adding names to your grid brings a couple of major benefits. 
   
- **Readability —** Right off the bat, your code is easier to understand. Line 3 now *describes* everything going on inside of the Grid container. You’re not just listing out columns; you’re outlining the *intent* of each column. 
   
- Assigning a column name, however, signals that this element has specifically been accounted for within the larger system. Naming also makes it easier to find the original column declaration, should we need to. 
   
- **Future-proofing —** Adding names makes your CSS more flexible 
   
- Without using named columns, you would have to update the column numbe 
   
- CSS Grid introduces the `fr` unit, which tells an area to occupy some fraction of the total available space 
   
- The `fr` unit is different from `%` or `vw` because while the latter units describe portions of a 100-unit whole, `fr`s are defined by the space not already used by something else. `fr`s split up this space relative to each other. 
   
- **Readability and clearer intent —** Using `fr`s, unlike using percents, lets us stick with whole numbers that are sized relative to each other, not relative to a whole. This keeps the intended behavior clear 
   
- **Less math —** The biggest benefit of the `fr` is that it takes the responsibility for doing exact arithmetic away from the developer and hands it off to the browser’s layout engine 
   
- Any change to `grid-column-gap` or to our column count will break the layout 
   
   - Note: Layout breaks when using percentages
   
- grid-template-columns: repeat(14, 1fr); 
   
- grid-template-columns: [left-gutter] 1fr [sidebar] 4fr [content] 8fr [right-gutter] 1fr 
   
- Pixels and columns are less salient than relationships and proportional space. 
   
