# In-Depth Understanding of the Box Model-Css Visual Formatting Model   Box Model   Positioning Solution   BFC - Titan Wolf

**Author:** blog.titanwolf.in  
**Full title:** In-Depth Understanding of the Box Model-Css Visual Formatting Model | Box Model | Positioning Solution | BFC - Titan Wolf  
**URL:** https://blog.titanwolf.in/a?ID=00550-2c41aa9b-49ab-496b-805f-4442c3a46c88  
**Source:** #articles #instapaper #readwise

- The page (document tree) can be imagined as a combination of boxes 
   
- (Visual formatting model) is a set of rules that lay out these boxes as visitors see 
   
- Element box 
   
- CSS assumes that each element will generate one or more boxes, called element boxes. 
   
- element box has a content area, and the surrounding area includes padding, border, and margin 
   
- Containing block 
   
- Each element is placed relative to the containing block, which is the "layout context" of an element, 
   
- <img>, <input>, <textarea>, <select>, and <object> in HTML are all replacement elements. 
   
- Replaceable elements also generate boxes in their display. 
   
- There are roughly two common box models, one is a block box, and the other It is a line-level box (Line Box) 
   
- Block Box 
   
- display : block , list-item, and table make an element a block-level element 
   
- Line Box 
   
- Each line is called a Line Box, which is composed of many inline-boxes in this line 
   
- display : inline will make an element called an inline element 
   
- inline-block 
   
- The object is presented as an inline object, but the content of the object is presented as a block object. Subsequent inline objects will be arranged in the same row 
   
- Formatting context 
   
