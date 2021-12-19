# Maximally Optimizing Image Loading for the Web in 2021

**Author:** industrialempathy.com  
**Full title:** Maximally Optimizing Image Loading for the Web in 2021  
**URL:** https://www.industrialempathy.com/posts/image-optimizations/  
**Source:** #articles #instapaper #readwise

- Minimizing the Largest Contentful Paint (LCP) through reducing bytes, caching, and lazy loading 
   
- Keeping Cumulative Layout Shift (CLS) to zero 
   
- Reducing First Input Delay(FID) through reduced (main-thread) CPU usage. 
   
- Optimization techniques 
   
- Responsive layout 
   
- in 2020 is that web browsers will reserve the correct vertical space for the image before it loads if the width and height attributes are provided for the img element. This avoids Cumulative Layout Shift (CLS). 
   
- <style>
  img {
  max-width: 100%;
  height: auto;
  }
  </style>
  <img height="853" width="1280" … /> 
   
- Lazy rendering 
   
- The new CSS attribute content-visibility: auto instructs the browser to not bother layouting the image until it gets near the screen 
   
- the most important one might be that the browser will not bother decoding our blurry placeholder image or the image itself unless it has to, saving CPU. 
   
- <style>
  main img {
  content-visibility: auto;
  }
  </style> 
   
- AVIF is notable because it very consistently outperforms JPEG in a very significant way. 
   
- To implement progressive enhancement for AVIF, use the picture element. 
   
- The actual img element is nested in the picture. This can be quite confusing, because the img is sometimes described as fallback for browsers without picture support 
   
- Load the right number of pixels 
   
- srcset and sizes attributes 
   
- the browser will always download the smallest possible image that provides the best image quality for the user. Or it may select a smaller image if, for example, the user has opted into some kind of data-saving mode. 
   
- Fallbacks 
   
- <source
  sizes="(max-width: 608px) 100vw, 608px"
  srcset="
  /img/Z1s3TKV-1920w.webp 1920w,
  /img/Z1s3TKV-1280w.webp 1280w,
  /img/Z1s3TKV-640w.webp 640w,
  /img/Z1s3TKV-320w.webp 320w
  "
  type="image/webp"
  />
  <source
  sizes="(max-width: 608px) 100vw, 608px"
  srcset="
  /img/Z1s3TKV-1920w.jpg 1920w,
  /img/Z1s3TKV-1280w.jpg 1280w,
  /img/Z1s3TKV-640w.jpg 640w,
  /img/Z1s3TKV-320w.jpg 320w
  "
  type="image/jpeg"
  /> 
   
- Caching / Immutable URLs 
   
- You want your caching headers to look something like this cache-control: public,max-age=31536000,immutable. 
   
- Lazy loading 
   
- Adding loading="lazy" to the img instructs the browser to only start fetching the image as it gets closer to the screen and is likely to actually be rendered. 
   
- <img loading="lazy" … /> 
   
- Asynchronous decoding 
   
- Adding decoding="async" to the img gives the browser permission to decode the image off the main thread avoiding user impact of the CPU-time used to decode the image. 
   
- <img decoding="async" … /> 
   
- Blurry placeholder 
   
- A blurry placeholder is an inline image that provides the user some notion of the image that will load eventually without requiring fetching bytes from the network. 
   
- It inlines the blurry placeholder as a background-image of the image. This avoids using a second HTML element and it naturally hides the placeholder when the image loads, so that no JavaScript is needed to implement this. 
   
- It wraps the data URI of the actual image in a data URI of a SVG image. That is done because the blurring of the image is done at the SVG level instead of through a CSS filter. 
   
- The result is that the blurring is only performed once per image when the SVG is rasterized, instead of on every layout saving CPU. 
   
- <img
  style="
  …
  background-size: cover;
  background-image: 
  url('data:image/svg+xml;charset=utf-8,%3Csvg xmlns=\'http%3A//www.w3.org/2000/svg\'
  xmlns%3Axlink=\'http%3A//www.w3.org/1999/xlink\' viewBox=\'0 0 1280 853\'%3E%3Cfilter id=\'b\' color-interpolation-filters=\'sRGB\'%3E%3CfeGaussianBlur stdDeviation=\'.5\'%3E%3C/feGaussianBlur%3E%3CfeComponentTransfer%3E%3CfeFuncA type=\'discrete\' tableValues=\'1 1\'%3E%3C/feFuncA%3E%3C/feComponentTransfer%3E%3C/filter%3E%3Cimage filter=\'url(%23b)\' x=\'0\' y=\'0\' height=\'100%25\' width=\'100%25\' 
  xlink%3Ahref=\'data%3Aimage/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAkAAAAGCAIAAACepSOSAAAACXBIWXMAAC4jAAAuIwF4pT92AAAAs0lEQVQI1wGoAFf/AImSoJSer5yjs52ktp2luJuluKOpuJefsoCNowB+kKaOm66grL+krsCnsMGrt8m1u8mzt8OVoLIAhJqzjZ2tnLLLnLHJp7fNmpyjqbPCqLrRjqO7AIeUn5ultaWtt56msaSnroZyY4mBgLq7wY6TmwCRfk2Pf1uzm2WulV+xmV6rmGyQfFm3nWSBcEIAfm46jX1FkH5Djn5AmodGo49MopBLlIRBfG8yj/dfjF5frTUAAAAASUVORK5CYII=\'%3E%3C/image%3E%3C/svg%3E');
  "
  …
  /> 
   
- (Optional-ish) JavaScript optimization 
   
- Browsers may feel obliged to rasterize the blurry placeholder even if the image is already loaded 
   
- if your images contain transparency, then this is actually not optional as otherwise the placeholder would shine through. 
   
