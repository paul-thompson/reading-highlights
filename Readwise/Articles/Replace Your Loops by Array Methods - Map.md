# Replace Your Loops by Array Methods - Map

**Author:** Fernando Daciuk  
**Full title:** Replace Your Loops by Array Methods - Map  
**URL:** https://medium.com/daily-js-tips/replace-your-loops-by-array-methods-map-4e9af2e18427  
**Source:** #articles #instapaper #readwise

- The `map()` method works like `forEach()` 
   
- this method iterates by an array, and receives two parameters: a callback function, and a second parameter, that represents the `this`, inside callback function. The second parameter is optional, and you’ll rarely need it. 
   
- The big difference between this two methods is that the `map()` method returns a new array, while `forEach()` doesn’t returns anything. 
   
- The `map()` method is much more clear than for loop 
   
- var productsIds = products.map(product => product.id); 
   
