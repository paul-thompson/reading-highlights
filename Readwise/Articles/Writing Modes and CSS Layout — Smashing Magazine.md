# Writing Modes and CSS Layout — Smashing Magazine

**Author:** Rachel Andrew  
**Full title:** Writing Modes and CSS Layout — Smashing Magazine  
**URL:** https://www.smashingmagazine.com/2019/08/writing-modes-layout/  
**Source:** #articles #instapaper #readwise

- underpin our new layout methods, and those ideas are increasingly being applied across all of CSS 
   
- What Are Writing Modes? 
   
- The writing mode of a document or a component refers to the direction that text flows 
   
- A language such as Arabic also has a horizontal-tb writing mode 
   
- however Arabic script is written right to left, and so sentences in Arabic start on the right. 
   
- Chinese, Japanese and Korean are written vertically, with the first character of the first sentence being top right. Following sentences being added to the left 
   
- vertical-rl. A vertical writing mode running from right to left. 
   
- Mongolian is also written vertically, but from left to right. 
   
- should you want to typeset Mongolian script you would use the writing mode vertical-lr. 
   
- The other two values of writing-mode are designed more for creative purposes than for typesetting vertical scripts. Using sideways-lr and sideways-rl turns text sideways — even characters normally written vertically and upright 
   
- When we change the writing mode of a document, what we are doing is switching the direction of the block flow 
   
- Inline elements, such as a word in a sentence display one after the other in the inline direction 
   
- Working in a horizontal writing mode, we become used to the fact that the block dimension runs top to bottom vertically, and the inline dimension left to right horizontally. 
   
- the inline dimension is horizontal only if we are in a horizontal writing mode. 
   
- The block dimension is only vertical when in a horizontal writing mode. Therefore it doesn’t relate to height, but to block size. 
   
- Logical, Flow-Relative Properties 
   
- the names of new CSS properties designed to reflect our new writing mode aware world. 
   
- If you use width that will always be a physical dimension 
   
- If you use inline-size, that will be the size in the inline dimension 
   
- The block-size property, however, gives the size in the block dimension, vertically if we are in a horizontal writing mode and horizontal in a vertical one. 
   
- I mentioned that the grid-area property could be used to set all four lines to place a grid item 
   
- Instead, we need to use top, left, bottom, right - the reverse of that order! Until I understood the connection between grid and writing modes 
   
- I came to realize that what we are doing is setting both start lines, then both end lines 
   
- If we use grid-area: 1 / 2 / 3 / 5; as in the pen below the lines are set as follows:
  grid-row-start: 1; - block start
  grid-column-start: 2 - inline start
  grid-row-end: 3 - block end
  grid-column-end: 5 - inline end 
   
- A row will follow the inline dimension of the writing mode in use. 
   
- if your writing mode is horizontal-tb a row runs horizontally. 
   
- If the text direction of the current script is left to right then items will line up starting from the left, if it is right to left they will line up starting on the right. 
   
- the inline direction is vertical. 
   
- With a writing mode of vertical-rl a column is horizontal 
   
- Grid Auto-Placement 
   
