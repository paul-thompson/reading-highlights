# Understanding Layout Algorithms

**Author:** joshwcomeau.com  
**Full title:** Understanding Layout Algorithms  
**URL:** https://www.joshwcomeau.com/css/understanding-layout-algorithms/  
**Source:** #articles #instapaper #readwise

- CSS is so much more than a collection of properties. It's a constellation of inter-connected layout algorithms. Each algorithm is a complex system with its own rules and secret mechanisms 
   
- We need to learn how the layout algorithms work, and how they use the properties we provide to them 
   
- Layout algorithms 
   
- Flexbox
  Positioned (eg. position: absolute)
  Grid
  Table
  Flow 
   
- As the browser renders our HTML, every element will have its layout calculated using a primary layout algorithm. We can opt into different layout algorithms with specific CSS declarations 
   
- Flow is the default layout algorithm used for non-table HTML elements. Unless we explicitly opt in to another layout algorithm, Flow will be used. 
   
- more accurate to say that the z-index property is not implemented in the Flow layout algorithm, and so we'd need to pick a different layout algorithm if we want this property to have an effect 
   
- the Flexbox algorithm implements the z-index property. When the language authors were designing the Flexbox algorithm, they decided to wire up the z-index property to control stacking order, just like it does in Positioned layout. 
   
- CSS properties on their own are meaningless. It's up to the layout algorithm to define what they do, how they're used in the calculations. 
   
- In Flow layout, width is a hard rule. It will take up 2000px of space, consequences be damned. 
   
- In the Flexbox algorithm, width is more of a suggestion. 
   
- The Flexbox specification calls this the hypothetical size. It's the size that the element would be, in an idyllic world, with no constraints or forces acting upon it. 
   
- It's not that width has some special caveat when it comes to Flexbox. It's that the Flexbox algorithm implements the width property in a different way than the Flow algorithm. 
   
- The properties we write are inputs, like arguments being passed to a function. It's up to the layout algorithm to choose what to do with those inputs 
   
- In technical terms, display: flex creates a flex formatting context. All direct children will participate in this context, and it means that they will use Flexbox layout instead of the default Flow layout. 
   
- Some layout algorithms are split into multiple variants. 
   
- Positioned layout, that refers to several different “positioning schemes”:
  Relative
  Absolute
  Fixed
  Sticky 
   
- Each variant is sorta like its own mini-layout algorithm 
   
- Conflicts 
   
- As I understand it, an element will be rendered using a primary layout mode. It's a bit like specificity: certain layout modes have higher priority than others. 
   
- In general, conflicts are usually pretty obvious / intentional. But if you ever find that an element isn't behaving the way you'd expect, it can be worth trying to identify which layout algorithm it's using 
   
