# Largest Contentful Paint

**Author:** web.dev  
**Full title:** Largest Contentful Paint  
**URL:** https://web.dev/lcp/  
**Source:** #articles #instapaper #readwise

- Largest Contentful Paint (LCP) is an important, user-centric metric for measuring perceived load speed because it marks the point in the page load timeline when the page's main content has likely loaded—a fast LCP helps reassure the user that the page is useful. 
   
- Older metrics like load or DOMContentLoaded are not good because they don't necessarily correspond to what the user sees on their screen. 
   
- First Contentful Paint (FCP) only capture the very beginning of the loading experience 
   
- What is LCP? 
   
- The Largest Contentful Paint (LCP) metric reports the render time of the largest visible within the viewport, relative to when the page first started loading. 
   
- What is a good LCP score 
   
- To provide a good user experience, sites should strive to have Largest Contentful Paint of 2.5 seconds or less 
   
- a good threshold to measure is the 75th percentile of page loads, segmented across mobile and desktop devices 
   
- What elements are considered? 
   
- the types of elements considered for Largest Contentful Paint are 
   
- <img> elements
  <image> elements inside an <svg> element
  <video> elements (the poster image is used)
  An element with a background image loaded via the url() function (as opposed to a CSS gradient)
  Block-level elements containing text nodes or other inline-level text elements children. 
   
- How is an element's size determined? 
   
- The size of the element reported for Largest Contentful Paint is typically the size that's visible to the user within the viewport 
   
- If the element extends outside of the viewport, or if any of the element is clipped or has non-visible overflow, those portions do not count toward the element's size. 
   
- For image elements that have been resized from their intrinsic size, the size that gets reported is either the visible size or the intrinsic size, whichever is smaller 
   
- For text elements, only the size of their text nodes is considered (the smallest rectangle that encompasses all text nodes). 
   
- The key point is that every text node belongs to (and only to) its closest block-level ancestor element. In spec terms: each text node belongs to the element that generates its containing block. 
   
- Web pages often load in stages, and as a result, it's possible that the largest element on the page might change. 
   
- It's important to note that an element can only be considered the largest contentful element once it has rendered and is visible to the user. 
   
- Images that have not yet loaded are not considered "rendered". Neither are text nodes using web fonts during the font block period 
   
- If an element that is currently the largest contentful element is removed from the viewport (or even removed from the DOM), it will remain the largest contentful element unless a larger element is rendered. 
   
- When is largest contentful paint reported? 
   
- The browser will stop reporting new entries as soon as the user interacts with the page (via a tap, scroll, or keypress), as user interaction often changes what's visible to the user (which is especially true with scrolling). 
   
- Caution: Since users can open pages in a background tab, it's possible that the largest contentful paint will not happen until the user focuses the tab, which can be much later than when they first loaded it. 
   
- Load time vs. render time 
   
- For security reasons, the render timestamp of images is not exposed for cross-origin images that lack the Timing-Allow-Origin header. 
   
- How are element layout and size changes handled? 
   
- Only the element's initial size and position in the viewport is considered. 
   
- This means images that are initially rendered off-screen and then transition on-screen may not be reported. 
   
- LCP can be measured in the lab or in the field, and it's available in the following tools 
   
- How to measure LCP 
   
- Field tools
  Chrome User Experience Report
  PageSpeed Insights
  Search Console (Core Web Vitals report)
  web-vitals JavaScript library 
   
- Lab tools
  Chrome DevTools
  Lighthouse
  WebPageTest 
   
- measuring LCP in JavaScript is more complicated. 
   
- Measure LCP in JavaScript 
   
- LCP is primarily affected by four factors 
   
- How to improve LCP 
   
- Slow server response times
  Render-blocking JavaScript and CSS
  Resource load times
  Client-side rendering 
   
