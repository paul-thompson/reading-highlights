# No One Told Me Scope and Scope Chain in JavaScript Is This Easy to Understand

**Author:** Divyojyoti Ghosh  
**Full title:** No One Told Me Scope and Scope Chain in JavaScript Is This Easy to Understand  
**URL:** https://javascript.plainenglish.io/scope-and-scope-chain-in-javascript-a92dbdb1452f  
**Source:** #articles #reader #readwise

- In computer programming scoping deals with the variables’ **organisation**(where does the variable live? ) and their **accession** (where can the variable be accessed from? ). 
   
- JavaScript has **lexical scoping** which means the placement of blocks and functions in the code controls the scoping. 
   
- The **scope** is the space or environment in the code where a particular variable has been declared 
   
- the **scope of a variable** is the region in the code where a particular variable can be accessed 
   
- • Global Scope
  • Function Scope
  • Block Scope 
   
- Global Scope 
   
- The scope of variables declared outside any function or block is Global i.e. they can be accessed everywhere in the code. 
   
- Function Scope 
   
- All the variables declared within a function have a function scope i.e. they cannot be accessed anywhere outside the function 
   
- All variables defined in a function whether they are declared using **var**, **const** or **let** have function scope. 
   
- Block Scope 
   
- The variables if declared using let or const within curly braces { } (apart from function) have block scope, i.e. these variables cannot be accessed outside the block 
   
- In strict mode, functions declared with let or const within a block are also blocked scope, even the named functions (not declared using var, let or const) are also blocked scope in strict mode. 
   
- The Scope Chain 
   
- During execution, if the JS engine come across a variable, to access the variable and its value it first searches in the local scope, if it doesn’t find the variable in the local scope, it searches for the variable in its parent’s scope. 
   
- If a variable is not found in this whole scope chain, the JS engine throws a reference error and declares the variable not defined. 
   
