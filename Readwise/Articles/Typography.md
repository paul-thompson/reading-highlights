# Typography

**Author:** web.dev  
**Full title:** Typography  
**URL:** https://web.dev/learn/design/typography/  
**Source:** #articles #instapaper #readwise

- If you don't specify any styles for your text, browsers will apply their own default styles. These are called User Agent stylesheets 
   
- If you don't specify a line length, browsers will wrap lines of text at the edge of the screen. So text on the web is responsive by default—it flows to fit the user's viewport 
   
- There's more to typography than choosing suitable fonts to use. You need to consider the user's preferences, the size of the text, line length, and the distance between the lines of text. 
   
- Scaling text 
   
- Switching between fixed text sizes at specific breakpoints is quite jumpy. A more responsive approach is to let the user's device width influence the text size. 
   
- It's important that you don't use the vw by itself in a font-size declaration. 
   
- The text will be resizable if you mix in a relative unit—like em, rem or ch. The CSS calc() function is perfect for this. 
   
- html {
  font-size: calc(0.75rem + 1.5vw);
  } 
   
- Clamping text 
   
- You can control where the scaling starts and ends using the CSS clamp() function. 
   
- The clamp() function is like the calc() function but it takes three values. The middle value is the same as what you pass to calc() 
   
- html {
  font-size: clamp(1rem, 0.75rem + 1.5vw, 2rem);
  } 
   
- You can't set a line length directly in CSS 
   
- Do
  article {
  max-inline-size: 66ch;
  } 
   
- Line height 
   
- Although there is no line-length property in CSS, there is a line-height property. 
   
- Shorter lines of text can have larger line-height values 
   
- Use unitless values for your line-height declarations. 
   
- Combinations and scale 
   
- Remember to prioritize hierarchy as you build your user interfaces for better clarity and page flow 
   
- Web fonts 
   
- Use @font-face to tell browsers where to find your web font files. Use woff2 as your web font format 
   
- Remember, design isn't just about how the final pixels look. How fast those pixels get painted is a critical part of the user experience. 
   
- Font loading 
   
- A rel attribute with a value of preload tells the browser to prioritize that file. 
   
- You need to include the crossorigin attribute even if you are hosting the font files yourself. 
   
- Use a font-display value of swap if you still want the web font to replace the system font whenever the web font finally loads. 
   
- Instead of having separate files for regular, bold, extra bold, and so on, a variable font file is responsive. It contains all the information it needs to be displayed across a spectrum of weights or styles. 
   
- More and more system fonts are now variable fonts. 
   
- Good typography on the web isn't just about the type choices that you make as a designer. Responsive typography is also about respecting the user's device and network connection 
   
