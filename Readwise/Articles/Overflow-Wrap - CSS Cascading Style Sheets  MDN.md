# Overflow-Wrap - CSS- Cascading Style Sheets   MDN

**Author:** developer.mozilla.org  
**Full title:** Overflow-Wrap - CSS: Cascading Style Sheets | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-wrap  
**Source:** #articles #instapaper #readwise

- overflow-wrap 
   
- The overflow-wrap CSS property applies to inline elements, setting whether the browser should insert line breaks within an otherwise unbreakable string to prevent text from overflowing its line box. 
   
- Note: In contrast to word-break, overflow-wrap will only create a break if an entire word cannot be placed on its own line without overflowin 
   
- normal
  Lines may only break at normal word break points (such as a space between two words). 
   
- anywhere 
   
- To prevent overflow, an otherwise unbreakable string of characters — like a long word or URL — may be broken at any point if there are no otherwise-acceptable break points in the line. 
   
- No hyphenation character is inserted at the break point. Soft wrap opportunities introduced by the word break are considered when calculating min-content intrinsic sizes. 
   
- break-word 
   
- The same as the anywhere value 
   
- but soft wrap opportunities introduced by the word break are NOT considered when calculating min-content intrinsic sizes. 
   
