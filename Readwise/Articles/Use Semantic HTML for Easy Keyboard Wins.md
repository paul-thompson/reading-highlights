# Use Semantic HTML for Easy Keyboard Wins

**Author:** Rob Dodson  
**Full title:** Use Semantic HTML for Easy Keyboard Wins  
**URL:** https://web.dev/use-semantic-html/  
**Source:** #articles #instapaper #readwise

- Keyboard support for free (and better mobile experiences 
   
- There are a number of built-in interactive elements with proper semantics and keyboard support. 
   
- The ones most developers use are 
   
- <a>
  <button>
  <input> (and its many types)
  <select>
  <textarea> 
   
- elements with the contenteditable attribute are sometimes used for freeform text entry. 
   
- Use button instead of div 
   
- to be considered accessible, a button should 
   
- Be focusable via the keyboard
  Support being disabled
  Support the ENTER or SPACE keys to perform an action
  Be announced properly by a screen reader 
   
- A div button has none of these things 
   
- button elements have a neat trick called synthetic click activation. If you add a "click" handler to a button, it will run when the user presses ENTER or SPACE 
   
- A div button doesn't have this feature 
   
- button is easy to style and full of accessibility wins! 
   
- Links versus buttons 
   
- Another common anti-pattern is to treat links as buttons 
   
- <a href="#" onclick=""> 
   
- If clicking on the element will perform an action on the page, use <button> 
   
- If clicking on the element will navigate the user to a new page then use <a>. This includes single page web apps that load new content and update the URL using the History API 
   
- buttons and links are announced differently by screen readers 
   
- Using built-in HTML elements can greatly improve the accessibility of your site, and significantly cut down on your workload. 
   
