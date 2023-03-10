# Notes on Josh Comeau's Custom CSS Reset   CSS-Tricks

**Author:** I’m gonna  
**Full title:** Notes on Josh Comeau's Custom CSS Reset | CSS-Tricks  
**URL:** https://css-tricks.com/notes-on-josh-comeaus-custom-css-reset/  
**Source:** #articles #instapaper #readwise

- “modern” CSS resets are more of a collection of opinionated default styles that do useful things that you want on all your new projects because, well, that’s how you roll. 
   
- *, *::before, *::after {
  box-sizing: border-box;
  } 
   
- body {
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
  } 
   
- I also generally like to put global typographic sizing stuff on the html selector instead, just because the “root” part of rem implies the <html> element — not the <body> — and I like sizing stuff in rem and then adjusting the root font-size at the root level in media queries. 
   
- That 1.5 value feels like a good default line-height (more of a 1.4 guy myself, but I’d rather go up than down). 
   
- img, picture, video, canvas, svg {
  display: block;
  max-width: 100%;
  } 
   
- Good move for a CSS reset. The block display type there prevents those annoying line-height gaps that always kill me 
   
- p, h1, h2, h3, h4, h5, h6 {
  overflow-wrap: break-word;
  } 
   
- Good move for sure. It’s bad news when a long word (like a URL) forces an element wide and borks a layout. I tend to chuck this on something — like article or .text-content or something — and let it cascade into that whole area 
   
