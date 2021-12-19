# Word Wrapping and Line Breaking in HTML TADS

**Author:** tads.org  
**Full title:** Word Wrapping and Line Breaking in HTML TADS  
**URL:** http://www.tads.org/t3doc/doc/htmltads/linebrk.htm  
**Source:** #articles #instapaper #readwise

- In practice, nearly all browsers use "word wrapping" to break up text lines; this means that the browser inserts line breaks at word boundaries only, so that an individual word is never split across two lines of text 
   
- HTML TADS has two basic modes for text wrapping: word and character. 
   
- This is the default mode, and is the style that almost always applies to languages like English that use groups of letters to represent words. 
   
- The formatter's rules for determining word boundaries are simple: a word boundary is a space, or a hyphen (but a break can occur only to the right of a hyphen, and only when the hyphen isn't followed by another hyphen). 
   
- In character-wrapping mode, the formatter can break a line anywhere. This mode is especially applicable to languages like Chinese in which each character represents an entire word. 
   
- The Non-Breaking Space 
   
- Standard HTML defines its own non-breaking space character, written as "&nbsp;" 
   
- it behaves as though it were a non-space character: the formatter never breaks a line at a non-breaking space (thus the name), it never combines a non-breaking space with adjacent ordinary spaces, and it never trims a non-breaking space from the beginning or end of a line. 
   
- For line-breaking purposes, the non-breaking space behaves as though it were an alphabetic character. 
   
- if the line-breaking rules allow it, the formatter can break the line immediately before or after an ordinary non-breaking space 
   
- The Soft Hyphen 
   
- Standard HTML defines another special control, the "soft hyphen," written as "&shy;". 
   
- This character tells the interpreter that it can break a word with hyphenation at a particular point, but that it doesn't have to. 
   
- Soft hyphens are normally invisible, so you can freely insert them into words without adding visual clutter. 
   
- When the formatter decides to take advantage of a soft hyphen to break a line, though, the soft hyphen is displayed as a normal hyphen at the end of the line. 
   
