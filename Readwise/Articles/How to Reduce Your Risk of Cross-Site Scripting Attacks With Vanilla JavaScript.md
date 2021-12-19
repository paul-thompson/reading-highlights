# How to Reduce Your Risk of Cross-Site Scripting Attacks With Vanilla JavaScript

**Author:** gomakethings.com  
**Full title:** How to Reduce Your Risk of Cross-Site Scripting Attacks With Vanilla JavaScript  
**URL:** https://gomakethings.com/how-to-reduce-your-risk-of-cross-site-scripting-attacks-with-vanilla-javascript/  
**Source:** #articles #instapaper #readwise

- Cross-site scripting (or XSS) attacks work by unexpectedly running JavaScript that does things like scrape cookies or grab data from localStorage and send it off to a remote location. 
   
- In an XSS attack, malicious code gets injected into your site and then executed 
   
- If you’re injecting your own markup into a page, there’s little cause for concern. The danger comes from injecting third-party or user-generated content into the DOM. 
   
- How do you prevent XSS attacks from happening? 
   
- Plain text properties. XSS attacks work when we inject markup into the UI. 
   
- We can use plain text properties (like Node.textContent) instead of HTML properties (like Element.innerHTML) 
   
- Encoding strings. If you need to use an HTML property but want certain bits of your string to render as plain text, you can encode that bit of string by converting any HTML characters to their plain text equivalents. 
   
- Sanitizing. This is the process of removing any potentially dangerous properties and values from HTML elements before injecting them into the UI. 
   
