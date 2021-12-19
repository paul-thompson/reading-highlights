# HTTP Request Methods

**Author:** dev.to  
**Full title:** HTTP Request Methods  
**URL:** https://dev.to/adidoshi/http-request-methods-16ik  
**Source:** #articles #instapaper #readwise

- An HTTP request is an action to be performed on a resource identified by a given Request-URL. Request methods are case-sensitive, always noted in upper case. 
   
- HTTP requests work as the intermediary transportation method between a client/application and a server. 
   
- 1. GET Method 
   
- GET method is used to retrieve and request data from a specified resource in a server. 
   
- A GET request is often used to typically fetch json data from the server, there are different formats by which you can retrieve the data 
   
- XML
  HTML
  Text
  JSON 
   
- 2. POST method 
   
- Another popular HTTP request method is POST. In web communication, POST requests are utilized to send data to a server to create or update a resource. 
   
- 3. PUT method 
   
- PUT is similar to POST as it is used to send data to the server to create or update a resource. 
   
- The difference between the two is that PUT requests are idempotent.
  This means that if you call the same PUT requests multiple times, the results will always be the same 
   
- 4. Delete method 
   
- the DELETE request method is used to delete resources indicated by a specific URL. Making a DELETE request will remove the targeted resource 
   
- The difference from POST is that you will need the id of the record to DELETE or PUT. 
   
- 5. PATCH 
   
- A PATCH request is similar to POST and PUT. However, its primary purpose is to apply partial modifications to the resource 
   
- the PATCH request is also non-idempotent. Additionally, unlike POST and PUT which require a full user entity, with PATCH requests, you may only send the updated username. 
   
