# Keyboard Access Fundamentals

**Author:** Rob Dodson  
**Full title:** Keyboard Access Fundamentals  
**URL:** https://web.dev/keyboard-access/  
**Source:** #articles #instapaper #readwise

- Many different users rely on the keyboard to navigate applications—from users with temporary and permanent motor impairments to users who use keyboard shortcuts to be more efficient and productive. 
   
- Focus and the tab order 
   
- At a given moment, focus refers to what element in your application (such as a field, checkbox, button, or link) currently receives input from the keyboard. 
   
- To move the focus on a page, use TAB to navigate "forward" and SHIFT + TAB to navigate "backward." 
   
- The currently focused element is often indicated by a focus ring, and various browsers style their focus rings differently. 
   
- The order in which focus proceeds forward and backward through interactive elements is called the tab order. 
   
- Interactive HTML elements like text fields, buttons, and select lists are implicitly focusable: they are automatically inserted into the tab order based on their position in the DOM 
   
- Implementing a logical tab order is an important part of providing your users with a smooth keyboard navigation experience. 
   
- Arrange elements in the DOM to be in logical order 
   
- Correctly set the visibility of offscreen content that should not receive focus 
   
- Arrange elements in the DOM to be in logical order 
   
- If the focus order seems wrong, you should rearrange the elements in the DOM to make the tab order more natural. 
   
- If you want something to appear visually earlier on the screen, move it earlier in the DOM. 
   
- Be careful when changing the visual position of elements using CSS to avoid creating an illogical tab order. 
   
- Correctly set the visibility of offscreen content 
   
- To prevent a particular interactive element from receiving focus, you should give the element either of the following CSS properties 
   
- display: none
  visibility: hidden 
   
- To add the element back into the tab order 
   
- display: block
  visibility: visible 
   
- If you can't figure out where the focus on your page is as you're tabbing, open the console and type: document.activeElement. 
   
