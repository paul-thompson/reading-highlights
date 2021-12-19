# MindBEMding – Getting Your Head ’round BEM Syntax – CSS Wizardry – Web Performance Optimisation

**Author:** Harry Roberts  
**Full title:** MindBEMding – Getting Your Head ’round BEM Syntax – CSS Wizardry – Web Performance Optimisation  
**URL:** https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/  
**Source:** #articles #instapaper #readwise

- BEM – meaning block, element, modifier – is a front-end naming methodology thought up by the guys at Yandex 
   
- The naming convention follows this pattern 
   
- .block {}
  .block__element {}
  .block--modifier {} 
   
- The reason for double rather than single hyphens and underscores is so that your block itself can be hyphen delimited, for example 
   
- .site-search {} 
  .site-search__field {} 
  .site-search--full {} 
   
- The point of BEM is to tell other developers more about what a piece of markup is doing from its name alone 
   
- By using BEM we can be more descriptive but also a lot more explicit; we tie concrete links to other elements of our code through naming alone. Powerful stuff 
   
- I dare say that if you shy away from code based purely on its looks then you’re often missing the point. 
   
- When you are using BEM, though, it is important to remember that you don’t need to use it for everything 
   
- .caps { text-transform: uppercase; } 
   
- This CSS would never fall into any BEM category, it’s merely a standalone rule. 
   
- .site-logo {} 
   
- Just because something happens to live inside a block it doesn’t always mean is is actually a BEM element. In the case of our site logo it lives in the .header purely coincidentally 
   
- One of the hardest parts of BEM is deciding when to start and stop scope, and when (or not) to use it. 
   
