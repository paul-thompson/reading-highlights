# The Philosophy of React- Declarative Rendering - Fjorge

**Author:** .classList.add()  
**Full title:** The Philosophy of React: Declarative Rendering - Fjorge  
**URL:** https://fjorgedigital.com/insights/blog/the-philosophy-of-react-declarative-rendering/  
**Source:** #articles #instapaper #readwise

- A core concept behind React is the idea of declarative rendering vs. imperative rendering. 
   
- Vanilla JS and libraries like jQuery are imperative 
   
- you directly command the element to change its class by calling a function like .classList.add() or .addClass() 
   
- React is declarative. When you want to change the class attribute of a DOM element, you do not directly send a command to the element. 
   
- The element will react to its component’s new state and props. 
   
- The advantage of declarative rendering over imperative rendering becomes clear when you have many different elements whose attributes depend on several different pieces of data 
   
- Those functions must also take into account the other functions that also affect it. The logic controlling a particular element’s attributes is fragmented and distributed, making it very difficult to track down bugs. 
   
- With declarative DOM manipulation, a single element would have all its attributes defined in a single spot within your render() function 
   
- In imperative rendering, many different functions push information down to an element. In declarative rendering, an element pulls information down from only state and props 
   
