# Style a Parent Element Based on Its Number of Children Using CSS -Has

**Author:** byBramus!  
**Full title:** Style a Parent Element Based on Its Number of Children Using CSS :Has  
**URL:** https://www.bram.us/2022/11/17/style-a-parent-element-based-on-its-number-of-children-using-css-has/  
**Source:** #articles #reader #readwise

- In CSS it’s possible to style elements based on the number of siblings they have by [leveraging the `nth-child` selector](https://www.bram.us/2015/03/04/quantity-queries-for-css/). 
   
- /* At most 3 (3 or less, excluding 0) children */ ul:has(> :nth-child(-n+3):last-child) { outline: 1px solid red; } /* At most 3 (3 or less, including 0) children */ ul:not(:has(> :nth-child(3))) { outline: 1px solid red; } /* Exactly 5 children */ ul:has(> :nth-child(5):last-child) { outline: 1px solid blue; } /* At least 10 (10 or more) children */ ul:has(> :nth-child(10)) { outline: 1px solid green; } 
   
- /* Between 7 and 9 children (boundaries inclusive) */ ul:has(> :nth-child(7)):has(> :nth-child(-n+9):last-child) { outline: 1px solid yellow; } 
   
- The pattern of each selector built here is this:
  parent:has(> count-condition) {
  …
  } 
   
- By using [`parent:has()`](https://brm.us/css-has) we can select the `parent` element that meets a certain condition for its children. 
   
- By passing `>` into `:has()`, we target the `parent`’s **direct** children. 
   
- The `*count-condition*` is something we need to come up with for each type of selection we want to do. Similar to Quantity Queries, we’ll leverage `:nth-child()` for this. 
   
- At most `x` children 
   
