# Modern Alternatives to BEM

**Author:** Home  
**Full title:** Modern Alternatives to BEM  
**URL:** https://daverupert.com/2022/08/modern-alternatives-to-bem/  
**Source:** #articles #instapaper #readwise

- We want to author in components
  We generally want low-specificity to avoid collisions
  We want a bucket (sometimes a very large bucket) of global utility classes or variables for ad-hoc composition or customizations 
   
- CUBE 
   
- - Composition
  - Utilities
  - Block
  - Exception 
   
- it’s less prescriptive about how you author “blocks” (read: components). You could totally use BEM inside that zone if you wanted. 
   
- HECS 
   
- In Web Components you get component-level scoping right out of the gate with Shadow DOM 
   
- The tradeoff here is Web Components eject from the cascade 
   
- CSS variables operate in a strange land of inheritable styles that do pass through the Shadow DOM, but not all Web Components support CSS variables, so your ability to control style gets limited by the components you use or the amount of Light DOM in your components. 
   
- WILS 
   
- You can author your CSS with near-zero specificity and even control the order in which your rules cascade. 
   
- - :where() # Zero specificity
  - :is() # Specificity is highest selector in group
  - @layer # High specificity, but control order styles apply
  - @scope # High specificity, but stop and start of styles 
   
- Over-abstracting in my head a bit, WILS is probably best on a global utility layer or base component library where you need to de-specify as much as possible. 
   
- GPC 
   
- Global styles, Page level styles, and Section-specific styles. 
   
- All your global CSS goes in the global layer, page-specific CSS goes in the page layer, and component (section-specific) styles go in the component layer. 
   
