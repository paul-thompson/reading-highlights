# Robots.txt File [2021 Examples]

**Author:** moz.com  
**Full title:** Robots.txt File [2021 Examples]  
**URL:** https://moz.com/learn/seo/robotstxt  
**Source:** #articles #instapaper #readwise

- Robots.txt is a text file webmasters create to instruct web robots (typically search engine robots) how to crawl pages on their website. The robots.txt file is part of the the robots exclusion protocol (REP), a group of web standards that regulate how robots crawl the web, access and index content, and serve that content up to users. 
   
- Basic format: 
   
- User-agent: [user-agent name]Disallow: [URL string not to be crawled] 
   
- In a robots.txt file with multiple user-agent directives, each disallow or allow rule only applies to the useragent(s) specified in that particular line break-separated set. 
   
- If the file contains a rule that applies to more than one user-agent, a crawler will only pay attention to (and follow the directives in) the most specific group of instructions. 
   
- Blocking all web crawlers from all content 
   
- User-agent: * Disallow: / 
   
- Allowing all web crawlers access to all content 
   
- User-agent: * Disallow: 
   
- Blocking a specific web crawler from a specific folder 
   
- User-agent: Googlebot Disallow: /example-subfolder/ 
   
- Blocking a specific web crawler from a specific web page 
   
- User-agent: Bingbot Disallow: /example-subfolder/blocked-page.html 
   
- How does robots.txt work? 
   
- Search engines have two main jobs 
   
- Crawling the web to discover content;
  Indexing that content so that it can be served up to searchers who are looking for information. 
   
