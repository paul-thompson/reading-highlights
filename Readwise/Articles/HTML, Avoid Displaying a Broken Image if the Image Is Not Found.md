# HTML  Avoid Displaying a Broken Image if the Image Is Not Found

**Author:** Flavio Copes  
**Full title:** HTML, Avoid Displaying a Broken Image if the Image Is Not Found  
**URL:** https://flaviocopes.com/html-remove-broken-image/  
**Source:** #articles #instapaper #readwise

- TIP: this inside an inline event handler in HTML refers to “this element” 
   
- <img src="/{{$bookname}}.png" 
  onerror="this.remove()" 
  /> 
   
- <img src="/{{$bookname}}.png" 
  onerror="this.onerror=null; this.src='fallback.png'" 
  />
  this.onerror=null here is needed so there’s no “infinite loop” if the fallback image is not found. 
   
