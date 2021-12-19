# Idempotent - MDN Web Docs Glossary- Definitions of Web-Related Terms   MDN

**Author:** developer.mozilla.org  
**Full title:** Idempotent - MDN Web Docs Glossary: Definitions of Web-Related Terms | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Glossary/Idempotent  
**Source:** #articles #instapaper #readwise

- An HTTP method is idempotent if an identical request can be made once or several times in a row with the same effect while leaving the server in the same state 
   
- idempotent method should not have any side-effects (except for keeping statistics). 
   
- the GET, HEAD, PUT, and DELETE methods are idempotent, but not the POST method 
   
   - Note: Implemented correctly
   
- To be idempotent, only the actual back-end state of the server is considered 
   
- the status code returned by each request may differ 
   
- Another implication of DELETE being idempotent is that developers should not implement RESTful APIs with a delete last entry functionality using the DELETE method. 
   
- GET /pageX HTTP/1.1 is idempotent. Called several times in a row, the client gets the same results: 
   
- POST /add_row HTTP/1.1 is not idempotent; if it is called several times, it adds several rows 
   
