# Styling Tables

**Author:** mozilla.org  
**Full title:** Styling Tables  
**URL:** https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Styling_tables  
**Source:** #articles #reader #readwise

- A [`table-layout`](https://developer.mozilla.org/en-US/docs/Web/CSS/table-layout) value of `fixed` is generally a good idea to set on your table, as it makes the table behave a bit more predictably by default 
   
- Normally, table columns tend to be sized according to how much content they contain, which produces some strange results 
   
- A [`border-collapse`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse) value of `collapse` is standard best practice for any table styling effort 
   
- set some [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) on the [`<th>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th) and [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td) elements — this gives the data items some space to breathe, making the table look a lot more legible. 
   
- Make your table markup as simple as possible, and keep things flexible, e.g. by using percentages, so the design is more responsive. 
   
- Use [`table-layout`](https://developer.mozilla.org/en-US/docs/Web/CSS/table-layout)`: fixed` to create a more predictable table layout that allows you to easily set column widths by setting [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) on their headings ([`<th>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th) 
   
- Use [`<thead>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead), [`<tbody>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody), and [`<tfoot>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot) to break up your table into logical chunks and provide extra places to apply CSS to, so it is easier to layer styles on top of one another if required. 
   
