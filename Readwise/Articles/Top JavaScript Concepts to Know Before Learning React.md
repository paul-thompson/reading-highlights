# Top JavaScript Concepts to Know Before Learning React

**Author:** TAPAS ADHIKARY  
**Full title:** Top JavaScript Concepts to Know Before Learning React  
**URL:** https://www.freecodecamp.org/news/top-javascript-concepts-to-know-before-learning-react/  
**Source:** #articles #instapaper #readwise

- Many developers choose a "learn as you go" approach when learning React. But this often doesn't result in productivity, and instead worsens the gaps in their JavaScript knowledge 
   
- you might begin to confuse JavaScript with React 
   
- React is a JavaScript framework for building UI components-based user interfaces. 
   
- React is built using modern JavaScript features, which were mostly introduced with ES2015. 
   
- The JavaScript You Need to Know Before Learning React 
   
- Callback Functions in JavaScript 
   
- Callbacks are critical to understand since they are used in array methods (such as map(), filter(), and so on), setTimeout(), event listeners (such as click, scroll, and so on), and many other places. 
   
- A callback function can be either an ordinary function or an arrow function. 
   
- Promises in JavaScript 
   
- consider stacking so many callback functions on top of each other because you do not want a specific function to run until the parent function has finished running or a specific time has passed 
   
- Callback hell is a big issue caused by coding with complex nested callbacks. 
   
- The primary reason for using promises is to prevent callback hell. With Promises, we may write asynchronous code in a synchronous manner. 
   
- A promise is an object that returns a value that you anticipate to see in the future but do not now see. 
   
- A practical use for promises would be in HTTP requests, where you submit a request and do not receive a response right away because it's an asynchronous activity. You only receive the answer (data or error) when the server responds. 
   
- const myPromise = new Promise((resolve, reject) => { 
  // condition
  }); 
   
- Promises have two parameters, one for success (resolve) and one for failure (reject). 
   
- There are 3 states of the Promise object 
   
- Pending: by default, this is the Initial State, before the Promise succeeds or fails.
  Resolved: Completed Promise
  Rejected: Failed Promise 
   
- function addName (time, name){
  return new Promise ((resolve, reject) => {
  if(name){
  setTimeout(()=>{
  console.log(name)
  resolve();
  },time)
  }else{
  reject('No such name');
  }
  })
  }
  addName(2000, 'Joel')
  .then(()=>addName(2000, 'Victoria'))
  .then(()=>addName(2000, 'John'))
  .then(()=>addName(2000, 'Doe'))
  .then(()=>addName(2000, 'Sarah'))
  .catch((err)=>console.log(err)) 
   
- Map() in JavaScript 
   
- One of the most often used methods is Array.map(), which allows you to iterate over an array and modify its elements using a callback function. The callback function will be run on each array element. 
   
- map() always returns a new array, even if it’s an empty array 
   
- It doesn’t change the size of the original array compared to the filter method 
   
- It always makes use of the values from your original array when making a new one. 
   
- Gotcha: The map method works almost like every other JavaScript iterator such as forEach() but it’s proper to always use the map method whenever you are going to return a value. 
   
- Filter() and Find() in JavaScript 
   
- Filter() provides a new array depending on certain criteria. 
   
- Unlike map(), it can alter the size of the new array, whereas find() returns just a single instance (this might be an object or item). If several matches exist, it returns the first match – otherwise, it returns undefined. 
   
- This generates a new array. It produces an empty array if the condition is not satisfied(no match). 
   
- Find() 
   
- The find() method, like the filter() method, iterates across the array looking for an instance/item that meets the specified condition. Once it finds it, it returns that specific array item and immediately terminates the loop. If no match is discovered, the function returns undefined. 
   
- Destructuring Arrays and Objects in JavaScript 
   
- Destructuring is a JavaScript feature introduced in ES6 that allows for faster and simpler access to and unpacking of variables from arrays and objects. 
   
- Object destructuring 
   
- Let’s now see how we could destructure an object – because in React you will be doing a lot of object descructuring 
   
- Rest and Spread Operators in JavaScript 
   
- JavaScript spread and rest operators use three dots .... The rest operator gathers or collects items – it puts the “rest” of some specific user-supplied values into a JavaScript array/object. 
   
- destructure to get the first and second fruits and then place the“rest” of the fruits in an array by making use of the rest operator. 
   
- const [firstFruit, secondFruit, ...rest] = fruits
  console.log(firstFruit, secondFruit, rest); //"Mango" "Pineapple" ["Orange","Lemon","Apple"] 
   
