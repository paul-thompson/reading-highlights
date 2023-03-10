# What Is the DOM

**Author:** egghead.io  
**Full title:** What Is the DOM?  
**URL:** https://egghead.io/learn/javascript/the-dom  
**Source:** #articles #instapaper #readwise

- The DOM is an acronym for “Document Object Model.” 
   
- The DOM shows relationships between elements, referred to as parents, children, and siblings. 
   
- The DOM is a type of API (Application Programming Interface) 
   
- The DOM is not the source HTML, or the code you write. As a matter of fact, the DOM is not a programming language at all. 
   
- The DOM is not what you see in the browser or in your browser’s DevTools 
   
- The DOM, or Document Object Model, is an API that helps developers interact with “document nodes” within the browser 
   
- The DOM tree shows relationships between different “nodes” (or elements) within a web page, and your web browsers use the DOM Tree to determine how to display these web pages. 
   
- The DOM Node Tre 
   
- The visual representation of the DOM looks like a “tree” of “nodes.” However, you won’t ever see the “tree” in actuality 
   
- Types of HTML Nodes 
   
- The DOM Tree is a tree structure representing different elements of an HTML page, and each HTML element is a “node. 
   
- There are 12 different node types in the DOM 
   
- Element
  Text
  Attr
  CDATASection
  EntityReference
  Entity
  Comment
  ProcessingInstruction
  Document
  Notation
  DocumentFragment
  DocumentType 
   
- Some node types can have “children,” which can be other types of nodes. 
   
- The DOM Tree is not the source code 
   
- The DOM is not the code you write, because the DOM is the result of your code; 
   
- when the HTML has invalid code, the DOM may fix the invalid HTML before showing it. In that case, when the visitor opens Developer Tools on their browser to inspect the code, they will see corrected HTML code instead of what the code’s author wrote. 
   
- Another instance when HTML may not match what shows up in the DOM is when the HTML is modified by JavaScript 
   
- JavaScript can only affect elements that exist in the DOM 
   
- what shows up in the Developer Tools may also not always be the DOM 
   
- if the code uses CSS pseudo-elements, the DOM does not include it in its tree, because the DOM builds itself from the source HTML document, not the styles applied to the elements 
   
- JavaScript can… 
   
- Change, add, or remove HTML elements and attributes
  Change CSS styles
  Create and react to HTML events like clicks or hovers 
   
