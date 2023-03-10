# Animated Position of Focus Ring   CSS-Tricks - CSS-Tricks

**Author:** Reply  
**Full title:** Animated Position of Focus Ring | CSS-Tricks - CSS-Tricks  
**URL:** https://css-tricks.com/animated-position-of-focus-ring/  
**Source:** #articles #instapaper #readwise

- Maurice Mahan created FocusOverlay, a “library for creating overlays on focused elements.” 
   
- What the library actually does is animate the focus rings as focus moves from one element to another. It’s based on the same idea as Flying Focus. 
   
- Performance isn’t just script size either. Looking through the code, it looks like the focus ring is created by appending a <div> to the <body> that has a super high z-index value in which to be seen and pointer-events: none as to not interfere 
   
