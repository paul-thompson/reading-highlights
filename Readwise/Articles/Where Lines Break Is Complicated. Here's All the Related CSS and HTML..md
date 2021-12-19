# Where Lines Break Is Complicated. Here's All the Related CSS and HTML.

**Author:** css-tricks.com  
**Full title:** Where Lines Break Is Complicated. Here's All the Related CSS and HTML.  
**URL:** https://css-tricks.com/where-lines-break-is-complicated-heres-all-the-related-css-and-html/  
**Source:** #articles #instapaper #readwise

- The text hanging out of the box is a visual problem. 
   
- Overflow is the right word here as well, as that’s exactly what is happening. We have overflow: auto; at our disposal as well, which would trigger a horizontal scrollbar. 
   
- The Sledgehammer: word-break: break-all; 
   
- Allows words to be broken anywhere. The word-break property does “solve” the issue 
   
- the word-break property redefines what a word is. The break-all value essentially treats non-CJK as CJK, which can break just about anywhere (except stuff like periods and close parenthesis). The keep-all value does the reverse, treating CJK as non-CJK 
   
- the word-break property redefines what a word is. The break-all value essentially treats non-CJK as CJK, which can break just about anywhere (except stuff like periods and close parenthesis). 
   
- the word-break property redefines what a word is. 
   
   - Note: The break-all value essentially treats non-CJK as CJK, which can break just about anywhere (except stuff like periods and close parenthesis). The keep-all value does the reverse, treating CJK as non-CJK
   
- The break-all value essentially treats non-CJK as CJK 
   
- A Subtle Fix: `overflow-wrap: break-word;` 
   
- p {
  word-wrap: break-word; /* old name */
  overflow-wrap: break-word;
  } 
   
- At first glance it might look very similar to the word-break: break-all; demo above, but notice how in the URL rather than breaking “pen” at “pe\n”, it breaks at the end of that word where the slash is 
   
- “If a word can’t break and would therefore overflow, then it can break anywhere to avoid overflow.” 
   
- A Heavier Fix, Sometimes: hyphens: auto; 
   
- The hyphens property does what you might expect…allows for hyphenation in line breaks 
   
- Hyphens can sometimes do the trick in URLs and long words, but it’s not guaranteed 
   
- hyphens affect all the text, breaking words more liberally to help text hug that right edge evenly 
   
- p {
  hyphens: auto;
  } 
   
- If a ‘word’ straddles the end of the line, we can hyphenate it 
   
- Future Sledgehammer: line-break: anywhere; 
   
- like word-break: break-all; except it actually breaks everything like a dumb terminal client. 
   
- The <wbr> element is a “word-break opportunity” meaning a long word that would normally cause an annoying overflow issue could be told that it’s ok to break at a certain point. Useful! It behaves like a zero-width space. 
   
- The &shy; character is just like the <wbr> element. 
   
- You can inject a line break via pseudo-element like ::before { content: "\A"; } as long as the element isn’t inline (or if it is, it needs white-space: pre;) 
   
