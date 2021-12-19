# The Humble  img  Element and Core Web Vitals — Smashing Magazine

**Author:** smashingmagazine.com  
**Full title:** The Humble <img> Element and Core Web Vitals — Smashing Magazine  
**URL:** https://www.smashingmagazine.com/2021/04/humble-img-element-core-web-vitals/  
**Source:** #articles #instapaper #readwise

- In this guide, we will be using Lighthouse to identify opportunities to improve the Core Web Vitals 
   
- You can also find Lighthouse in PageSpeed Insights, CI and WebPageTest. 
   
- Keep in mind that Lighthouse is a lab tool 
   
- To ensure our image is accessible, we add the alt attribute. The value of this attribute should be a textual description of the image, and is used as an alternative to the image when it can’t be displayed or seen 
   
- Images can impact the Core Web Vitals in a number of ways. E.g. LCP measures when the largest contentful element (images, text) in a user’s viewport, such as one of these images, becomes visible. 
   
- Largest Contentful Paint (LCP) is a Core Web Vitals metric that measures when the largest contentful element (images, text) in a user’s viewport, such as one of these images, becomes visible. 
   
- When an image is the largest contentful element, how slowly that image loads can impact LCP. In addition to applying image compression (e.g using Squoosh, Sharp, ImageOptim or an image CDN), and using a modern image format, you can tweak the <img> element to serve the most appropriate responsive version of an image or lazy-load it. 
   
- Layout shifts can be distracting to users. Imagine you’ve started reading an article when all of a sudden elements shift around the page, throwing you off and requiring you to find your place again. 
   
- The most common causes of CLS include images without dimensions 
   
- It’s possible for images to block a user’s bandwidth and CPU on page load. They can get in the way of how critical resources are loaded, in particular on slow connections and lower-end mobile devices leading to bandwidth saturation 
   
- ignoring them means the browser may not be able to reserve sufficient space in advance of them loading. 
   
- By reducing main-thread CPU usage, FID can also be reduced 
   
- Lighthouse 
   
- Use CSS aspect-ratio or aspect ratio boxes to reserve space otherwise 
   
- For low impact to First Input Delay 
   
- While not render-blocking, they can indirectly impact render performance. 
   
- How Do Images Impact User Experience And The Core Web Vitals? 
   
- Avoid images causing network contention with other critical resources like CSS and JS. 
   
- You may have heard of Core Web Vitals (CWV). It’s an initiative by Google to share unified guidance for quality signals that can be key to delivering a great user experience on the web 
   
- The humble <img> element has gained some superpowers over the years. 
   
- For a fast Largest Contentful Paint: 
   
- Request your key hero image early. 
   
- Use srcset + efficient modern image formats.
  Avoid wasting pixels (compress, don’t serve overly high DPR images). 
   
- Lazy-load offscreen images (reduce network contention for key resources). 
   
- For a low Cumulative Layout Shift 
   
- Set dimensions (width, height) on your images. 
   
