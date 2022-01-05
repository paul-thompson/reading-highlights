# The Arrow Function in JS!

**Author:** dev.to  
**Full title:** The Arrow Function in JS!  
**URL:** https://dev.to/ziratsu/the-arrow-function-in-js-528f  
**Source:** #articles #instapaper #readwise

- The arrow function exists since 2015 and is quite different from the classic functions 
   
- const add = (a,b) => {
  return a + b;
  } 
   
- const add = (a,b) => a + b; 
   
- If you have one parameter (but only one), you can remove the parenthesis 
   
- const add = a => a; 
   
- useful when you use it with some higher order function like the map.() 
   
- The difference between a classic function and an arrow function. 
   
- The main difference between the classic and arrow function is the value of "this". 
   
- If you use a classic function as the value of a property in an object, "this" will refer to the calling context 
   
- if you use an arrow function, "this" will return the global object 
   
- Instead of refering the direct context, it will refer to the parent of that context. 
   
