# CSS — Layout Patterns #4

**Author:** Nidhin kumar  
**Full title:** CSS — Layout Patterns #4  
**URL:** https://levelup.gitconnected.com/css-layout-patterns-4-756d340fe507  
**Source:** #articles #reader #readwise

- RAM(Repeat, Auto, Minmax) 
   
- A responsive layout with automatically-placed and flexible children 
   
- The key terms to remember here are **repeat, auto-(fit|fill), and minmax()**, which you remember by the acronym **RAM**. 
   
- using the **auto-fit** keyword instead of an explicit numeric value. This enables auto-placement of these child elements 
   
- children have a base minimum value of **150px** with a maximum value of **1fr**, meaning on smaller screens, they will take up the full **1fr width**, and as they reach **150px** wide each, they will start to flow onto the same line. 
   
- With `**auto-fit**`, any completely empty tracks will **collapse to 0** and the filled tracks will grow to take up their space 
   
   - Note: Technically the growing is due to the Max of minmax?
   
- .parent { 
  display: grid; 
  **grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));** 
  } 
   
