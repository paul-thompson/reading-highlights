# [Sketchnote] Visibility in CSS   Megan Sullivan

**Author:** meganesulli.com  
**Full title:** [Sketchnote] Visibility in CSS | Megan Sullivan  
**URL:** https://meganesulli.com/blog/visibility-in-css/  
**Source:** #articles #instapaper #readwise

- two considerations when choosing the right approach to hiding an element with CSS 
   
- Should it still be visible in the accessibility tree? 
   
- Yes: The element should be announced by assistive technologies like screen readers. 
   
- No: The element should not be announced by assistive technologies. 
   
- Should it preserve space in the DOM? 
   
- Yes: There should be empty space left behind where the element would have been rendered if it were visible. 
   
- No: The hidden element should get pulled out of the flow of the document entirely. 
   
- Opacity is a great property to use you want to animate the visibility of an element on your page 
   
- Since opacity preserves space for the element, you don't have to worry about content lower down the page jumping up and down as your element becomes visible or invisible 
   
- Visible in Accessibility Tree & Does Not Preserve Space 
   
- .visually-hidden {
  border: 0;
  clip: rect(0,0,0,0);
  height: 1px;
  margin: -1px;
  overflow: hidden;
  padding: 0;
  position: absolute;
  width: 1px;
  } 
   
- You might use these styles for screen-reader-only text or for headings that are needed semantically but aren't part of the page's design 
   
- .visibility {
  visibility: hidden;
  } 
   
- You can use the visibility property to hide an element from assistive technologies while still leaving behind empty space for that element on the rendered page. 
   
- MDN uses the example of hiding a single cell in a table without messing up the alignment of the rest of the table cells. 
   
- Not Visible in Accessibility Tree & Does Not Preserve Space 
   
- .display-none {
  display: none;
  } 
   
- If you want an element to be hidden for both visual users and assistive technology users, you can set the display property to none. This will hide both the element and all its descendants from assistive technologies. 
   
