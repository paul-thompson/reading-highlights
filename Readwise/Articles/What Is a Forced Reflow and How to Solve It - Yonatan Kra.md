# What Is a Forced Reflow and How to Solve It - Yonatan Kra

**Author:** GitHub  
**Full title:** What Is a Forced Reflow and How to Solve It? - Yonatan Kra  
**URL:** https://yonatankra.com/layout-reflow/  
**Source:** #articles #instapaper #readwise

- Force reflow (or Layout Reflow) is a major performance bottleneck 
   
- Forced Reflow is a disturbance in the force… sorry… in the flow. That means that we force a later stage (layout) into our javascript. 
   
- How forced reflow is created 
   
- Querying the DOM is called: Measure. 
   
- Changing the DOM is called: Mutate. 
   
- After you are changing the DOM, the browser flags its layout cache as invalid and schedules a recalculation 
   
- The reflow happens when during Javascript we mutate the DOM and then measure it. 
   
- How to Solve Forced Reflow? 
   
- Solving a Forced Reflow is usually straight forward. You just need to avoid a DOM measurement after a DOM mutation in the same CRP. 
   
- Summary 
   
