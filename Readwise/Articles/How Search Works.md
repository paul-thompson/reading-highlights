# How Search Works

**Author:** Lizzi Harvey  
**Full title:** How Search Works  
**URL:** https://web.dev/how-search-works/  
**Source:** #articles #instapaper #readwise

- What does a search engine do? 
   
- Search engines are the digital version of a librarian. They use a comprehensive index to help find the right information for a query. 
   
- How crawlers browse the web 
   
- Crawling is like reading through all the books in the library. Before search engines can bring any search results, they need to have as much information from the web as possible. 
   
- search engines use a crawler—a program that travels from site to site and acts like a browser 
   
- Crawlers try to fetch each URL to determine the state of the document. If a document returns an error status code, crawlers cannot use any of its content, and might retry the URL at a later time 
   
- Once they get a successful response, meaning they've found a document accessible to users, they check if it's allowed to be crawled and then download the content 
   
- Following links is how crawlers find new pages on the web. 
   
- Crawlers don't actively click links or buttons, but instead send URLs to a queue to crawl them later. When accessing a new URL, no cookies, service workers or local storage (like IndexedDB) are available 
   
- Building an index 
   
- After retrieving a document, the crawler hands the content to the search engine to add it to the index. 
   
- Search engines look at keywords, the title, links, headings, text, and many other things. These are called signals which describe the content and context of the page. 
   
- To avoid indexing and showing the recipe twice, search engines determine what the main URL should be and discard the alternative URLs showing the same content. 
   
- Serving the most useful results 
   
- Search engines do more work then just matching the query to keywords in the index. To give useful results, they might consider context, alternative wording, location of the user, and more. 
   
- When a user searches for something, search engines determine the most useful results and then show them to the user. 
   
- how to optimize for search engines 
   
- By making sure search engines can find and automatically understand your content, you are improving the visibility of your site for relevant searches. 
   
- Audit your site with Lighthouse and check the SEO results to see how well search engines can surface your content 
   
