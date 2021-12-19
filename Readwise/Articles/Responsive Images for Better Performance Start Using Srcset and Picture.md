# Responsive Images for Better Performance- Start Using Srcset and Picture

**Author:** dev.to  
**Full title:** Responsive Images for Better Performance: Start Using Srcset and Picture  
**URL:** https://dev.to/mustapha/responsive-images-for-better-performance-start-using-srcset-and-picture-11kc  
**Source:** #articles #instapaper #readwise

- The srcset and sizes attributes 
   
- Two new attributes have been added to the <img> tag: srcset and sizes. These two attributes tell the browser what resolutions are available for a given image, and what size the image is supposed to be displayed at, at any given breakpoint 
   
- The srcset attribute contains a comma-separated list of URLs with a w-descriptor 
   
- One awesome thing about this syntax is that we don’t need to tell the browser what images to use for the different pixel density displays, and what images to use for the different screen sizes. The browser is able to pick the best image size on its own. 
   
- The sizes attribute 
   
- While the srcset attribute describes the actual width of the source files, the sizes attribute tells the browser how wide the image is supposed to be displayed on the screen. 
   
- <img srcset="/assets/images/image-tiny.jpeg 150w,
  /assets/images/image-small.jpeg 300w,
  /assets/images/image-medium.jpeg 600w,
  /assets/images/image-large.jpeg 1000w,
  /assets/images/image-extra-large.jpeg 1500w"
  sizes="(max-width: 700px) calc(100vw - 10px),
  calc(50vw - 10px)"
  src="/assets/images/image-medium.jpeg"
  alt="A photo of Lyon city"> 
   
- Note that the order of the image-URLs in the srcset attribute doesn’t matter. The order in the sizes attribute, however, matters a lot! 
   
- Picture 
   
- You can think of the <picture> element as a group of image sources. 
   
- <picture>
  <!-- Dark theme -->
  <source media="(prefers-color-scheme: dark)"
  srcset="/assets/images/tiny-dark.png 150w,
  /assets/images/small-dark.png 300w,
  /assets/images/medium-dark.png 600w,
  /assets/images/large-dark.png 1000w,
  /assets/images/xl-dark.png 1500w"
  sizes="(max-width: 700px) 100vw, 50vw">
  <!-- Light theme -->
  <source srcset="/assets/images/tiny.png 150w,
  /assets/images/small.png 300w,
  /assets/images/medium.png 600w,
  /assets/images/large.png 1000w,
  /assets/images/xl.png 1500w"
  sizes="(max-width: 700px) 100vw, 50vw">
  <img src="/assets/images/medium.png" alt="Banner image">
  </picture> 
   
- you should always add an <img> tag inside the the <picture> tag to specify the alt attribute and loading="lazy" if you want to lazy load the image. 
   
