# Consistent  Fluidly Scaling Type and Spacing

**Author:** css-tricks.com  
**Full title:** Consistent, Fluidly Scaling Type and Spacing  
**URL:** https://css-tricks.com/consistent-fluidly-scaling-type-and-spacing/  
**Source:** #articles #instapaper #readwise

- inconsistent spacing—especially vertically—that makes content hard to scan and creates this subtle, disjointed feeling. 
   
- What the heck is a sizing scale? 
   
- A sizing scale is a uniform progression of sizes based on a scale—or, more accurately, a ratio. 
   
- “Perfect Fourth” scale which uses a ratio of 1.333. This means each time you go up a size, you multiply the current size by 1.333, and each time you go down a size, you subtract 1.333. 
   
- CSS clamp() and type fluidity 
   
- the summary of clamp() is that it does clever stuff based on three parameters you give it:
  a minimum value
  an ideal value
  a maximum value 
   
- CSS gives us full responsive text sizes based on the viewport width with handy locks to make sure sizes don’t get too big or too small. 
   
- :root {
  --size-300: clamp(0.7rem, 0.66rem + 0.2vw, 0.8rem);
  --size-400: clamp(0.88rem, 0.83rem + 0.24vw, 1rem);
  --size-500: clamp(1.09rem, 1rem + 0.47vw, 1.33rem);
  --size-600: clamp(1.37rem, 1.21rem + 0.8vw, 1.78rem);
  --size-700: clamp(1.71rem, 1.45rem + 1.29vw, 2.37rem);
  --size-800: clamp(2.14rem, 1.74rem + 1.99vw, 3.16rem);
  --size-900: clamp(2.67rem, 2.07rem + 3vw, 4.21rem);
  --size-1000: clamp(3.34rem, 2.45rem + 4.43vw, 5.61rem);
  }; 
   
