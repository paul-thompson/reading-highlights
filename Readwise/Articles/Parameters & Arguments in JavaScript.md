# Parameters & Arguments in JavaScript

**Author:** Yash Agrawal  
**Full title:** Parameters & Arguments in JavaScript  
**URL:** https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04  
**Source:** #articles #instapaper #readwise

- Javascript is a functional language meaning that functions are the primary modular units of execution. 
   
- the terms parameters and arguments are often interchangeably used as if it were one and the same thing but there is a very subtle difference. 
   
- Parameters are variables listed as a part of the function definition. 
   
- Arguments are values passed to the function when it is invoked. 
   
- JavaScript does not throw an error if the number of arguments passed during a function invocation are different than the number of parameters listed during function definition. 
   
- Basically, when excess arguments are provided, they don’t get assigned to any parameters 
   
- if we have more parameters than the arguments, the parameters that have no corresponding arguments are set to undefined 
   
- The arguments parameter 
   
- The arguments parameter is implicitly passed just like the this parameter. It is a local variable accessible within all functions and contains an entry for each argument passed to that function 
   
- The arguments object is an array-like construct which can be used to access arguments passed to the function even if a matching parameter isn’t explicitly defined. 
   
