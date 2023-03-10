# Hyphens - CSS- Cascading Style Sheets   MDN

**Author:** CSS Scroll Snap  
**Full title:** Hyphens - CSS: Cascading Style Sheets | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Web/CSS/hyphens  
**Source:** #articles #instapaper #readwise

- The hyphens CSS property specifies how words should be hyphenated when text wraps across multiple lines 
   
- Hyphenation rules are language-specific. In HTML, the language is determined by the lang attribute, and browsers will hyphenate only if this attribute is present and the appropriate hyphenation dictionary is available. 
   
- If supported, hyphenate-character may be used to specify an alternative hyphenation character to use at the end of the line being broken. 
   
- none 
   
- Words are not broken at line breaks, even if characters inside the words suggest line break points. Lines will only wrap at whitespace. 
   
- manual 
   
- Words are broken for line-wrapping only where characters inside the word suggest line break opportunities 
   
- auto 
   
- The browser is free to automatically break words at appropriate hyphenation points, following whatever rules it chooses. 
   
- suggested line break opportunities (see below) will override automatic break point selection when present. 
   
- You must specify a language using the lang HTML attribute to guarantee that automatic hyphenation is applied in that language. 
   
- There are two Unicode characters used to manually specify potential line break points within text 
   
- U+2010 (HYPHEN) 
   
- The "hard" hyphen character indicates a visible line break opportunity. Even if the line is not actually broken at that point, the hyphen is still rendered. 
   
- U+00AD (SHY) 
   
- An invisible, "soft" hyphen. This character is not rendered visibly; instead, it marks a place where the browser should break the word if hyphenation is necessary. In HTML, use &shy; to insert a soft hyphen 
   
- When the HTML <wbr> element leads to a line break, no hyphen is added. 
   
