# Make a Button Element Look Like a Link - Piccalilli

**Author:** piccalil.li  
**Full title:** Make a Button Element Look Like a Link - Piccalilli  
**URL:** https://piccalil.li/quick-tip/link-button/  
**Source:** #articles #instapaper #readwise

- you can make a proper <button> element look like a link and retain all of that accessibility and semantic goodness with only a tiny bit of CSS 
   
- .link-button {
  display: inline;
  padding: 0;
  border: 0;
  font: inherit;
  text-decoration: underline;
  cursor: pointer;
  background: transparent;
  color: currentColor;
  -webkit-appearance: none;
  } 
   
- The benefit of using a <button> instead, is that you get all of the other interactive events for free, such as keyboard events, but also, some assistive technology allows users to loop through all of the buttons on the page 
   
- Remember: if your user is supposed to go somewhere, use an <a> element. If something with JavaScript needs to happen, use a <button> element. 
   
