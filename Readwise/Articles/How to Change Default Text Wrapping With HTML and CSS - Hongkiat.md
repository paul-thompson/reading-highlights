# How to Change Default Text Wrapping With HTML and CSS - Hongkiat

**Author:** hongkiat.com  
**Full title:** How to Change Default Text Wrapping With HTML and CSS - Hongkiat  
**URL:** https://www.hongkiat.com/blog/change-default-text-wrapping-html-css/  
**Source:** #articles #instapaper #readwise

- Unlike paper, web pages can almost infinitely extend sideways. 
   
- Browsers wrap text depending on the width of the text container and the width of the screen so that we can see all the text without having to scroll sideways much (only downwards). 
   
- Wrapping is something browsers do considering many factors, such as the language of the text or the placement of punctuation and spaces 
   
- Other than wrapping, browsers also take care of the spaces; they merge multiple consecutive spaces in the source code into one single space on the rendered page, and they also register forced line breaks before start working on the wrapping. 
   
- we can easily end up in circumstances where the default browser behaviour isn’t what we are looking for 
   
- It may also happen that we just desperately need those spaces preserved in our text, however the browser keeps combining them into one, forcing us to add multiple &nbsp; in the source code. 
   
- Wrapping preferences might also change with the language and purpose of the text 
   
- Browsers decide where to wrap an overflowing text depending on word boundaries, hyphens, syllables, punctuations, spaces and more 
   
- when the browser does break the text at one such place, the break is called a soft wrap break. 
   
- The simplest way to force an extra break can be done by using the good old <br> element. 
   
- what is whitespace? It’s a set of space characters. Each space in the set varies from each other in length, direction, or both. 
   
- They also consider these space characters for wrapping opportunities (places where a text can be wrapped) when wrapping is needed. 
   
- Note that the white-space property doesn’t affect all kinds of space, just the most frequent ones such as the regular horizontal single space, tab space, and line feeds. 
   
- The pre-wrap value of white-space preserves all the whitespaces and wraps the text 
   
- The pre value of white-space preserves all the whitespaces and prevents the wrapping of the text 
   
- the pre-line value of white-space preserves the vertical whitespaces such as new lines and wraps the text 
   
- The browser didn’t break the word.
  However, if you have to allow the breaking of letters in a word so that the text would look even at the right side you need to use the break-all value for the word-break property 
   
- Developers can also add wrap opportunities inside words, using the <wbr> HTML element 
   
- The hyphens CSS property is another way to control breaks between letters in a word 
   
- In short, the property allows you to create wrapping opportunities through hyphenation. 
   
- Its auto value prompts the browser to automatically hyphenate and break words where needed while wrapping. 
   
- The overflow-wrap CSS property controls if a browser may break words (or preserved spaces, support for which might happen in the near future) on overflow 
   
- Note that overflow-wrap is also known as word-wrap (they are aliases) 
   
- Browsers wrap text depending on the width of the text container and the width of the screen 
   
- When to change default text wrapping 
   
- There are a fair number of CSS properties (and HTML elements!) that can control the wrapping and the breakpoints and also define how spaces and line breaks are processed before wrapping. 
   
- Soft wrap opportunities & soft wrap breaks 
   
- Browsers decide where to wrap an overflowing text depending on word boundaries, hyphens, syllables, punctuations, spaces and more. 
   
- Whitespace 
   
- the white-space property is about more than just wrapping. First of all, what is whitespace? It’s a set of space characters. Each space in the set varies from each other in length, direction, or both. 
   
- browsers collapse multiple spaces (both horizontal and vertical) in the source into a single space. They also consider these space characters for wrapping opportunities (places where a text can be wrapped) when wrapping is needed. 
   
- With no space in-between the letters in the HTML code above (i.e. no wrapping opportunities), the text wasn’t wrapped at first and was preserved as a single word. 
   
- when the permission was given to wrap the text by breaking words (i.e. the break-word value was given to overflow-wrap), the wrapping happened by breaking the whole string wherever it was necessary. 
   
