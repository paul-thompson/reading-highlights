# Cumulative Layout Shift

**Author:** debugbear.com  
**Full title:** Cumulative Layout Shift  
**URL:** https://www.debugbear.com/docs/metrics/cumulative-layout-shift  
**Source:** #articles #instapaper #readwise

- Cumulative Layout Shift (CLS) measures how much content moves around on the page after being rendered. 
   
- Layout shifts hurt user experience, as they can cause accidental clicks on the wrong element or make users lose track of where they were when reading an article. 
   
- The Cumulative Layout Shift score currently accounts for 5% over the overall Lighthouse Performance score. 
   
- You can prevent layout shifts if you know the size of the element that's being loaded. 
   
- In that case, you can provide an empty placeholder with the appropriate height, and then fill in the contents later. 
   
- Web fonts 
   
- Web fonts can also cause layout shifts, as the size of rendered text changes once the fonts have loaded. 
   
- You can reduce these layout shifts by using setting the font-display CSS property to either optional or fallback. 
   
- Lighthouse lab data only tests layout shifts during the initial page load, while field data also counts layout shifts that users experience when scrolling down the page 
   
