# Exploring JavaScript Array Methods

**Author:** Todd Motto  
**Full title:** Exploring JavaScript Array Methods  
**Source:** #books #api_book #readwise

- Array ForEach is a method that exists on the Array.prototype that was introduced in ECMAScript 5 (ES5) and is supported in all modern browsers. 
   
- ForEach, unlike other array methods, does not return any value. 
   
- Think of Array ForEach as: “I want to access my array values one-by-one so I can do something with them” 
   
- array.forEach((value, index, array) => {...}, thisArg); 
   
- ForEach is also considered a “modern for…in loop” replacement, despite behaving differently and having less flexibility. 
   
- Array ForEach syntax deconstructed 
   
- ForEach’s first argument is a callback function 
   
- value (the current element) 
   
- index (the element’s index - fairly commonly used) 
   
- array (the array we are looping - rarely used) 
   
- Inside the body of the function we would access value and do something with us, sum values, inject template into the DOM, anything you like 
   
- second argument thisArg allows the this context to be changed 
   
- 1 ['a', 'b', 'c', 'd'].forEach(function(item, index) {
  2 console.log(item, index);
  3 }); 
   
- Further tips and tricks 
   
- ForEach is great for simple looping as it doesn’t return any values 
   
- You cannot break or continue items inside a ForEach 
   
- You cannot ForEach in reverse, use for...in or for...of 
   
- You can access the array you’re looping in the third argument of the callback 
   
- You can change the this context via a second argument to .forEach(callback, thisArg)
  so that any references to this inside your callback point to your object 
   
- You can use arrow functions with ForEach but remember that this will be incorrect if you also supply a thisArg due to arrow functions not having a this context 
   
- Using ForEach will skip empty array slots 
   
