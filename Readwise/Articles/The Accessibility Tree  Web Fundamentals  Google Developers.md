# The Accessibility Tree   Web Fundamentals   Google Developers

**Author:** Text alternatives  
**Full title:** The Accessibility Tree | Web Fundamentals | Google Developers  
**URL:** https://developers.google.com/web/fundamentals/accessibility/semantics-builtin/the-accessibility-tree  
**Source:** #articles #instapaper #readwise

- Imagine that you're building a user interface for screen reader users only. Here, you don't need to create any visual UI at all, but just provide enough information for the screen reader to use. 
   
- you'd be creating is a kind of API describing the page structure, similar to the DOM API, but you can get away with less information and fewer nodes, because a lot of that information is only useful for visual presentation. 
   
- The browser takes the DOM tree and modifies it into a form that is useful to assistive technology. We refer to this modified tree as the Accessibility Tree. 
   
- The accessibility tree is what most assistive technologies interact with. 
   
- For web browsers, there's an extra step in each direction, because the browser is in fact a platform for web apps that run inside it 
   
- the browser needs to translate the web app into an accessibility tree, and must make sure that the appropriate events get fired in JavaScript based on the user actions that come in from the assistive technology. 
   
- We do this by ensuring that we express the semantics of our pages correctly: making sure that the important elements in the page have the correct accessible roles, states, and properties, and that we specify accessible names and descriptions. 
   
- Semantics in native HTML 
   
- A browser can transform the DOM tree into an accessibility tree because much of the DOM has implicit semantic meaning 
   
- the DOM uses native HTML elements that are recognized by browsers and work predictably on a variety of platforms 
   
- Accessibility for native HTML elements such as links or buttons is thus handled automatically. 
   
- When we don't use an actual button element, the screen reader has no way to know what it has landed on 
   
- Using a native element also has the benefit of taking care of keyboard interactions for us. And remember that you don't have to lose your spiffy visual effects just because you use a native element; you can style native elements to make them look the way you want and still retain the implicit semantics and behavior. 
   
- Broadly, there are two types of names 
   
- Visible labels, which are used by all users to associate meaning with an element, and 
   
- Text alternatives, which are only used when there is no need for a visual label 
   
- providing text alternatives for any non-text content is the very first item on the WebAIM checklist. 
   
