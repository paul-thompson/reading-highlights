# When Does a Box Establish an Inline Formatting Context - Pretag

**Author:** pretagteam.com  
**Full title:** When Does a Box Establish an Inline Formatting Context? - Pretag  
**URL:** https://pretagteam.com/question/when-does-a-box-establish-an-inline-formatting-context  
**Source:** #articles #instapaper #readwise

- If the "block container box" contains text and block elements, then the text is treated as being contained in one or more anonymous block-level boxes, and a block-formatting context is established.,Acting as a "block container box 
   
- the block-element establishes a block-formatting context if the block-element has at least one child block-level element. 
   
- If all the child elements are inline-level boxes, then an inline-formatting context is established 
   
- an inline formatting context cannot be triggered explicitly 
   
- a block formatting context that can be triggered explicitly (for example, setting overflow: hidden to a block-level element) 
   
- Note: A block container box can both establish a block formatting context and an inline formatting context simultaneously. 
   
- Floating an item also creates a BFC for that item, and so our columns don’t attempt to wrap around each other 
   
