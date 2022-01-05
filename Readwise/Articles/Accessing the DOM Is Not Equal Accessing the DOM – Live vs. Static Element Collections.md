# Accessing the DOM Is Not Equal Accessing the DOM – Live vs. Static Element Collections

**Author:** stefanjudis.com  
**Full title:** Accessing the DOM Is Not Equal Accessing the DOM – Live vs. Static Element Collections  
**URL:** https://www.stefanjudis.com/blog/accessing-the-dom-is-not-equal-accessing-the-dom/  
**Source:** #articles #instapaper #readwise

- browser receives an HTML document, it creates the Document Object Model (DOM) which is a tree representation of the document 
   
- Dealing with NodeLists meant some surprises for me in the past. They look like Arrays but they are not 
   
- Although NodeList is not an Array, it is possible to iterate on it using forEach(). Several older browsers have not implemented this method yet. You can also convert it to an Array using Array.from. 
   
- Other methods that are provided by NodeLists are item, entries, keys, and values. 
   
- The magic of live collections 
   
- In some cases, the NodeList is a live collection [...] 
   
- The apparent difference is that there are more elements included when you access elements via childNodes. 
   
- childNodes) reflects the elements of the DOM even when elements were added or removed 
   
- Not every method to query the DOM returns a NodeList 
   
- HTMLCollection. So what is this other type? It only includes the matching elements and does not include text nodes, it provides only two methods (item and namedItem) and it is live which means that it will also include added elements 
   
- HTMLCollection. So what is this other type? It only includes the matching elements and does not include text nodes, it provides only two methods (item and namedItem) and it is live 
   
- HTMLCollection. So what is this other type? It only includes the matching elements and does not include text nodes, it provides only two methods 
   
- HTMLCollection is a historical artifact we cannot rid the web of. While developers are of course welcome to keep using it, new API standard designers ought not to use it [...] 
   
- a certain amount of time NodeList and HTMLCollection where competing standards and now we're stuck with both of them. 
   
- Evolving the web is complicated 
   
- we have childNodes (live NodeList) next to children (live HTMLCollection), querySelectorAll (static NodeList) next to getElementsByTagName (live HTMLCollection) and some unexpected edge-cases depending on how you access elements. 
   
