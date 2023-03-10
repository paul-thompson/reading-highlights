# CSS Grid Layout

**Author:** freeCodeCamp.org  
**Full title:** CSS Grid Layout  
**URL:** https://www.freecodecamp.org/news/css-grid-layout/  
**Source:** #articles #reader #readwise

- Grid lets you move any *grid item* to any predefined *grid area* on the page. The items you move do not have to be adjacent. 
   
- Instead of moving the `<div>` from `<footer>` to `<aside>` in the HTML, you can just change it’s placement with `grid-area` in the CSS stylesheet. 
   
- In Grid, we apply layout styles to the parent container and not the items. Flex on the other hand targets the flex item to set properties like `flex-basis`, `flex-grow`, and `flex-shrink` 
   
- .container { display: grid; /* display grid by default */ } @supports not (display: grid) { /* if grid is not supported by the browser */ .container { display: flex; /* display flex instead of grid */ } } 
   
- Defining templates 
   
- Rows and columns 
   
- The `fr` unit 
   
- Grid introduces a new `fr` unit, which stands for *fraction*. The good thing about using the `fr` unit is that it takes care of calculations for you. Using `fr` avoids margin and padding issues. With `%` and `em` etc. 
   
