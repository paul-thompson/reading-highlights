# Resizing With CSS

**Author:** CSS { In Real Life } | Resizing with CSS  
**Full title:** Resizing With CSS  
**URL:** https://css-irl.info/resizing-with-css/?ref=css-layout-news  
**Source:** #articles #reader #readwise

- You can select which direction to apply the resizing: `horizontal`, `vertical` or `both`, as well as logical properties `inline` and `block`, with `none` as the default.
  /* Makes the element horizontally resizeable */div { resize: horizontal;} 
   
- The element must be a scroll container, meaning that it must have its `overflow` property value set to `scroll` or `auto` in order for `resize` to have any effect. 
   
- `resize` also respects flex and grid layouts. 
   
- One drawback is the resize control is only positioned in the bottom right corner of the element, and it’s not possible to style it. 
   
