# What Is a URL - Learn Web Development   MDN

**Author:** developer.mozilla.org  
**Full title:** What Is a URL? - Learn Web Development | MDN  
**URL:** https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL  
**Source:** #articles #instapaper #readwise

- Uniform Resource Locators (URLs) 
   
- With Hypertext and HTTP, URL is one of the key concepts of the Web. It is the mechanism used by browsers to retrieve any published resource on the web 
   
- A URL is nothing more than the address of a given unique resource on the Web 
   
- each valid URL points to a unique resource. Such resources can be an HTML page, a CSS document, an image, etc 
   
- A URL is composed of different parts, some mandatory and others optional. 
   
- think of a URL like a regular postal mail address 
   
- the scheme represents the postal service you want to use 
   
- the domain name is the city or town 
   
- the port is like the zip code 
   
- the path represents the building where your mail should be delivered 
   
- the parameters represent extra information such as the number of the apartment in the building 
   
- the anchor represents the actual person to whom you've addressed your mail. 
   
- The first part of the URL is the scheme, which indicates the protocol that the browser must use to request the resouce 
   
- Usually for websites the protocol is HTTPS or HTTP (its unsecured version). 
   
- browsers also know how to handle other schemes such as mailto: (to open a mail client) 
   
- the authority, which is separated from the scheme by the character pattern :// 
   
- If present the authority includes both the domain (e.g. www.example.com) and the port (80), separated by a colon 
   
- If present the authority includes both the domain (e.g. www.example.com) and the port (80) 
   
- If present the authority includes both the domain 
   
- and the port (80), separated by a colon 
   
- and the port 
   
- separated by a colon 
   
- The domain indicates which Web server is being requested. Usually this is a domain name, but an IP address may also be used 
   
- The port indicates the technical "gate" used to access the resources on the web server. 
   
- It is usually omitted if the web server uses the standard ports of the HTTP protocol (80 for HTTP and 443 for HTTPS) to grant access to its resources. Otherwise it is mandatory 
   
- The separator between the scheme and authority is :// 
   
- The colon separates the scheme from the next part of the URL, while // indicates that the next part of the URL is the authority. 
   
- One example of a URL that doesn't use an authority is the mail client 
   
- /path/to/myfile.html is the path to the resource on the Web server 
   
- Nowadays, it is mostly an abstraction handled by Web servers without any physical reality. 
   
- The Web server can use those parameters to do extra stuff before returning the resource. Each Web server has its own rules regarding parameters, and the only reliable way to know if a specific Web server is handling parameters is by asking the Web server owner 
   
- #SomewhereInTheDocument is an anchor to another part of the resource itself. 
   
- It is worth noting that the part after the #, also known as the fragment identifier, is never sent to the server with the request. 
   
- The HTML language — which will be discussed later on — makes extensive use of URLs 
   
- to create links to other documents with the <a> element; 
   
- to link a document with its related resources through various elements such as <link> or <script>; 
   
- to display media such as images (with the <img> element), videos (with the <video> element), sounds and music (with the <audio> element), etc.; 
   
- to display other HTML documents with the <iframe> element. 
   
- The required parts of a URL depend to a great extent on the context in which the URL is used. 
   
- When a URL is used within a document, such as in an HTML page, things are a bit different. Because the browser already has the document's own URL, it can use this information to fill in the missing parts of any URL available inside that document 
   
- We can differentiate between an absolute URL and a relative URL by looking only at the path part of the URL. If the path part of the URL starts with the "/" character, the browser will fetch that resource from the top root of the server, without reference to the context given by the current document. 
   
- We can differentiate between an absolute URL and a relative URL by looking only at the path part of the URL 
   
- If the path part of the URL starts with the "/" character, the browser will fetch that resource from the top root of the server, without reference to the context given by the current document. 
   
- character, the browser will fetch that resource from the top root of the server, without reference to the context given by the current document. 
   
   - Note: If the URL starts with a "/"
   
- Implicit protocol 
   
- In this case, the browser will call that URL with the same protocol as the one used to load the document hosting that URL. 
   
- Implicit domain name 
   
- The browser will use the same protocol and the same domain name as the one used to load the document hosting that URL. Note: it isn't possible to omit the domain name without omitting the protocol as well. 
   
