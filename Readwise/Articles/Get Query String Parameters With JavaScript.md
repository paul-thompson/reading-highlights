# Get Query String Parameters With JavaScript

**Author:** David Walsh  
**Full title:** Get Query String Parameters With JavaScript  
**URL:** https://davidwalsh.name/query-string-javascript  
**Source:** #articles #instapaper #readwise

- We've always been able to get the full query string via the window.location.search property: 
   
- After years of ugly string parsing, there's a better way: URLSearchParams Let's have a look at how we can use this new API to get values from the location! 
   
- URLSearchParams also provides familiar Object methods like keys(), values(), and entries() 
   
- While URLSearchParams is ideal, not all browsers support that API. 
   
- function getUrlParameter(name) {
  name = name.replace(/[\[]/, '\\[').replace(/[\]]/, '\\]');
  var regex = new RegExp('[\\?&]' + name + '=([^&#]*)');
  var results = regex.exec(location.search);
  return results === null ? '' : decodeURIComponent(results[1].replace(/\+/g, ' '));
  }; 
   
- getUrlParameter('post'); // "1234"
  getUrlParameter('action'); // "edit" 
   
