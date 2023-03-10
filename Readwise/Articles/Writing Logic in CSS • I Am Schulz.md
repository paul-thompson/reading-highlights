# Writing Logic in CSS • I Am Schulz

**Author:** Control Structures  
**Full title:** Writing Logic in CSS • I Am Schulz  
**URL:** https://iamschulz.com/writing-logic-in-css/  
**Source:** #articles #instapaper #readwise

- CSS is a highly specialized programming language focusing on style systems 
   
- Control Structures 
   
- Variables 
   
- Variables are the most straightforward ones. They’re called Custom Properties in CSS 
   
- :root {
  --color: red;
  }
  span {
  color: var(--color, blue);
  } 
   
- The double-dash declares a variable and assigns a value. 
   
- has to happen in a scope because doing so outside of a selector would break the CSS syntax 
   
- Notice the :root selector, which works as a global scope. 
   
- Conditions 
   
- Selectors are scoped to their elements, media queries are scoped globally, and need their own selectors. 
   
- Attribute Selectors 
   
- [data-attr="true"] {
  /* if */
  }
  [data-attr="false"] {
  /* elseif */
  }
  :not([data-attr]) {
  /* else */
  } 
   
- Pseudo Classes 
   
- :checked {
  /* if */
  }
  :not(:checked) {
  /* else */
  } 
   
- Media Queries 
   
- :root {
  color: red; /* else */
  }
  @media (min-width > 600px) {
  :root {
  color: blue; /* if */
  }
  } 
   
- Loops 
   
- Counters are both the most straightforward form of loops in CSS, but also the one with the narrowest use case 
   
- main {
  counter-reset: section;
  }
  section {
  counter-increment: section;
  counter-reset: section;
  }
  section > h2::before {
  content: "Headline " counter(section) ": ";
  } 
   
- .grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  } 
   
- This fills the grid with as many elements as it can fit, while scaling them to fill the available space, but breaking them into multiple rows when it needs. It repeats for as long as it finds items and caps them to a minimum width of 300px and a maximum width of one fraction of its own size 
   
- finally, there are looped selectors. They take an argument, which can be a formula to select very precisely. 
   
- section:nth-child(2n) {
  /* selects every even element */
  }
  section:nth-child(4n + 2) {
  /* selects every fourth, starting from the 2nd */
  } 
   
- Logic Gates 
   
- Ana Tudor wrote an article on CSS Logic Gates. Those work on the idea of combining variables with calc 
   
- Techniques 
   
- The Owl Selector
  * + * {
  margin-top: 1rem;
  } 
   
- The Owl Selector selects every item that follows an item. 
   
- Conditional Styling 
   
