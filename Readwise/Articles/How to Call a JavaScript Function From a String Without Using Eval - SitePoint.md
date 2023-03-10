# How to Call a JavaScript Function From a String Without Using Eval - SitePoint

**Author:** Craig Buckler  
**Full title:** How to Call a JavaScript Function From a String Without Using Eval - SitePoint  
**URL:** https://www.sitepoint.com/call-javascript-function-string-without-using-eval/  
**Source:** #articles #instapaper #readwise

- eval is evil in JavaScript! The MDN eval page states 
   
- eval executes a string containing code 
   
- eval raises several issues 
   
- Security: your string can be injected with other commands by third-party scripts or user input. 
   
- Debugging: it’s difficult to debug errors — you have no line numbers or obvious points of failure. 
   
- Optimization: the JavaScript interpreter cannot necessarily pre-compile the code because it could change 
   
- In the past it was primarily used for de-serializing JSON strings but we now have the safer JSON.parse method. 
   
- use the window object which references the current window and all items within it. We can check whether fnstring is available as an object within window and run it if it’s a function 
   
- var fnstring = "runMe";
  var fn = window[fnstring];
  if (typeof fn === "function") fn(); 
   
- if the function we want to call has parameters — perhaps stored in an array? No problem; we simply use the apply method 
   
- var fnstring = "runMe";
  var fnparams = [1, 2, 3];
  var fn = window[fnstring];
  if (typeof fn === "function") fn.apply(null, fnparams); 
   
