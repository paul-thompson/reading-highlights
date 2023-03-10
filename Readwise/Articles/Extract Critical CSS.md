# Extract Critical CSS

**Author:** Case studies  
**Full title:** Extract Critical CSS  
**URL:** https://web.dev/extract-critical-css/  
**Source:** #articles #instapaper #readwise

- The browser must download and parse CSS files before it can show the page, which makes CSS a render-blocking resource 
   
- Key Term 
   
- Critical CSS is a technique that extracts the CSS for above-the-fold content in order to render content to the user as fast as possible 
   
- Improving render times can make a huge difference in perceived performance, especially under poor network conditions. On mobile networks, high latency is an issue regardless of bandwidth. 
   
- If you have poor First Contentful Paint (FCP) and see "Eliminate render-blocking resource" opportunity in Lighthouse audits it's a good idea to give critical CSS a go. 
   
- Keep in mind that if you inline a large amount of CSS, it delays the transmission of the rest of the HTML document. If everything is prioritized then nothing is 
   
- Inlining also has some downsides in that it prevents the browser from caching the CSS for reuse on subsequent page loads, so it's best to use it sparingly 
   
- To minimize the number of roundtrips to first render, aim to keep above-the-fold content under 14 KB (compressed). 
   
- For most servers, 10 packets or approximately 14 KB is the maximum that can be transferred in the first roundtrip. 
   
- Generally speaking, the more CSS a site has, the greater the possible impact of inlined CSS. 
   
- Overview of tools 
   
- Critical 
   
- Critical extracts, minifies and inlines above-the-fold CSS and is available as npm module. 
   
- CriticalCSS is another npm module that extracts above-the-fold CSS. It is also available as a CLI. 
   
- Penthouse 
   
- Penthouse is a good choice if your site or app has a large number of styles or styles which are being dynamically injected into the DOM 
   
