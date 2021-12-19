# Understanding the CSS Box Model for Inline Elements – Mozilla Hacks - The Web Developer Blog

**Author:** Κατασκευή Ιστοσελίδων Θεσσαλονίκη  
**Full title:** Understanding the CSS Box Model for Inline Elements – Mozilla Hacks - The Web Developer Blog  
**URL:** https://hacks.mozilla.org/2015/03/understanding-inline-box-model  
**Source:** #articles #instapaper #readwise

- In a web page, every element is rendered as a rectangular box 
   
- Depending on the element’s display property, its box may be one of two types: a block box or an inline box. 
   
- Inline boxes are laid out horizontally in a box called a line box 
   
- If there isn’t enough horizontal space to fit all elements into a single line, another line box is created under the first one 
   
- When an inline box is split across more than one line, it’s still logically a single box. This means that any horizontal padding, border, or margin is only applied to the start of the first line occupied by the box, and the end of the last line 
   
- If you need to adjust the height between lines, use line-height instead 
   
- From Firefox 39 onwards, the box model overlay for split inline elements shows each individual line occupied by the element 
   
- Highlighting each individual line box is important for understanding how the box model is applied to inline elements, and also helps you check the space between lines and the vertical alignment of inline boxes 
   
