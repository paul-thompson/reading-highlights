# Css Visual Formatting Model - CodeProject Reference

**Author:** reference.codeproject.com  
**Full title:** Css Visual Formatting Model - CodeProject Reference  
**URL:** https://reference.codeproject.com/css/visual_formatting_model  
**Source:** #articles #instapaper #readwise

- The CSS visual formatting model is an algorithm that processes a document and displays it on visual media. 
   
- The type of box: inline, inline-level, atomic inline-level, block 
   
- The model renders a box in relation to the edge of its containing block 
   
- Usually, a box establishes the containing block for its descendants. However, a box is not constrained by its containing block; when a box's layout goes outside the containing block, it is said to overflow. 
   
- Box generation 
   
- Box generation is the part of the CSS visual formatting model that creates boxes from the document's elements 
   
- display CSS property is: block, list-item or table. A block-level element is visually formatted as a block (e.g., paragraph), intended to be vertically stacked. 
   
- Each block-level box participates in a block formatting context. Each block-level element generates at least one block-level box, called the principal block-level box. 
   
- Some elements, like a list-item element generating further boxes to handle bullets and other typographic elements introducing the list item, may generate more boxes, but most generate only the principal block-level box 
   
- The principal block-level box contains descendant-generated boxes and generated content. It is also the box involved in the positioning scheme 
   
- A block-level box may also be a block container box. A block container box is a box that contains only other block-level boxes, or creates an inline formatting context, and thus contains only inline boxes. 
   
- It is important to note that the notions of a block-level box and block container box are disjoined. The first describes how the box behaves with its parents and sibling, the second how it interacts with its descendants 
   
- Block-level boxes that also are block container boxes are called block boxes 
   
- Anonymous block boxes 
   
