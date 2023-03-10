# The Difference Between DOM and Virtual DOM

**Author:** What is DOM  
**Full title:** The Difference Between DOM and Virtual DOM  
**URL:** https://dev.to/codeslinger/the-difference-between-dom-and-virtual-dom-52o1  
**Source:** #articles #instapaper #readwise

- It takes HTML elements and wraps them in an object with a tree structure — maintaining the parent/child relationships of those nested HTML elements. 
   
- Any manipulation of certain elements inside it causes complete re-render. 
   
- complete renders of real DOM are very costly, causing applications to have slow performance. 
   
- DOM manipulation is the heart of the modern, interactive web. 
   
- Inefficient updating like repainting the whole page for each change is very very expensive 
   
- To Keep Real and Virtual DOM in sync a process called Reconciliation is used. Diffing algorithm is a technique of reconciliation that is used by React. 
   
- By comparing the new virtual DOM with a pre-update version, React figures out exactly which virtual DOM objects have changed. This process is called “diffing.”
  Once React knows which virtual DOM objects have changed, then React updates those objects, and only those objects, on the real DOM 
   
# The Difference Between DOM and Virtual DOM

**Author:** What is DOM  
**Full title:** The Difference Between DOM and Virtual DOM  
**URL:** https://dev.to/codeslinger/the-difference-between-dom-and-virtual-dom-52o1  
**Source:** #articles #instapaper #readwise

- It takes HTML elements and wraps them in an object with a tree structure — maintaining the parent/child relationships of those nested HTML elements. 
   
- Any manipulation of certain elements inside it causes complete re-render. 
   
- complete renders of real DOM are very costly, causing applications to have slow performance. 
   
- DOM manipulation is the heart of the modern, interactive web. 
   
- Inefficient updating like repainting the whole page for each change is very very expensive 
   
- To Keep Real and Virtual DOM in sync a process called Reconciliation is used. Diffing algorithm is a technique of reconciliation that is used by React. 
   
- By comparing the new virtual DOM with a pre-update version, React figures out exactly which virtual DOM objects have changed. This process is called “diffing.”
  Once React knows which virtual DOM objects have changed, then React updates those objects, and only those objects, on the real DOM 
   
