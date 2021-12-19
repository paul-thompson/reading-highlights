# How CSS Box Sizing Works - Piccalilli

**Author:** piccalil.li  
**Full title:** How CSS Box Sizing Works - Piccalilli  
**URL:** https://piccalil.li/tutorial/how-css-box-sizing-works/  
**Source:** #articles #instapaper #readwise

- pretty much everything is a box. Regardless of how an element looks visually, it’s still a box. 
   
- Padding and borders 
   
- When we add padding and borders to an element: by default, their values will be added to the computed width and height. 
   
- .box {
  box-sizing: border-box;
  } 
   
- account for the padding and border too, instead of adding them to the size”. 
   
- You can think of the box’s width now as an absolute value, where before it was a base value that was affected by other elements 
   
- Setting box-sizing: border-box provides clarity and predictability, which for a lot of developers, makes CSS much more accessible and understandable 
   
- /* Reset rule */
  *,
  *::before,
  *::after {
  box-sizing: border-box;
  } 
   
- Setting box-sizing: border-box is such a life saver for front-end developers 
   
