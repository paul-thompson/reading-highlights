# Grid-Auto-Rows - CSS&colon; Cascading Style Sheets   MDN

**Author:** CSS Scroll Snap  
**Full title:** Grid-Auto-Rows - CSS&colon; Cascading Style Sheets | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-rows  
**Source:** #articles #instapaper #readwise

- The grid-auto-rows CSS property specifies the size of an implicitly-created grid row track or pattern of tracks 
   
- If a grid item is positioned into a row that is not explicitly sized by grid-template-rows, implicit grid tracks are created to hold it 
   
- either by explicitly positioning into a row that is out of range, or by the auto-placement algorithm creating additional rows. 
   
- minmax(min, max) 
   
- Is a functional notation that defines a size range greater than or equal to min and less than or equal to max. If max is smaller than min, then max is ignored and the function is treated as min 
   
- Represents the formula min(max-content, max(auto, argument)), which is calculated similar to auto (i.e. minmax(auto, max-content)), except that the track size is clamped at argument if it is greater than the auto minimum 
   
