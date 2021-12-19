# Debugging CSS

**Author:** Ahmad Shadeed  
**Full title:** Debugging CSS  
**Source:** #books #api_book #readwise

- It’s worth mentioning that when we assign display: flex to an element, the flex container establishes a new flex formatting context. Adding float won’t work. Moreover, there is no margin collapse for the child items of a flex container 
   
- Some HTML Elements Can’t Be Flex Containers 
   
- Elements such as button, fieldset, and summary don’t work as flex containers. 
   
- The browser’s default rendering of those element’s UI conflicts with the display: flex declaration. 
   
- The padding property adds space inside an element. That’s what differentiates it from margin. 
   
- By default, an HTML img will be sized according to its content 
   
- The initial width of block-level elements such as div and p is auto, which lets the elements take up the full width of their parent 
   
- Setting the width to 100% would cause its contents to take up the full width of its parent without the margin being calculated. 
   
- You can’t set a percentage-based height for an element unless the height of its parent is explicitly defined. 
   
- If the value of min-width is greater than that of max-width, then it will be taken as a width. 
   
- A common use case for the max-width property is to add it as a constraint on an element, such as a page wrapper or container. 
   
- Horizontal scrolling is an indication that an element is positioned outside the viewport’s boundaries or that an element is wider than the viewport. 
   
- Firefox shows a “scroll” label for elements that are wider than the viewport 
   
- When you click on the scroll label, Firefox will highlight the element that is causing the horizontal scrolling. 
   
- Making the scrollbars visible can help us to spot scrolling issues much more quickly. 
   
- Windows shows the scrollbars by default, so there is no need to do anything there. 
   
- A fixed width will definitely cause horizontal scrolling. 
   
