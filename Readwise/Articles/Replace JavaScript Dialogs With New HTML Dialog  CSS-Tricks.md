# Replace JavaScript Dialogs With New HTML Dialog   CSS-Tricks

**Author:** css-tricks.com  
**Full title:** Replace JavaScript Dialogs With New HTML Dialog | CSS-Tricks  
**URL:** https://css-tricks.com/replace-javascript-dialogs-html-dialog-element/  
**Source:** #articles #instapaper #readwise

- you get a lot of modal-related features for free with alert(), confirm(), and prompt() that often go overlooked 
   
- It’s a true modal. As in, it will always be on top of the stack — even on top of that <div> with z-index: 99999 
   
- It’s accessible with the keyboard. Press Enter to accept and Escape to cancel. 
   
- It’s screen reader-friendly. It moves focus and allows the modal content to be read aloud 
   
- It traps focus. Pressing Tab will not reach any focusable elements on the main page, but in Firefox and Safari it does indeed move focus to the browser UI. 
   
- It supports user preferences. We get automatic light and dark mode support right out of the box. 
   
- It pauses code-execution., Plus, it waits for user input 
   
- Probably because they look like system errors that cannot be styled. Another big consideration: there has been movement toward their deprecation 
   
- It’s impossible to completely replace Javascript dialogs with identical functionality, but if we use the showModal() method of <dialog> combined with a Promise that can either resolve (accept) or reject (cancel) — then we have something almost as good. 
   
- A dialog class 
   
