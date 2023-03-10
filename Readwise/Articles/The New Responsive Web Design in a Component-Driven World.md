# The New Responsive- Web Design in a Component-Driven World

**Author:** Miriam Suzanne  
**Full title:** The New Responsive: Web Design in a Component-Driven World  
**URL:** https://web.dev/new-responsive/  
**Source:** #articles #instapaper #readwise

- "responsive design", you are most likely thinking about using media queries to change layout when resizing a design from mobile size, to tablet size, through to desktop size. 
   
- Viewport-based media queries give you some powerful tools, but lack a lot of finesse. 
   
- When referring to components for the sake of this article, this means elements, including elements that are made up of other elements, like a card or sidebar. Those components make up our web pages 
   
- Responsive to the user 
   
- New user preference media features, give you the ability to style web experiences that align with the user's own specific preferences and needs 
   
- This means that preference media features allow you to adapt your user experiences to your user's experiences 
   
- prefers-reduced-motion
  prefers-contrast
  prefers-reduced-transparency
  prefers-color-scheme
  inverted-colors
  And more 
   
- Preference features pick up on the preferences a user has set in their operating system, and help to build a more robust and personalized web experience, especially for those with accessibility needs. 
   
- Responsive to the container 
   
- It's hard to understate what the shift from page-based responsive design to container-based responsive design will do to evolve the design ecosystem 
   
- This amount of flexibility is something that is not possible with media queries alone. 
   
- Mixing Container Queries with Media Queries 
   
- how powerful it is to combine media queries (adjusting the global, or macro styles) with container queries (adjusting the container's children, and their micro styles). 
   
- we can think of Macro and Micro layouts within the same UI component to allow for some really nice nuanced design decisions. 
   
- Using container queries today 
   
- demos are now available to play with behind a flag in Chrome Canary. Go to about://flags in Canary and turn on the #enable-container-queries flag. 
   
- Scoped styles 
   
- the CSS working group is also actively discussing scoped styles to help with proper namespacing and collision-avoidance for components 
   
- Scoped styles allow for pass-through and component-specific styling to avoid naming collisions, something that many frameworks and plugins like CSS modules already enable us to do within frameworks 
   
- Scoping would allow us to create "donut shaped" selectors, where we can specify where to keep a style encapsulated, and where to break out of that scoped style to refer back to a more global style. 
   
- Responsive to the form factor 
   
- the new era of responsive design is a shift in form factors, and the growing possibilities of what we'll need to be designing for as a web community (such as shape-shifting screen or virtual reality). 
   
- Foldable or flexible screens, and designing for screen spanning is one example of where we can see a form factor shift today 
   
- Conclusion 
   
- This is the new responsive.
  It's combining macro layout with micro layout, and on top of all of that, it's taking user customization and form factor into account. 
   
