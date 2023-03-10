# What Every JavaScript Developer Should Know About ECMAScript 2015

**Author:** K. Scott Allen  
**Full title:** What Every JavaScript Developer Should Know About ECMAScript 2015  
**Source:** #books #kindle #readwise

- JavaScript only offers function scope and global scope to control the lifetime of a variable. There is no block scope1. 
   
- The new let keyword of 2017 will replace var for variable declarations and provide true block scoping. 
   
- ES2017 still supports the var keyword, but we should think of var as an obsolete keyword when writing new code. let is the new var! 
   
- The const keyword will give you a read-only variable. Like let, a variable declared with const will have block scope, and you can not redeclare a const. 
   
- The official specification says const should fail with a runtime error if a program tries to assign a new value to a constant, and constant declarations without an initializer should be a syntax error. 
   
- const tells other programmers about the intended behavior of a variable, 
   
- Before 2015, developers applied default values to incoming parameters using || expressions inside the function. 
   
- In 2017, default values are explicit and appear in the parameter list for a function. 
   
- A rest parameter allows a function to work with a variable number of arguments. 
   
- A function’s rest parameter always appears at the end of the argument list and uses a triple dot prefix (…), 
   
- arguments is not an array, which creates confusion. 
   
- Rest parameters will avoid confusion by always giving us a true array, and by using a dedicated syntax, that makes rest parameters easy to spot when reading the function signature. 
   
- Spread Operator 
   
- The spread operator shares the same syntax we saw with rest parameters, a series of three dots (...). 
   
