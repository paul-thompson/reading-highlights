# Function Expressions vs. Function Declarations Revisisted

**Author:** gomakethings.com  
**Full title:** Function Expressions vs. Function Declarations Revisisted  
**URL:** https://gomakethings.com/function-expressions-vs.-function-declarations-revisisted/  
**Source:** #articles #instapaper #readwise

- historically been two ways to write a function. 
   
- // Function declaration
  function add (num1, num2) {
  return num1 + num2;
  } 
   
- // Function expression
  let add = function (num1, num2) {
  return num1 + num2;
  }; 
   
- There’s now a third way: ES6 arrow functions. 
   
- Hoisting 
   
- function declarations are hoisted to the top of the code by the browser before any code is executed. 
   
- all of the functions written with function declarations are “known” before any code is run. 
   
- This allows you to call a function before you declare it. 
   
- Function expressions, however, do not hoist 
   
- Which one should you use? 
   
- Function declarations are more common, and I like to adhere a bit more to conventions. 
   
- it’s more clear that the thing that’s coming is a function because function is the first word you see 
   
