# Building a Resilient Frontend Using Progressive Enhancement

**Author:** gov.uk  
**Full title:** Building a Resilient Frontend Using Progressive Enhancement  
**URL:** https://www.gov.uk/service-manual/technology/using-progressive-enhancement  
**Source:** #articles #instapaper #readwise

- based on the idea that you should start by making your page work with just HTML, before adding anything else like Cascading Style Sheets (CSS) and JavaScript. 
   
- HTML is the most resilient layer. If the HTML fails there’s no web page. 
   
- make your service more resilient
  mean your service’s most basic functionality will work and meet the core needs of the user
  improve accessibility by encouraging best practices like writing semantic markup
  help users with device or connectivity limitations to use your service 
   
- Using interactive elements 
   
- there must be a fallback that allows for the same core functionality. For example, a dynamic autocomplete element could fall back to a <select> element, or something similar. 
   
- You must also structure your source order and document outline logically. 
   
- Once you’ve built a foundation of HTML for your service, you can add things 
   
- images
  styling
  video and audio
  scripted behaviour, for example JavaScript
  smoother and faster interactions that do not require the user to refresh the entire page
  ways to validate data that users submit before that data hits the network
  interactive charts 
   
- Building more complex services 
   
- first try to make the functionality work without JavaScript. If that’s not possible, your JavaScript implementation should have a fallback digital interaction 
   
- Using JavaScript frameworks 
   
- Some JavaScript frameworks require the user to download large amounts of data 
   
- Using JavaScript frameworks can cause other issues, such as 
   
- reliance on third-party code that your developers do not have control over
  difficulties in finding the skills required to maintain the framework, if its popularity drops 
   
- The server should render the HTML fallback and deliver that code to the browser as normal. You can then use JavaScript to enhance the component where necessary 
   
- Using JavaScript server-side rendering (SSR) 
   
- You can use server-side rendering, also known as isomorphic JavaScript or Universal JavaScript. 
   
- Testing your service 
   
- You’ll need to test the components of your service that heavily rely on JavaScript or JavaScript frameworks for accessibility. 
   
- Do not assume users turn off CSS or JavaScript 
   
- There are many situations when extra layers can fail to load or are filtered 
   
- temporary network errors
  third-party browser extensions like ad blockers
  third-party supplier downtime, such as when using a content delivery network
  DNS lookup failures
  bugs introduced by browser updates
  corporate firewalls blocking, removing or changing content (large institutions like banks or government departments may use these) 
   
- mobile network providers changing content to speed up load times and reduce bandwidth usage
  personal firewalls or antivirus software changing or blocking content
  the use of unsecure connections, where internet providers insert their own code into the page that accidentally conflicts with your own 
   
