# What Does the HTML Image Decoding Async Attribute Do and How Can It Help Us to Improve Performance

**Author:** js-craft.io  
**Full title:** What Does the HTML Image Decoding Async Attribute Do and How Can It Help Us to Improve Performance  
**URL:** http://www.js-craft.io/blog/what-does-the-html-image-decoding-async-attribute-do-and-how-can-it-help-us-to-improve-performance/  
**Source:** #articles #instapaper #readwise

- By default, browsers are loading text and images at the same time. 
   
- This looks nice as it provides the user with the full experience when that loading is done. 
   
- The decoding="async" attribute will tell the browser that it is OK for image decoding to be done at a later moment so that the browser can continue displaying content even if the images are not fully loaded 
   
- There are 3 accepted values for the decoding attribute 
   
- sync: the rendering will continue only after the image is ready; preferred for a "complete experience" 
   
- async: continue the rendering and as soon as image decoding is complete, the browser will update the presentation; preferred
  for performance 
   
- auto: will let the browser do what it determines is best approach (not sure who it decides that 
   
