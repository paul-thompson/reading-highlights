# Accessible Tap Targets

**Author:** web.dev  
**Full title:** Accessible Tap Targets  
**URL:** https://web.dev/accessible-tap-targets/  
**Source:** #articles #instapaper #readwise

- When your design is displayed on a mobile device, you should ensure that interactive elements like buttons or links are large enough, and have enough space around them, to make them easy to press without accidentally overlapping onto other elements. 
   
- A minimum recommended touch target size is around 48 device independent pixels on a site with a properly set mobile viewport. 
   
- Touch targets should also be spaced about 8 pixels apart, both horizontally and vertically, so that a user's finger pressing on one tap target does not inadvertently touch another tap target. 
   
- Testing your touch targets 
   
- you can use DevTools to check that the computed value of that area is large enough. 
   
- Using media queries to detect touchscreen use 
   
- A coarse pointer indicates a touchscreen, which could be a mobile device but may also be a laptop screen or large tablet. 
   
- If you are adjusting your CSS within a media query to increase the touch target, testing for a coarse pointer allows you to increase the tap targets for all touchscreen users. 
   
- .container a {
  padding: .2em;
  }
  @media (pointer: coarse) {
  .container a {
  padding: .8em;
  }
  } 
   
