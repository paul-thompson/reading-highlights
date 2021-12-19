# Thinking in React – React

**Author:** reactjs.org  
**Full title:** Thinking in React – React  
**URL:** https://reactjs.org/docs/thinking-in-react.html  
**Source:** #articles #instapaper #readwise

- Start With A Mock 
   
- Step 1: Break The UI Into A Component Hierarchy 
   
- draw boxes around every component (and subcomponent) in the mock and give them all names 
   
- Use the same techniques for deciding if you should create a new function or object. One such technique is the single responsibility principle, that is, a component should ideally only do one thing 
   
- If it ends up growing, it should be decomposed into smaller subcomponents. 
   
- UI and data models tend to adhere to the same information architecture. 
   
- Separate your UI into components, where each component matches one piece of your data model. 
   
- FilterableProductTable (orange): contains the entirety of the example 
   
- SearchBar (blue): receives all user input 
   
- ProductTable (green): displays and filters the data collection based on user input 
   
- ProductCategoryRow (turquoise): displays a heading for each category 
   
- ProductRow (red): displays a row for each product 
   
- you’ll see that the table header (containing the “Name” and “Price” labels) isn’t its own component. This is a matter of preference, and there’s an argument to be made either way. 
   
- if this header grows to be complex (e.g., if we were to add affordances for sorting), it would certainly make sense to make this its own ProductTableHeader component. 
   
- Components that appear within another component in the mock should appear as a child in the hierarchy 
   
- FilterableProductTable
  SearchBar
  ProductTable
  ProductCategoryRow
  ProductRow 
   
- Step 2: Build A Static Version in React 
   
- To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props 
   
- props are a way of passing data from parent to child. 
   
- State is reserved only for interactivity, that is, data that changes over time 
   
