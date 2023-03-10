# Special Edition- CSS in Web Performance - CSS-Tricks

**Author:** Chris  
**Full title:** Special Edition: CSS in Web Performance - CSS-Tricks  
**URL:** https://css-tricks.com/newsletter/special-edition-css-in-web-performance/  
**Source:** #articles #instapaper #readwise

- CSS is Render Blocking 
   
- If it wasn’t, the web would either be very jerky-looking all the time, with extreme “Flashes of Unstyled Content” (FOUC). 
   
- Critical CSS”, where the only CSS that loads is that which is needed for that very first paint, and the rest is deferred 
   
- Do we make the CSS async? Or can we make the JavaScript ignore that CSS is blocking? 
   
- Blocking JS execution is bad. In today’s JS-rich apps a delay like this is a life/death situation 
   
- Scott Jehl noted in The Simplest Way to Load CSS Asynchronously 
   
- <link 
  rel="stylesheet" 
  href="/path/to/my.css" 
  media="print"
  onload="this.media='all'"> 
   
- making some JavaScript run without waiting for CSS, even if you don’t change the HTML syntax for loading the CSS at all. It’s not async or defer on the <script>, those do nothing unfortunately in this case. It’s a Data URL! 
   
- <script 
  async 
  src="data:text/javascript,log%5B%27inline%20HEAD%20script%27%5D%20%3D%20%2Bnew%20Date%20-%20start%3B">
  </script> 
   
- It will execute as soon as the browser sees it, not waiting for the CSS to load. 
   
- Using Less CSS 
   
- if you have junk stylesheets that do nothing for you, those need to get gone. 
   
- Another player here is this whole world of Atomic CSS. 
   
- What about CSS in JS? 
   
- instead your JavaScript component files have chunks of CSS-like code in them to do the styling. 
   
- JavaScript is definitely a slower thing to load and execute than CSS is, so that’s going to make things slower off the bat (more JavaScript). But right away you have to factor in that we may not be loading any .css files at all! 
   
- TLDR: Don’t use runtime CSS-in-JS if you care about the load performance of your site. Simply less JS = Faster Site. 
   
- It’s taken for granted at this point that when it comes to CSS, the best performance is… CSS. Just as little of it as is reasonably possible. 
   
