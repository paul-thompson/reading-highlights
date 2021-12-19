# How to Use JSON.parse() and JSON.stringify()   DigitalOcean

**Author:** digitalocean.com  
**Full title:** How to Use JSON.parse() and JSON.stringify() | DigitalOcean  
**URL:** https://www.digitalocean.com/community/tutorials/js-json-parse-stringify  
**Source:** #articles #instapaper #readwise

- The JSON object, available in all modern browsers, has two useful methods to deal with JSON-formatted content: parse and stringify. 
   
- JSON.parse() takes a JSON string and transforms it into a JavaScript object 
   
- JSON.stringify() takes a JavaScript object and transforms it into a JSON string. 
   
- although the methods are usually used on objects, they can also be used on arrays 
   
- JSON.parse() can take a function as a second argument that can transform the object values before they are returned 
   
- const userStr = JSON.stringify(user);
  JSON.parse(userStr, (key, value) => {
  if (typeof value === 'string') {
  return value.toUpperCase();
  }
  return value;
  }); 
   
- Note: Trailing commas are not valid in JSON, so JSON.parse() throws an error if the string passed to it has trailing commas. 
   
- JSON.stringify() can take two additional arguments, the first one being a replacer function and the second a String or Number value to use as a space in the returned string. 
   
- The replacer function can be used to filter out values 
   
