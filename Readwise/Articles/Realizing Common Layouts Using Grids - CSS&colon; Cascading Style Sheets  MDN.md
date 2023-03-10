# Realizing Common Layouts Using Grids - CSS&colon; Cascading Style Sheets   MDN

**Author:** mozilla.org  
**Full title:** Realizing Common Layouts Using Grids - CSS&colon; Cascading Style Sheets | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Realizing_common_layouts_using_CSS_Grid_Layout  
**Source:** #articles #reader #readwise

- We name areas using the [`grid-area`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-area) property. 
   
- this layout dictates a single column, and rows will be created as needed for each of the items in the implicit grid. 
   
- grid-template-areas: "header" "nav" "content" "sidebar" "ad" "footer"; 
   
- @media (min-width: 500px) { .wrapper { grid-template-columns: 1fr 3fr; grid-template-areas: "header header" "nav nav" "sidebar content" "ad footer"; } 
   
