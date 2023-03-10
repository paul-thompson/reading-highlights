# How Browsers Work- Behind the Scenes of Modern Web Browsers - HTML5 Rocks

**Author:** html5rocks.com  
**Full title:** How Browsers Work: Behind the Scenes of Modern Web Browsers - HTML5 Rocks  
**URL:** https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/  
**Source:** #articles #instapaper #readwise

- UI backend: used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. Underneath it uses operating system user interface methods. 
   
- It is important to note that browsers such as Chrome run multiple instances of the rendering engine: one for each tab. Each tab runs in a separate process. 
   
- Different browsers use different rendering engines: Internet Explorer uses Trident, Firefox uses Gecko, Safari uses WebKit. Chrome and Opera (from version 15) use Blink, a fork of WebKit. 
   
- The rendering engine will start getting the contents of the requested document from the networking layer. This will usually be done in 8kB chunks 
   
- The rendering engine will start parsing the HTML document and convert elements to nodes in a tree called the "content tree". 
   
- The render tree contains rectangles with visual attributes like color and dimensions. The rectangles are in the right order to be displayed on the screen. 
   
- The browser's main functionality 
   
- The main flow 
   
- Parsing is based on the syntax rules the document obeys: the language or format it was written in. 
   
- The job of the HTML parser is to parse the HTML markup into a parse tree 
   
- DOM 
   
- The output tree (the "parse tree") is a tree of DOM element and attribute nodes. 
   
