# Replaced Elements - CSS- Cascading Style Sheets   MDN

**Author:** developer.mozilla.org  
**Full title:** Replaced Elements - CSS: Cascading Style Sheets | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element  
**Source:** #articles #instapaper #readwise

- In CSS, a replaced element is an element whose representation is outside the scope of CSS 
   
- Some replaced elements, such as <iframe> elements, may have stylesheets of their own, but they don't inherit the styles of the parent document. 
   
- Typical replaced elements are:
  <iframe>
  <video>
  <embed>
  <img> 
   
- Some elements are treated as replaced elements only in specific cases:
  <option>
  <audio>
  <canvas>
  <object>
  <applet> 
   
- Objects inserted using the CSS content property are anonymous replaced elements. They are "anonymous" because they don't exist in the HTML markup 
   
- some replaced elements, but not all, have intrinsic dimensions or a defined baseline, which is used by some CSS properties, such as vertical-align. Only replaced elements can ever have intrinsic dimensions. 
   
- Certain CSS properties can be used to specify how the object contained within the replaced element should be positioned within the element's box area 
   
- object-fit
  Specifies how the replaced element's content object should be fitted to the containing element's box. 
   
- object-position
  Specifies the alignment of the replaced element's content object within the element's box. 
   
