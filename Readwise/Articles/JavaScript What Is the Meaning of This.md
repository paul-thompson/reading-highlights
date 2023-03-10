# JavaScript- What Is the Meaning of This

**Author:** const  
**Full title:** JavaScript: What Is the Meaning of This?  
**URL:** https://web.dev/javascript-this/  
**Source:** #articles #instapaper #readwise

- If the function is defined as an arrow function 
   
- const arrowFunction = () => {
  console.log(this);
  }; 
   
- In this case, the value of this is always the same as this in the parent scope 
   
- const outerThis = this;
  const arrowFunction = () => {
  console.log(this === outerThis);
  }; 
   
- Arrow functions are great because the inner value of this can't be changed, it's always the same as the outer this 
   
- With arrow functions, the value of this can't be changed 
   
- 'Bound' instance methods 
   
- if you want to ensure this always refers to the class instance, the best way is to use arrow functions and class fields 
   
- class Whatever {
  someMethod = () => {
  console.log(this);
  };
  } 
   
- it starts to make sense if you think of class fields as syntactic sugar for setting things in the constructor:
  class Whatever {
  someMethod = (() => {
  const outerThis = this;
  return () => {
  console.log(this === outerThis);
  };
  })();
  } 
   
- class Whatever {
  constructor() {
  const outerThis = this;
  this.someMethod = () => {
  console.log(this === outerThis);
  };
  }
  } 
   
- Alternative pattens involve binding an existing function in the constructor, or assigning the function in the constructor. If you can't use class fields for some reason, assigning functions in the constructor is a reasonable alternative 
   
- class Whatever {
  constructor() {
  this.someMethod = () => {
  };
  }
  } 
   
