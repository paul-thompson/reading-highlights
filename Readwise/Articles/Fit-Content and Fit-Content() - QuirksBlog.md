# Fit-Content and Fit-Content() - QuirksBlog

**Author:** quirksmode.org  
**Full title:** Fit-Content and Fit-Content() - QuirksBlog  
**URL:** https://www.quirksmode.org/blog/archives/2021/04/fitcontent_and.html  
**Source:** #articles #instapaper #readwise

- fit-content and fit-content(), which are special values for width and grid definitions. 
   
- Normally (i.e. with width: auto defined or implied) a box will take as much horizontal space as it can 
   
- order the browser to determine it from the box’s contents. That’s what min-content and max-content do 
   
- min-content means: the minimal width the box needs to contain its contents. In practice this means that browsers see which bit of content is widest and set the width of the box to that value. 
   
- The widest bit of content is the longest word in a text 
   
- max-content means: the width the box needs to contain all of its contents. 
   
- all text is placed on one line and the box becomes as wide as necessary to contain that entire line 
   
- The largest bit of content may also be an image or video other asset; in that case browsers use this width to determine the box’s width 
   
- If you use hyphens: auto or something similar, the browser will break the words at the correct hyphenation points before determining the minimal width 
   
- fit-content 
   
- box {
  width: auto;
  min-width: min-content;
  max-width: max-content;
  } 
   
- fit-content as min- or max-width 
   
- this fairly useless and potentially confusing. What you really mean is min-width: min-content or max-width: max-content. If that’s what you mean, say so. Your CSS will be clearer if you do. 
   
- I believe that it would be better not to use fit-content for min-width or max-width; but only for width 
   
- fit-content in flexbox and grid: nope 
   
- fit-content does not work in flexbox and grid 
   
- Note that grid and flex items have min-width: min-content by default, 
   
- fit-content() 
   
- fit-content and fit-content() as width 
   
- Grid 
   
- 1fr fit-content(200px) 1fr 
   
- It means
  1fr min(max-content-size, max(min-content, 200px)) 
   
- The max() argument becomes min-content or 200 pixels, whichever is larger 
   
