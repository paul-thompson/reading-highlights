# When a Line Doesn’t Break   CSS-Tricks

**Author:** css-tricks.com  
**Full title:** When a Line Doesn’t Break | CSS-Tricks  
**URL:** https://css-tricks.com/when-a-line-doesnt-break/  
**Source:** #articles #instapaper #readwise

- We expect a line to break when the text on that line reaches the parent box boundaries 
   
- When the parent box doesn’t have enough room for the next word in a line, it breaks it and moves down to the next line and repeats that process. 
   
- As far as CSS goes, there are five (!) properties that can possibly affect how and when a line breaks. 
   
- characters that are use for formatting purposes but considered by minifies to be irrelevant to the final result. 
   
- The browser does actually care about whitespaces… but only sometimes. 
   
- We can get natural line breaks from special characters 
   
- Besides spaces, excluding non-breaking spaces (&nbsp;), there are some other characters that will force a line break 
   
- Besides spaces, excluding non-breaking spaces 
   
- there are some other characters that will force a line break 
   
- After hyphen (-)
  After en dash (–)
  Before and after em dash (—)
  After question mark (?)
  Zero-width white space (U+200B or &#8203;) 
   
- After hyphen (-)
  After en dash (–)
  Before and after em dash (—) 
   
- After hyphen (-) 
   
- After hyphen 
   
- After en dash 
   
- Before and after em dash 
   
- After question mark 
   
- Zero-width white space (U+200B or &#8203;) 
   
- Zero-width white space 
   
- These line breaks happen at rendering time which means the browser still sees this as one long word. 
   
- Use pseudo-elements 
   
- What makes this solution effective is that it’s not affected by an HTML minifier because the whitespace is added when the CSS is applied. 
   
- there’s a little trick to using ::after and the content property with whitespacing and display: inline-block. The inline-block element adds a breaking character at the end of the text. Then the content property space comes after the breaking character created by the inline-block element, which results in the space being removed at rendering time. That is, unless the white-space property is set to pre 
   
- Use inline-block instead 
   
- This works similar to adding a zero-width space character, but the list items will have no visual separation. 
   
- We can also turn to the display: inline-flex instead of inline-block solution. 
   
