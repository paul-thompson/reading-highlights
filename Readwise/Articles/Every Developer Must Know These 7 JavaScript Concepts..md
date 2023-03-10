# Every Developer Must Know These 7 JavaScript Concepts.

**Author:** 3. Hoisting  
**Full title:** Every Developer Must Know These 7 JavaScript Concepts.  
**URL:** https://dev.to/nathannosudo/every-developer-must-know-these-7-javascript-concepts-3ecp  
**Source:** #articles #instapaper #readwise

- 1. Scope 
   
- Scope means variable access. What variable do I have access to when a code is running? 
   
- Local Scope allows access to everything within the boundaries (inside the box) 
   
- Global Scope is everything outside the boundaries (outside the box). 
   
- A global scope can not access a variable defined in local scope because it is enclosed from the outer world, except if you return it. 
   
- 2. IIFE (Immediately Invoked Function Expression) 
   
- the primary reason to use IIFE is to immediately execute the code and obtain data privacy 
   
- 3. Hoisting 
   
- In Javascript, you can call a function before it is defined and you won’t get an error ‘Uncaught ReferenceError’ 
   
- 4. Closure 
   
- A closure is simply a function inside another function that has access to the outer function variable 
   
- The inner function (closure) can access the variable defined in its scope (variables defined between its curly brackets), in the scope of its parent function, and the global variables 
   
- Closures can be defined in simple terms as “a function run, the function executed. It’s never going to execute again but it’s going to remember that there are references to those variables so the child scope always has access to the parent scope.” 
   
- 5. Callbacks 
   
- a callback is simply a function that is passed to another function as a parameter and is invoked or executed inside the other function 
   
- (when X is completed, then Y is executed, and it goes on.). This is the reason callback is generally used in the asynchronous operation of javascript to provide the synchronous capability. 
   
- 6. Promises 
   
- this recursive structure of callback is called ‘callback hell’ and promises to help to solve this kind of issue. Promises are useful in asynchronous javascript operations when we need to execute two or more back-to-back operations (or chaining callback) 
   
- A Promise is an object representing the eventual completion or failure of an asynchronous operation. 
   
- A promise may be in three possible states…
  Fulfilled: When the operation is completed successfully.
  Rejected: When the operation is failed.
  Pending: initial state, neither fulfilled nor rejected. 
   
- 7. Async & Await 
   
- Async & await just syntactic sugar on top of Promises and like promises it also provides a way to maintain asynchronous operation more synchronously 
   
- ES5 -> Callback
  ES6 -> Promise
  ES7 -> async & await 
   
