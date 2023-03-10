# Intro to React - JSX and Elements

**Author:** React Features  
**Full title:** Intro to React - JSX and Elements  
**URL:** https://dev.to/maxdemaio/intro-to-react-jsx-and-elements-3n8k  
**Source:** #articles #instapaper #readwise

- React is a modern JavaScript library for building interactive user interfaces 
   
- React Features 
   
- Components/JSX: components are the building blocks of React applications. 
   
- After compilation, JSX expressions become JavaScript function calls and evaluate to JavaScript objects. Components can be simple or stateful. 
   
- Virtual DOM: Instead of rebuilding the entire DOM tree for updates, React makes use of the virtual DOM. The virtual DOM is a lightweight copy of the actual DOM. React will update exactly which virtual DOM objects have changed through diffing 
   
- React has a waterfall like concept of transferring data to other parts of the application. State is passed to the view and child components. Actions are triggered by the view and can update state. 
   
- Getting Started 
   
- We can use create-react-app to bootstrap a React application 
   
- ReactDOM.render() renders an element or component to the virtual DOM. The first parameter specifies what needs to be rendered. The second argument specifies where to render. 
   
- Babel compiles JSX down to React.createElement() calls. 
   
- Unlike browser DOM elements, React elements are cheap to create because they’re plain JavaScript objects 
   
- Babel compiles JSX down to React.createElement() calls. Then, React.createElement() creates objects aka React elements 
   
- React elements are representations of what we’d want to see on the screen. Note, elements make up components. React reads these objects and uses them to make the DOM and update it. 
   
