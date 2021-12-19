# A Use Case for CSS Min-Content and Max-Content

**Author:** stefanjudis.com  
**Full title:** A Use Case for CSS Min-Content and Max-Content  
**URL:** https://www.stefanjudis.com/today-i-learned/a-use-case-for-css-min-content-and-max-content/  
**Source:** #articles #instapaper #readwise

- you can use min-content, max-content and even fit-content to define an element's width. 
   
- these values is that they consider the element's content and children. 
   
- max-content determines a size assuming that there is infinite available space. 
   
- min-content defines an element's minimal possible size that does not lead to overflowing content 
   
- fit-content is the mix of min-content and max-content; if there's enough space, it defines as much size as possible, and otherwise, it falls back to a minimum size that does not include overflowing elements. 
   
- Another great use case for fit-content is when you want to build a centered navigation. 
   
