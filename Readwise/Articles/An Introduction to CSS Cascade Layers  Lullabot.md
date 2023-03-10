# An Introduction to CSS Cascade Layers   Lullabot

**Author:** Chris DeLuca  
**Full title:** An Introduction to CSS Cascade Layers | Lullabot  
**URL:** https://www.lullabot.com/articles/introduction-css-cascade-layers  
**Source:** #articles #reader #readwise

- Cascade layers help solve the problem of **specificity escalation**. Specificity escalation is a problem where your styles get more and more specific, not to achieve a more narrow selection of elements but simply to override previous styles. 
   
- Cascade Layers offer a method of *direct* control over [specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity). It uses a new at-rule, `@layer`, to group styles in priority order. 
   
- @layer low, high; @layer low { .greetings { background-color: purple; } } @layer high { button { background-color: green; } } 
   
- The selector inside the `high` layer has lower specificity than the selector inside the `low` layer. Yet, the `high` layer *itself* takes priority over the `low` layer. 
   
- The "regular" cascade and specificity 
   
- Cascade layers are their own style priority bucket. It sits below inline styles and above selector specificity and source order. 
   
- The Cascade layer's control is *direct*, unlike selectors. Selecting an ID has more specificity than selecting a class, but there is no way to select an element by class and give it more specificity than an ID. No way, that is, until now. Cascade layers give us that control. 
   
- Cascade layers defined with `@layer <name>`. Multiple names can be defined at once, separated by commas, and each layer has specificity precedence in the order they are defined (in this case, left to right). Multiple `@layer` definitions are allowed, and their precedence is sorted in the order they are defined. 
   
- Layer names can be anything. They work best when they describe the group of styles you are encapsulating.
  @layer vendor, base, components, utilities, 
   
- Layers can also be unnamed, but only in the block form. 
   
- Unnamed layers will have specificity in the order they were defined as normal. 
   
- Styles outside a layer will always have more priority than styles inside a layer. 
   
- Styles outside layers also have more specificity than unnamed layers. 
   
- Inside a layer block, source order still applies. This includes styles appended in a later layer block. 
   
- Unnamed layers can not be appended. 
   
