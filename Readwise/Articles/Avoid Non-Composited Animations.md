# Avoid Non-Composited Animations

**Author:** web.dev  
**Full title:** Avoid Non-Composited Animations  
**URL:** https://web.dev/non-composited-animations/  
**Source:** #articles #instapaper #readwise

- Non-composited animations can appear janky (i.e. not smooth) on low-end phones or when performance-heavy tasks are running on the main thread 
   
- Background 
   
- The browser's algorithms for converting HTML, CSS, and JavaScript into pixels are collectively known as the rendering pipeline. 
   
- each step of the rendering pipeline the browser uses the result of the previous operation to create new data. 
   
- Non-composited animations perform worse because they force the browser to do more work 
   
- How Lighthouse detects non-composited animations 
   
- When an animation can't be composited, Chrome reports the failure reasons to the DevTools trace, which is what Lighthouse reads 
   
- How to ensure animations are composited 
   
