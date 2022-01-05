# How to Work With the DOM Tree and Nodes   DigitalOcean

**Author:** digitalocean.com  
**Full title:** How to Work With the DOM Tree and Nodes | DigitalOcean  
**URL:** https://www.digitalocean.com/community/tutorials/understanding-the-dom-tree-and-nodes  
**Source:** #articles #instapaper #readwise

- The DOM is often referred to as the DOM tree, and consists of a tree of objects called nodes. 
   
- Understanding HTML and JavaScript terminology is essential to understanding how to work with the DOM. 
   
- The DOM Tree and Nodes 
   
- All items in the DOM are defined as nodes. 
   
- Element nodes
  Text nodes
  Comment nodes 
   
- When an HTML element is an item in the DOM, it is referred to as an element node. Any lone text outside of an element is a text node, and an HTML comment is a comment node. In addition to these three node types, the document itself is a document node, which is the root of all other nodes. 
   
- The DOM consists of a tree structure of nested nodes, which is often referred to as the DOM tree 
   
- Note: When working with an HTML-generated DOM, the indentation of the HTML source code will create many empty text nodes, which won’t be visible from the DevTools Elements tab. Read about Whitespace in the DOM 
   
- Every node in a document has a node type, which is accessed through the nodeType property. 
   
