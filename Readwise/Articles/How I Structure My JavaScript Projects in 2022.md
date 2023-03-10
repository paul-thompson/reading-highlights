# How I Structure My JavaScript Projects in 2022

**Author:** event-listeners.js  
**Full title:** How I Structure My JavaScript Projects in 2022  
**URL:** https://gomakethings.com/how-i-structure-my-javascript-projects-in-2022/  
**Source:** #articles #instapaper #readwise

- The JavaScript patterns I use 
   
- For libraries, I typically use a Constructor pattern. 
   
- For simple scripts on personal projects, I typically use a small function as a wrapper. I generally want to explicitly invoke it rather than using an Immediately Invoked Function Expression (or IIFE). 
   
- I used to use revealing module patterns a lot more often, but these days, I tend to use ES modules instead 
   
- I’m a big fan of running NPM scripts directly. It gives me more control than CodeKit, but a much smaller set of dependencies (and less things breaking all the time) than Gulp. 
   
- Every single one of my projects now uses my Build Tool Boilerplate. 
   
- How I organize code within a file 
   
- Variables at the top of the page
  Functions and methods in the middle
  Initializations and event listeners at the end 
   
- // 
  // Variables
  // 
   
- //
  // Methods
  // 
   
- // 
  // Inits & Event Listeners
  // 
   
- I use JSDoc to document my code. Some text editors will use this to pull out information about functions when used in other places in your code 
   
- How I modularize and organize files 
   
- ES modules. They help me keep my code more structured and organized. 
   
- For JavaScript libraries, I organize my functions and files by what they do: event-listeners.js, dom.js, 
   
- For websites and apps, I tend to keep each library or discrete piece of functionality in its own file, and import them into files specific to the pages they’re needed on: search.js, table-of-contents.js, and so on 
   
- I keep all of my build files in a src directory, and compile them with rollup.js and my Build Tools Boilerplate into a dist directory. 
   
