# Handling Long Words and URLs (Forcing Breaks  Hyphenation  Ellipsis  Etc)   CSS-Tricks

**Author:** @css-tricks  
**Full title:** Handling Long Words and URLs (Forcing Breaks, Hyphenation, Ellipsis, Etc) | CSS-Tricks  
**URL:** https://css-tricks.com/snippets/css/prevent-long-urls-from-breaking-out-of-container/  
**Source:** #articles #instapaper #readwise

- .dont-break-out {
  /* These are technically the same, but use both */
  overflow-wrap: break-word;
  word-wrap: break-word;
  -ms-word-break: break-all;
  /* This is the dangerous one in WebKit, as it breaks things wherever */
  word-break: break-all;
  /* Instead use this non-standard one: */
  word-break: break-word;
  /* Adds a hyphen where the word breaks, if supported (No Blink) */
  -ms-hyphens: auto;
  -moz-hyphens: auto;
  -webkit-hyphens: auto;
  hyphens: auto;
  } 
   
- overflow-wrap: break-word; makes sure the long string will wrap and not bust out of the container. You might as well use word-wrap as well because as the spec says, they are literally just alternate names for each other 
   
- With overflow-wrap in use all by itself, words will break kinda anywhere they need to. If there is an “acceptable break” character (like a literal dash, for instance), it will break there, otherwise it just does what it needs to do 
   
- You might as well use hyphens as well, because then it will try to tastefully add a hyphen where it breaks if the browser supports it (Blink doesn’t at time of writing, Firefox does). 
   
- word-break: break-all; is to tell the browser that it’s OK to break the word wherever it needs to. Even though it kinda does that anyway so I’m not sure in what cases it’s 100% necessary. 
   
