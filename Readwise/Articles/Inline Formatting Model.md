# Inline Formatting Model

**Author:** meyerweb.com  
**Full title:** Inline Formatting Model  
**URL:** https://meyerweb.com/eric/css/inline-format.html  
**Source:** #articles #instapaper #readwise

- inline formatting model 
   
- em-box = font-size = content-area 
   
- content-area + (half-)leading = inline box 
   
- inline box(min/max) = line-box 
   
- font-size = the value used with the em-box to scale the font for display 
   
- content-area = in non-replaced elements, the box described by the font-size of each character in the element, strung together; in replaced elements, the intrinsic height of the element plus any margins, borders, or padding 
   
- (half-)leading = the difference between font-size and line-height, applied equally above and below the content-area for each element 
   
- inline box = the addition of (half-)leading to the content-area for each element; for non-replaced elements, the height of the inline box of an element will be exactly equal to the value for line-height; for replaced elements, the height of the inline box of an element will be exactly equal to the intrinsic height of the element plus any margins, borders, or padding 
   
- line-box = the box which bounds the highest and lowest points of the inline boxes which are part of the line 
   
- the content-area is analogous to the content box of a block-level element 
   
- the background of an inline element is applied to the content-area plus any padding 
   
- any border on the inline element will surround the content-area plus any padding 
   
- margins on non-replaced elements have no vertical effects on inline elements or the boxes they generate (but will have horizontal effects) 
   
- margins and borders on replaced elements affect the height of the inline box for that element, and by implication the height of the line-box for that line 
   
- Consequences 
   
- The content-area is defined by the font-size of the elements, and the height of the line-box is equal to the value of line-height. 
   
- In the case of a line which contains inline elements, both replaced and non-replaced, which have differing font-size and line-height values, the solution is as follows. For each element, the content-area's height is taken from the font-size of each non-replaced element, and from the intrinsic height of a replaced element and any padding, borders, or margins it has 
   
- The leading is then applied to each element, half above and half below. This yields a number of inline boxes which are aligned according to the value(s) of vertical-align. The highest inline box's top defines the top of the line-box, and the lowest inline box's bottom defines the bottom of the line-box. 
   
- If a replaced element appears in the line, its content-area is equivalent to its intrinsic height and width, plus any padding, border, or margins. 
   
- line-height has no effect on the inline box of replaced elements 
   
