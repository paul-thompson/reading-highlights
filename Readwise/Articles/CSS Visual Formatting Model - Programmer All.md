# CSS Visual Formatting Model - Programmer All

**Author:** programmerall.com  
**Full title:** CSS Visual Formatting Model - Programmer All  
**URL:** https://programmerall.com/article/4150414771/  
**Source:** #articles #instapaper #readwise

- The visual formatting model generates 0, 1 or more boxes for each element of the document according to the CSS box model 
   
- Box types: block-level box, inline-level box, inline-box, atomic inline-level box 
   
- A box is rendered relative to the boundary of its containing block. Usually a box creates a containing block for its descendant elements 
   
- When its layout goes outside the containing block, it is called overflow. 
   
- The definition of a containing block is different from the concept of a block container box. 
   
- Box generation 
   
- generate boxes from document elements. 
   
- The type of generated box depends on the CSS property display 
   
- Block-level-box:Block-level boxes participate in the block formatting context. 
   
- Each block-level element generates at least one block-level box, which is called a principal block-level box. 
   
- Some elements, such as <li>, generate additional boxes to place bullets, but most elements only generate a main block-level box. 
   
- Block-container box:Except for the table box and replaceable elements, the block-level boxes are all block container boxes 
   
- The block container box either contains only block-level boxes (except table boxes and replaceable elements), or generates an inline formatting context (inline formatting context, which contains only inline boxes, such as inline-block). 
   
- Block boxes:A box that is both a block-level box and a block container box is a block box. 
   
- element:Elements are the basis of the document structure. In CSS, each element generates a box containing content. 
   
- Replacement elements usually have inherent dimensions: an inherent width, an inherent height, and an inherent ratio 
   
- Some CSS properties such as vertical-align may use the intrinsic size or baseline of the replacement element 
   
