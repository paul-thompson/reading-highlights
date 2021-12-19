# Barebones CSS for Fluid Images—zachleat.com

**Author:** Zach Leatherman  
**Full title:** Barebones CSS for Fluid Images—zachleat.com  
**URL:** https://www.zachleat.com/web/fluid-images/  
**Source:** #articles #instapaper #readwise

- width: 100% CSS forces the image to fill up the width of the container. This overrides any [width] attribute you have set 
   
- The 100% in max-width refers to the container dimensions 
   
- Practically speaking, the image will never grow larger than its own internal or intrinsic dimensions 
   
- Another way to think about this, the image width can range between 0 and [width], depending on the container size. 
   
- When I traditionally used width: 100% it bulldozed the [width] attribute 
   
- a strict max-width: 100% now competes with the [width] attribute. One easy solution here is to add width: auto to pair with our max-width: 100% CSS 
   
- srcset and max-width: 100%
  Using [width="400"][height="400"] 
   
- when [width][height] are not included or when width: auto was left off. The maximum width now correctly matches the intrinsic width of the largest image in our srcset list. 
   
- practically I would recommend to pair max-width: 100% with width: auto to fix this in the easiest way but this might help avoid some confusion for some folks that aren’t aware of this 
   
- img {
  max-width: 100%;
  }
  img[width] {
  width: auto; 
  }
  img[width][height] {
  height: auto; 
  } 
   
- img[src$=".svg"] {
  width: 100%;
  height: auto;
  max-width: none;
  } 
   
- ❌ <img> with { max-width: 100%; width: auto; height: auto } console logs CLS penalties. 
   
- img[width][height] {
  height: auto; 
  } 
   
