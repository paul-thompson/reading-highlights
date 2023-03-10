# Constructing the Object Model   Web Fundamentals   Google Developers

**Author:** developers.google.com  
**Full title:** Constructing the Object Model | Web Fundamentals | Google Developers  
**URL:** https://developers.google.com/web/fundamentals/performance/critical-rendering-path/constructing-the-object-model  
**Source:** #articles #instapaper #readwise

- Before the browser can render the page, it needs to construct the DOM and CSSOM trees 
   
- Bytes → characters → tokens → nodes → object model. 
   
- HTML markup is transformed into a Document Object Model (DOM); 
   
- DOM and CSSOM are independent data structures. 
   
- The final output of this entire process is the Document Object Model (DOM) of our simple page, which the browser uses for all further processing of the page 
   
- Every time the browser processes HTML markup, it goes through all of the steps above: convert bytes to characters, identify tokens, convert tokens to nodes, and build the DOM tree. 
   
- The DOM tree captures the properties and relationships of the document markup, but it doesn't tell us how the element will look when rendered. That’s the responsibility of the CSSOM. 
   
- As with HTML, we need to convert the received CSS rules into something that the browser can understand and work with. Hence, we repeat the HTML process, but for CSS instead of HTML: 
   
