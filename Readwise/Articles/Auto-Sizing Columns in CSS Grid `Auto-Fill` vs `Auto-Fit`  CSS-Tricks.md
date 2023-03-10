# Auto-Sizing Columns in CSS Grid- `Auto-Fill` vs `Auto-Fit`   CSS-Tricks

**Author:** Sara Soueidan  
**Full title:** Auto-Sizing Columns in CSS Grid: `Auto-Fill` vs `Auto-Fit` | CSS-Tricks  
**URL:** https://css-tricks.com/auto-sizing-columns-css-grid-auto-fill-vs-auto-fit/  
**Source:** #articles #reader #readwise

- the `repeat()` function allows you to repeat columns as many times as needed 
   
- The `1fr` is what tells the browser to distribute the space between the columns so that each column equally gets one fraction of that space 
   
- grid-template-columns: repeat( 12, minmax(250px, 1fr) ); 
   
- The columns will not wrap into new rows if the viewport width is too narrow to fit them all with the new minimum width requirement, because we’re explicitly telling the browser to repeat the columns 12 times per row 
   
- To achieve wrapping, we can use the `auto-fit` or `auto-fill` keywords. 
   
- grid-template-columns: repeat( auto-fit, minmax(250px, 1fr) ); 
   
- the elements will wrap into rows when the width is not large enough to fit them in without any overflow 
   
- `auto-fill` FILLS the row with as many columns as it can fit. So it creates implicit columns whenever a new column can fit, because it’s trying to FILL the row with as many columns as it can. The newly added columns can and may be empty, but they will still occupy a designated space in the row. 
   
- `auto-fit` FITS the CURRENTLY AVAILABLE columns into the space by expanding them so that they take up any available space. The browser does that after FILLING that extra space with extra columns (as with `auto-fill` ) and then collapsing the empty ones. 
   
- Up to a certain point, both `auto-fill` and `auto-fit` show identical results 
   
- The difference between these two keywords is made apparent when the viewport gets wide enough to fit one (or more) extra column(s) (that) into the row. At that point, the browser is presented with two ways to handle the situation, and how it handles it largely depends on whether or not there is content to be placed into that extra column. 
   
- n the case where there is no content to place into a new column: “Do I allow this new column to occupy space in the row (and, therefore, affect the position and size of the rest of the rows)? or do I collapse that column and use its space to expand the other columns?” 
   
- `auto-fill` behavior: “*fill* that row up! Add as many columns as you can. I don’t care if they’re empty — they should all still show up 
   
- `auto-fit` does, too, fill the row with more columns are the viewport width increases, but the only difference is that the newly added columns (and any column gaps associated with them) are collapsed 
   
- `auto-fit` behavior: “make whatever columns you have fit into the available space. Expand them as much as you need to fit the row size. Empty columns must not occupy any space. Put that space to better use by expanding the filled (as in: filled with content/grid item 
   
- A useful tip to remember here is that the columns added in both cases (whether collapsed or not) are not implicit columns 
   
- The difference between `auto-fill` and `auto-fit` for sizing columns is only noticeable when the row is wide enough to fit more columns in it. 
   
