# Image Optimization

**Author:** Addy Osmani and Smashing Magazine  
**Full title:** Image Optimization  
**Source:** #books #kindle #readwise

- Images and animations are an important part of the web experience — arguably the most important part. 
   
- HTTP Archive has historically reported2 an average of two-thirds of resource bytes associated with media. 
   
- There are three metrics to consider when looking at pixel volume: CSS pixels, natural pixels, and screen pixels: 
   
- •CSS pixel volume is from the CSS perspective of layout. This measure focuses on the bounding boxes into which an image or video could be stretched or squeezed. 
   
- •Natural pixels refer to the logical pixels represented in a file. 
   
- •Screen pixels refer to the physical electronics on the display. Prior to mobile phones and modern high-resolution displays, there was a 1:1 relationship between CSS pixels and LED points on a screen. 
   
- modern screens have a higher ratio of physical pixels to traditional CSS pixels. This ratio is referred to as the device pixel ratio, or colloquially referred to as Retina™ displays. 
   
- Images represent a lower priority request by the browser but can easily block CSS and JavaScript in the download. 
   
- Slow transfers of visual content, therefore, can give the perception of a slow web page. 
   
- Optimizing image and video content is a balancing act between applying best practices that can help reduce the bytes transferred over the network and preserving the fidelity of the intended experience. 
   
- File formats: using the optimal file format. 
   
- •Responsive: applying responsive images techniques to transfer only the pixels that will be shown on screen. 
   
- •Lazy loading: to transfer content only when a human will see it. 
   
- •Accessibility: ensuring a consistent experience for all people. 
   
- Just re-encoding progressive JPEG images can save 150 milliseconds at the median and nearly 6 seconds at p90. 
   
- The good news is that there is a lot of low-hanging fruit that web developers can pick to improve image optimization and increase user engagement 
   
- Our brains are able to interpret images much faster than text, which is why high-quality images often help increase conversions, improve user engagement, and add more depth to any web page. 
   
- The effort you invest in optimizing image delivery will likely have visible, measurable results on your site’s performance. 
   
- When considering image optimization, remember that the fastest request is the one that isn’t made. 
   
- They let us convey ideas much faster than text, help us tell powerful stories and engage with our users in ways that few other forms of content can. 
   
- Often, image content is a primary visual cue that a page is ready to be used, so slow transfers of images imply the page is slow 
   
- Unoptimized images require massive amounts of bandwidth because they often have large file sizes. 
   
- Slow images can also block CSS and JavaScript owing to network contention, which itself can delay page rendering. 
   
- Faster websites often have higher conversion rates, so investing in an efficient compression strategy to minimize bloat from high-quality images is important. 
   
- Many developers err on the side of caution when setting image quality because they’re worried about degrading visual quality. 
   
- Effective compression reduces the size of an image while still delivering a crisp level of detail. 
   
- the content of an image can strongly affect how effective each format is. 
   
- Sites that load fast prioritize the resources a user needs when they need it. 
   
- Core Web Vitals is an initiative by Google to encourage sites to identify opportunities to improve user experience. 
   
- To place an image on a web page, we use the <img> element. This is an empty element — it has no closing tag — requiring a minimum of one attribute to be helpful: src, the source. 
   
- To ensure our image is accessible, we add the alt attribute. 
   
- When width and height are specified on an image, the browser knows how much space to reserve for the image until it is downloaded. 
   
- Forgetting to include the image’s dimensions can cause layout shifts, as the browser is unsure how much space the image will need. 
   
- The decoding attribute on <img> allows you to signal a preference between synchronous and asynchronous image decoding. 
   
- Placeholders 
   
- Placeholders are often inline, Base64-encoded data URLs which are low-quality image placeholders (LQIP) or SVG image placeholders (SQIP). 
   
- displaying a placeholder approximating the final image as it loads in. This can improve perceived performance in certain cases. 
   
- Lazy-Render Offscreen Content 
   
- the CSS content-visibility property, which allows the browser to skip rendering, layout, and paint for elements until they are needed. 
   
- The content-visibility property can take a number of values; auto is the one that offers performance benefits. 
   
- You can pair content-visibility with contain-intrinsic-size, which provides the natural size of the element if it is affected by size containment. 
   
- Maintain a Consistent Aspect Ratio 
   
- The aspect ratio of an image is the ratio of its width to its height. 
   
- the dimensions of images can vary and introduce layout shifts depending on how much space is available 
   
- Historically, developers have used the padding-top hack to maintain aspect ratio using an image’s width. This involves using two containers: 
   
- The new CSS aspect-ratio property, available in modern browsers, is clearer than the padding-top hack and doesn’t involve more manual calculation for positioning. 
   
- Optimizing Image Quality 
   
- Squoosh.app1 is a free, web-based tool that reduces image size through modern image compression techniques. 
   
- If you need to compress multiple images, ImageOptim 
   
- •Best quality: when quality matters more than bandwidth. 
   
- •Good quality: when you care about shipping smaller file sizes but don’t want to negatively impact image quality too much. 
   
- •Low quality: when you care enough about bandwidth that image degradation is OK. 
   
- •Lowest quality: bandwidth savings are paramount. 
   
- Audit Your Images 
   
- WebPageTest supports auditing for image compression via the “Compress Images” section. 
   
- Other popular performance auditing tools are PageSpeed Insights8 and Website Speed Test9 by Cloudinary which includes a detailed image analysis audit. 
   
- Measuring Image Quality 
   
- The image quality indexes you see in optimization tools are approximations of human perception. 
   
- There is no ideal image quality measurement, however, but some, such as the structural similarity index measure (SSIM) and Butteraugli, stand out. 
   
- SSIM 
   
- The structural similarity index measure12 is a method for measuring the similarity between two images. 
   
- The SSIM algorithm considers three key components of our visual system: luminance, contrast, and structure. 
   
- Butteraugli15 is a tool developed by Google for measuring perceived differences between images. 
   
- While SSIM looks at the aggregate of errors from an image, Butteraugli looks at the worst part. 
   
- Butteraugli to find the minimal JPEG quality threshold before visual degradation was bad enough for a user to notice something wasn’t clear. 
   
- Avoid Recompressing Images with Lossy Codecs 
   
- Each additional round of compression is going to introduce generational loss — information will be lost and compression artifacts will start to build up — even if you’re recompressing at a high quality setting. 
   
- MozJPEG (perhaps accidentally) has a better resistance to recompression degradation thanks to trellis quantization21 
   
- Trivia • ImageMagick23 is often recommended for image optimization. It’s a fine tool, but its output generally requires further optimization, and other tools can offer better output. 
   
- Comparing Image Formats 
   
- There are two fallacies when converting and comparing image formats: 
   
- That quality is a consistent term that means the same thing across all formats. 
   
- That your eyes have the same composition of photoreceptor cells (cones and rods) and that your perception of “same” and “different” is the same as everyone else’s. 
   
- To address the second fallacy, we can use math to compare the differences between images. 
   
- common algorithms that can produce an experience score include peak signal-to-noise ratio (PSNR), structural dissimilarity (DSSIM), Butteraugli, and SSIMULACRA2 (developed by Cloudinary). 
   
- Image Context 
   
- •Does the format have the functionality required (such as transparency or animation)? 
   
- •Can the target audience view the file? 
   
- •Is the format effective at optimizing this specific image content? 
   
- there are two dimensions that predominantly affect the effectiveness of formats: 
   
- Number of colors and color depth: grayscale, 8-bit, 10-bit wide gamut, etc. 
   
- Photograph versus illustration: how much of the image is generated by a computer or a camera’s image sensor? 
   
- the WebP format does not have the ability to produce full chroma images, while JPEG can. 
   
- JPEG Quality !== JPEG Quality 
   
- JPEG quality 80 with libjpeg-turbo (a JPEG encoder) will not use the same definition as quality factor 80 in MozJPEG. 
   
- Color Management 
   
- There are at least three possible perspectives to take on color: biology, physics, and print. 
   
- The additive model of RGB compared with CMYK’s subtractive model. 
   
- Color Spaces 
   
- these colors. sRGB4 was designed to be a standard5 color space for the web and is based on the RGB color model. 
   
- sRGB is about 20% narrower than Adobe RGB, and ProPhoto RGB is about 50% wider10 than Adobe RGB. 
   
- Gamma Correction and Compression 
   
- Gamma correction12 (or just gamma) controls the overall brightness of an image. Changing the gamma can also alter the ratio of red to green and blue colors. 
   
- has wide gamut or not. JPEG 
   
- Decoding image data is a key step, and decode time is a major component of the overall image load time after downloading. 
   
- Getting pixels on the screen involves using the graphics libraries provided by the underlying operating system. On most platforms, this is done with a standardized API called OpenGL. 
   
- Rasterization (“raster”) also decodes image resources in the page. “Paint” references compressed image data (e.g. JPEG) and “raster” invokes the correct decoder to decompress it. 
   
- In a single-threaded environment, both JavaScript execution and operations such as layout and rasterization occur on the main thread. 
   
- rendering of larger images causes a significant blip in performance not only due to the higher consumption of memory and processing power but also because of the way they are handled by browsers. 
   
