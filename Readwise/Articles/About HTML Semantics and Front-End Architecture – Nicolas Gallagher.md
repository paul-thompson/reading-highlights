# About HTML Semantics and Front-End Architecture – Nicolas Gallagher

**Author:** nicolasgallagher.com  
**Full title:** About HTML Semantics and Front-End Architecture – Nicolas Gallagher  
**URL:** http://nicolasgallagher.com/about-html-semantics-front-end-architecture/  
**Source:** #articles #instapaper #readwise

- The principle of writing “semantic HTML” is one of the foundations of modern, professional front-end development. 
   
- not all semantics need to be content-derived. Class names cannot be “unsemantic”. Whatever names are being used: they have meaning, they have purpose. 
   
- We can leverage the agreed “global” semantics of HTML elements, certain HTML attributes, Microdata, etc., without confusing their purpose with those of the “local” website/application-specific semantics that are usually contained in the values of attributes like the class attribute. 
   
- Content-layer semantics are already served by HTML elements and other attributes 
   
- Class names impart little or no useful semantic information to machines or human visitors unless it is part of a small set of agreed upon (and machine readable) names – Microformats. 
   
- The primary purpose of a class name is to be a hook for CSS and JavaScript. 
   
- Class names should communicate useful information to developers. It’s helpful to understand what a specific class name is going to do when you read a DOM snippet 
   
- The most reusable components are those with class names that are independent of the content. 
   
- Front-end architecture 
   
- The aim of a component/template/object-oriented architecture is to be able to develop a limited number of reusable components that can contain a range of different content types. 
   
- Scalable HTML/CSS must, by and large, rely on classes within the HTML to allow for the creation of reusable components. A flexible and reusable component is one which neither relies on existing within a certain part of the DOM tree, nor requires the use of specific element types. 
   
- An approach that improves the ease with which you can combine other components with uilist is to use classes to style the child DOM elements. Although this helps to reduce the specificity of the rule, the main benefit is that it gives you the option to apply the structural styles to any type of child node. 
   
- JavaScript-specific classes 
   
- An approach that I’ve found helpful is to use certain classes only for JavaScript hooks – js-* – and not to hang any presentation off them. 
   
- <a href="/login" class="btn btn-primary js-login"></a> 
   
- Components often have variants with slightly different presentations from the base component, e.g., a different coloured background or border. There are two mains patterns used to create these component variants. 
   
- “single-class” and “multi-class” patterns 
   
- The “single-class” pattern 
   
- .btn, .btn-primary { /* button template styles */ }
  .btn-primary { /* styles specific to save button */ }
  <button class="btn">Default</button>
  <button class="btn-primary">Login</button> 
   
- The “multi-class” pattern 
   
- .btn { /* button template styles */ }
  .btn-primary { /* styles specific to primary button */ }
  <button class="btn">Default</button>
  <button class="btn btn-primary">Login</button> 
   
- A “multi-class” pattern means you only need a single intra-component selector to target any type of btn-styled element within the component 
   
