# Day 35- Forgiving Selectors

**Author:** Manuel Matuzović  
**Full title:** Day 35: Forgiving Selectors  
**URL:** https://www.matuzo.at/blog/2022/100daysof-day35/  
**Source:** #articles #reader #readwise

- a downside to using a selector list is that a single invalid or unsupported selector in the list of selectors invalidates the entire rule. 
   
- [:has()](https://www.matuzo.at/blog/2022/100daysof-day6/), [:where() or :is()](https://www.matuzo.at/blog/2022/100daysof-day13/) because they're so-called “forgiving selectors”. They just ignore the invalid selectors and apply the rules to the others 
   
- button:where(:hover, :focus, $btn) { 
  background-color: hwb(90 20% 20%); 
  } 
   
