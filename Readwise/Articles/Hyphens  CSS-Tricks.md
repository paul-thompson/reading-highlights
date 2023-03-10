# Hyphens   CSS-Tricks

**Author:** DigitalOcean  
**Full title:** Hyphens | CSS-Tricks  
**URL:** https://css-tricks.com/almanac/properties/h/hyphenate/  
**Source:** #articles #instapaper #readwise

- The hyphens property controls hyphenation of text in block level elements 
   
- You can prevent hyphenation from happening at all, allow it, or only allow it when certain characters are present. 
   
- hyphens is language-sensitive. Its ability to find break opportunities depends on the language, defined in the lang attribute of a parent element 
   
- hyphens: none 
   
- Words are never hyphenated at line breaks, even if characters inside the word suggest where hyphenation could or should go. 
   
- hyphens: manual 
   
- Words are only broken at line breaks where there are characters inside the word that suggest line break opportunities. 
   
- U+2010 (HYPHEN): the “hard” hyphen character indicates a visible line break opportunity. Even if the line is not actually broken at that point, the hyphen is still rendered. Literally a “-“. 
   
- U+00AD (SHY): an invisible, “soft” hyphen. This character is not rendered visibly; instead, it suggests a place where the browser might choose to break the word if necessary. In HTML, you can use &shy to insert a soft hyphen. 
   
- hyphens: auto 
   
- Words can be broken at appropriate hyphenation points either as determined by hyphenation characters (see above) inside the word or as determined automatically by a language-appropriate hyphenation resource 
   
