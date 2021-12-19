# Displays Images With Incorrect Aspect Ratio

**Author:** web.dev  
**Full title:** Displays Images With Incorrect Aspect Ratio  
**URL:** https://web.dev/image-aspect-ratio/  
**Source:** #articles #instapaper #readwise

- If a rendered image has an aspect ratio that's significantly different from the aspect ratio in its source file (the natural aspect ratio), the rendered image may look distorted, possibly creating an unpleasant user experience. 
   
- How the Lighthouse image aspect ratio audit fails 
   
- Lighthouse flags any image with a rendered dimension more than a few pixels different from the expected dimension when rendered at its natural ratio 
   
- There are two common causes for an incorrect image aspect ratio 
   
- An image is set to explicit width and height values that differ from the source image's dimensions 
   
- An image is set to a width and height as a percentage of a variably-sized container 
   
- Ensure images display with the correct aspect ratio 
   
- Use an image CDN 
   
- An image CDN can make it easier to automate the process of creating different sized versions of your images 
   
- Check the CSS that affects the image's aspect ratio 
   
- Chrome DevTools can show you the CSS declarations that affect a given image. 
   
- Check the image's width and height attributes in the HTML 
   
- When possible, it's good practice to specify each image's width and height attributes in your HTML so that the browser can allocate space for the image. 
   
