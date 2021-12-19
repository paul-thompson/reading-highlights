# Stick to Compositor-Only Properties and Manage Layer Count

**Author:** developers.google.com  
**Full title:** Stick to Compositor-Only Properties and Manage Layer Count  
**URL:** https://developers.google.com/web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  
**Source:** #articles #instapaper #readwise

- Compositing is where the painted parts of the page are put together for displaying on screen. 
   
- TL;DR 
   
- Stick to transform and opacity changes for your animations. 
   
- Promote moving elements with will-change or translateZ. 
   
- Avoid overusing promotion rules; layers require memory and management. 
   
- Use transform and opacity changes for animations 
   
- The best-performing version of the pixel pipeline avoids both layout and paint, and only requires compositing changes 
   
- Today there are only two properties for which that is true - transforms and opacity: 
   
- The caveat for the use of transforms and opacity is that the element on which you change these properties should be on its own compositor layer. 
   
- Promote elements that you plan to animate 
   
- you should promote elements that you plan to animate 
   
- .moving-element {
  will-change: transform;
  } 
   
- Or, for older browsers, or those that don’t support will-change 
   
- .moving-element {
  transform: translateZ(0);
  } 
   
- the browser can potentially make provisions, such as creating compositor layers. 
   
- Manage layers and avoid layer explosions 
   
- The problem here is that every layer you create requires memory and management, and that’s not free. In fact, on devices with limited memory the impact on performance can far outweigh any benefit of creating a layer. 
   
- Warning: Do not promote elements unnecessarily. 
   
- Use Chrome DevTools to understand the layers in your app 
   
- enable the Paint profiler in Chrome DevTools’ Timeline 
   
