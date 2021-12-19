# 〈img Decoding〉Attribute for Synchronous-Asynchronous Image Decode

**Author:** usefulangle.com  
**Full title:** 〈img Decoding〉Attribute for Synchronous/Asynchronous Image Decode  
**URL:** https://usefulangle.com/post/277/img-decoding-attribute  
**Source:** #articles #instapaper #readwise

- The <img> tag can include a decoding attribute through which we can specify a hint to the browser whether decoding of the image should be done synchronously or asynchronously 
   
- <!-- asynchronously decode the image -->
  <img src="img/test.jpg" decoding="async" > 
   
- async : Decode the image asynchronously. Rendering of page and decoding of image is done in parallel. This obviously makes the page to render faster. 
   
- Improve Page Performance with decoding Attribute 
   
- Decoding is an expensive operation. Until the image is decoded, the page remains in a non-responsive "frozen" state. 
   
- First the image is downloaded from the server. 
   
- Controlling Image Decode through the decoding Attribute 
   
- How Browser Renders an Image in Page 
   
- Using the decoded data, image is rendered on page 
   
- The decoding attribute for an <img> can specify whether to decode the image in parallel or along with the rest of the page content 
   
- Then image data is read (decoded). 
   
