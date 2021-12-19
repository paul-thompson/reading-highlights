# Finding-Fixing Unintended Body Overflow

**Author:** css-tricks.com  
**Full title:** Finding/Fixing Unintended Body Overflow  
**URL:** https://css-tricks.com/findingfixing-unintended-body-overflow/  
**Source:** #articles #instapaper #readwise

- var docWidth = document.documentElement.offsetWidth;
  [].forEach.call(
  document.querySelectorAll('*'),
  function(el) {
  if (el.offsetWidth > docWidth) {
  console.log(el);
  }
  }
  ); 
   
- It’s just more common and practical to use overflow-x. 
   
