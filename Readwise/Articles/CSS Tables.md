# CSS- Tables

**Author:** Kudzanayi Dzvairo  
**Full title:** CSS: Tables  
**URL:** https://medium.com/@kudzanayi/css-tables-a70b235621d3  
**Source:** #articles #reader #readwise

- To get rid of this double border problem you can simply collapse the adjoining table cell borders and create clean single line borders 
   
- border-collapse: collapse 
   
- To add more space between the table cell contents and the cell borders, you can simply use the CSS padding property 
   
- By default a table will render just wide enough to contain all its contents 
   
- A table expands and contracts to accomodate the data contained inside it. This is its default behavior. As data fills the table it continues to expand as long as there is space. However to manage layout one must set a fixed width. 
   
- `table-layout` property. This property defines the algorithm to be used to layout the table cells, rows and columsn. This property take one of two values. 
   
- **auto** — Uses an automatic table layout algorithm. With this algorithm, the widths of the tables and its cells are adjusted to fit the content. This is the default value 
   
- **fixed —** Uses the fixed table layour algorithm. With this algorithm, the horizontal layout of the table does not depend on the contents of the cells; it only depends on the table’s width, the width of the columns, and borders or cell spacing.It is normally faster than auto. 
   
- For horizontal alignment of text inside the table cells you an use the text-align property in the same way as you use with other elements. You align text to either left, right, center or justify 
   
- Similarly you can do the same vertically and align elements to the top, bottom or middle using the CSS `vertical-align` property 
   
- You can set the vertical position of a table caption using the CSS `caption-side` property. This can be placed either top or bottom 
   
- Setting different background colors for alternate rows is a popular technique to improve the readability of tables that has a large amount of data. This is commonly known as zebra-striping a table
  You can simply achieve this effect by using the CSS `:nth-child()` pseudo-class selector
  tbody tr:nth-child(odd){ 
  background-color:#f2f2f2; 
  } 
   
- Tables are not responsive in nature. However, to support mobile dvies you can add responsiveness to your tables by enabling horizontal scrolling on small screens. To do this simply wrap your table with a <div> element and apply the style `overflow-x:auto`
  <div style="overflow-x: auto"> 
  <table> 
  ...table content... 
  </table> 
  </div> 
   
