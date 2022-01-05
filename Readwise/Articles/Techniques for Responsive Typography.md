# Techniques for Responsive Typography

**Author:** tympanus.net  
**Full title:** Techniques for Responsive Typography  
**URL:** https://tympanus.net/codrops/2013/11/19/techniques-for-responsive-typography/  
**Source:** #articles #instapaper #readwise

- One of the most important aspects of responsive web design is responsive typography. 
   
- From choosing a font type and color, to achieving legible font sizes, line heights, and line lengths on different screen sizes, there are several ways to go about achieving fluid and truly responsive text on the web. 
   
- First Things First: Making text accessible 
   
- you need to make sure that your text is legible and accessible by using sufficient color contrast and an easily readable font to avoid turning your page’s content into an eye sore. 
   
- Choose A Readable Font Face 
   
- when it comes to body type you need to make sure you choose a font that’s easily readable. 
   
- /* Declare your font using the @font-face rule */
  /* Source: http://www.paulirish.com/2009/bulletproof-font-face-implementation-syntax/ */
  @font-face {
  font-family: 'Graublau Web';
  src: url('GraublauWeb.eot?') format('eot'), 
  url('GraublauWeb.woff') format('woff'), 
  url('GraublauWeb.ttf') format('truetype');
  } 
   
- After you’ve declared your font, you can use it just like you would use any other font in your style sheet, and provide a fallback font 
   
- 'Droid Sans', Arial, sans-serif; /* you can add any number of fallback fonts */ 
   
- Font Color Accessibility 
   
- A website’s content is primarily there to be read, and low-contrast font colors can lead to text being unreadable. 
   
- Text is much easier to read when there is sufficient contrast between the text and the background 
   
- the W3C also introduced a new media query concept in the Media Queries Module Level 4, namely the Luminosity media query, among other new media features, which, if implemented, will allow designers and developers to adjust the style of the document in response to the ambient luminosity in which the device is used, 
   
- Use “real” text rather than text within graphics 
   
- Although it is possible to provide alternative text for graphics, it is not possible to enlarge text in most graphics without some loss of quality (unless the graphic is vector-based 
   
- Making big headlines responsive 
   
- Using CSS Viewport Units 
   
- Using the viewport units allows you to make sure your text always fits into its container’s width, because the font size changes relative to the initial containing block, the viewport 
   
- The viewport-percentage lengths are relative to the size of the initial containing block. 
   
- 1vw = Equal to 1% of the width of the initial containing block. 
   
- there isn’t any algorithm applied to spread the letters and calculate the best number of letters on each row and then split the heading into rows like the slabText plugin 
   
- Using Media Queries 
   
- The last and most commonly known way to make headlines responsive is by using the good ol’ media queries to define the font’s size on different screen sizes, using a set of defined breakpoints to adjust the font size accordingly 
   
- body {
  font-size: 100%; /* start with a flexible baseline, more on this in the next section */
  }
  h1 {
  font-size: 2.5em;
  }
  @media screen and (max-width: 50em) {
  h1 {
  font-size:2em;
  }
  }
  @media screen and (max-width: 40em) {
  h1 {
  font-size:1.5em;
  }
  }
  @media screen and (max-width: 30em) {
  h1 {
  font-size:1.2em;
  }
  } 
   
- It’s worth noting that it’s a best practice when you’re declaring media queries that you use em for setting your media query breakpoints, as using pixels will enact a horizontal scroll bar when you zoom in to the page and things don’t scale so well 
   
- Making body text responsive 
   
- notes to keep in mind. Not only do you have to resize the text to fit its container while maintaining excellent readability and reasonable line lengths, but you need to remember to preserve vertical rhythm with optimized and flexible line heights, make sure your text scales well on high-resolution screens, and can be easily resized by the user. 
   
- Using em and Media Queries 
   
- Pixels provide a high level of control over our text sizes, but it also comes with a well-known drawback: Text doesn’t scale up (or down) when you resize it in Internet Explorer, so there’s no way your reader will be able to increase the size of the font on your page if they want to when you’re using pixels to size it 
   
- it is recommended that you use a percentage value to set the font size for your page’s body, and start defining the content size proportional to this value 
   
- Setting the font size on the body to 100% sets the text size to the browser’s default font size, which is usually 16px 
   
- A lot of developers tend to, or prefer to, use a baseline value of 62.5% on the body instead of a 100%, because the resulting font size applied to it will be an even 10px 
   
- we can’t achieve truly responsive type without maintaining a flexible line height for our content 
   
- An even better, more flexible and more convenient way to set line heights is by using unitless values. Eric Meyer has written an excellent and very clear article explaining why it’s preferable that you set line heights in unitless values. 
   
- If the rhythm of the page is to be maintained, the spacing of paragraphs should be related to the basic line height unit. This is achieved simply by setting top- and bottom-margins equal to the line height.— Richard Rutter, Compose To a Vertical Rhythm, 24Ways Blog 
   
- Using rem and Media Queries 
   
- very similar to the em, except that the font size defined using rem is set relative to the font size of the root element, the html, instead of the body, and this is where the r in rem comes from, as rem stands for “root em“. 
   
- you set a font size of 100% on the html element instead of the body, and then to resize your text in the media queries, 
   
- The best thing about using rems is that you can size the text of your entire content in context of the root element, not in the context of its container. 
   
- Using rem is also preferable when you’re working on large-scale projects with lots of content and modules where keeping track of context and font size can get very tiresome 
   
- Using CSS Viewport Units 
   
- Using viewport units to resize body text has an obvious advantage over the previous methods using em and rem in that the text becomes 100% fluid, and does not depend on a set of media query breakpoints to resize 
   
- Using a jQuery Plugin 
   
