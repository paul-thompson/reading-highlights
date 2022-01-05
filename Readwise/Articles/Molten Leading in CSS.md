# Molten Leading in CSS

**Author:** css-tricks.com  
**Full title:** Molten Leading in CSS  
**URL:** https://css-tricks.com/molten-leading-css/  
**Source:** #articles #instapaper #readwise

- Tim’s coined phrase “molten leading”, which is essentially line-height that depends on line length. 
   
- What interests me most here is a fundamental triadic relationship in typesetting — that of a text’s font size, line height, and line length. Adjusting any one of these elements without also adjusting the others is a recipe for uncomfortable reading, which is one reason designers have such a difficult time with fluid web layout. 
   
- ((current width − min-width) / (max-width − min-width)) × (line-height − min-line-height) + min-line-height = line-height 
   
- body {
  font-size: 1em;
  line-height: 1.4em;
  }
  @media screen and (min-width: 20em) {
  body {
  font-size: calc(1em + (1.3125 - 1) * ((100vw - 20em) / (80 - 20)));
  line-height: calc(1.4em + (1.8 - 1.4) * ((100vw - 20em) / (80 - 20)));
  }
  }
  @media (min-width: 80em) {
  body {
  font-size: 1.3125em;
  line-height: 1.8em;
  }
  } 
   
