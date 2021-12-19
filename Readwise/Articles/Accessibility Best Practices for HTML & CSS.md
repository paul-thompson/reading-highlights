# Accessibility Best Practices for HTML & CSS

**Author:** codingcat.dev  
**Full title:** Accessibility Best Practices for HTML & CSS  
**URL:** https://codingcat.dev/post/9aa1087f-eade-4156-a0d0-30354885c8b7  
**Source:** #articles #instapaper #readwise

- I still recommend having experienced screen readers and accessibility experts test your site and run your site through the WebAIM Web Accessibility Evaluation Tool, WAVE. 
   
- Having better accessibility isn't only the right thing to do, it also increases your Search Engine Optimization, SEO, which can rank you higher in Google's algorithm 
   
- Everything should start with a good foundation and with Hypertext Markup Language, HTML, that is the structure of your page 
   
- a blind user only hears the order defined in the HTML of a page 
   
- see the layout of a page linearized into one column and the order of the markup to see if it makes sense. 
   
- Semantic HTML 
   
- The word semantic relates to the meaning of something in a language or logic. 
   
- The layout of the page defines the page regions that are identified by web browsers and assistive technologies. 
   
- Structural 
   
- Use the header and footer elements to define the top and bottom of a page, but also can define the top and bottom of an article or section. 
   
- Use the nav element for major blocks of links to allow assistive technologies to quickly and easily navigate through the site. 
   
- Use the main tag to define the main content of the page and aside to define anything related to the main content. 
   
- Only use divs and spans for styling purposes. Use the section tag to group related elements with a heading and the article tag to group a self-contained item that is independent or reusable 
   
- The article element can be posts, news articles, product cards, comments, or any other form of independent items or content 
   
- Content 
   
- Use the correct levels for headings, from the most important as an h1 down through h6 and do not skip heading levels 
   
- Use the paragraph, p, element to wrap self-contained blocks of text that focus on a single topic or theme. 
   
- Use the anchor, a, tag for links that go somewhere else and the button tag for an action like submitting a form or a click event. 
   
- Language 
   
- Don't use dashes if you can avoid it. Instead of writing 5–7, write 5 to 7. 
   
- Expand abbreviations — instead of writing Jan, write January. 
   
- Expand acronyms, at least once or twice. Instead of writing HTML in the first instance, write Hypertext Markup Language. 
   
- Forms 
   
- consider keeping forms short and only ask users for the minimal information needed to complete the process. 
   
- Use the label element with a for attribute that matches an id attribute on the accompanying input or wrap the label around the input. 
   
- Make sure instructions needed to complete an input are listed before the input area and make clear if an input is required and any validation requirements 
   
- Styling 
   
- The best practice is to leave the browser defaults if you don't know how to correctly restyle them 
   
- Contrast 
   
- There should be sufficient contrast between any foreground text and the background color behind it 
   
- There are many extensions and plugins that check for contrast issues, but they can be inaccurate and inconsistent. The WebAIM provides a contrast checker at https://webaim.org/resources/contrastchecker/. 
   
- For non-text items the contrast ratio should be a minimum of 3:1. 
   
- States 
   
- The focus state shows when a user is focused, either by click, keyboard, or voice, on an element. Only interactive elements need to have a focus state. 
   
- The hover and active states are sometimes styled similarly. The active state shows when something is activated, usually a button or a link, and the hover shows when it is being hovered on. The styles are not the important part for accessibility on these elements, but telling assistive technologies when an element is active is important 
   
- Animations 
   
- Users should be able to control any moving, flashing, or blinking content on a page. 
   
- A good practice is to use a prefers-reduced-motion media feature to turn off animations. If the animation is critical to understanding something, add it back in with a selector after turning down all animations 
   
- Make sure all animated content has pause, stop and hide capabilities and check the tab order to ensure it works correctly. 
   
- Do NOT have anything that flashes more than three times in a one second period as this is known to cause seizures 
   
