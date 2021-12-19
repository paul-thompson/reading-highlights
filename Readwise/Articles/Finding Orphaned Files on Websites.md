# Finding Orphaned Files on Websites

**Author:** shallowsky.com  
**Full title:** Finding Orphaned Files on Websites  
**URL:** https://shallowsky.com/blog/tags/weborphan/  
**Source:** #articles #instapaper #readwise

- I noticed a lot of old files, files that didn't seem to be referenced by any of the site's pages. Orphaned files. 
   
- I found a few people who had managed to use linklint, but only by spidering an entire website to local files (thus getting rid of any server side dependencies like PHP, CGI or SSI) and then running linklint on the local directory. 
   
- What I needed was a program that could look at a website and local directory at the same time, and compare them, flagging any file that isn't referenced by anything on the website. 
   
- I ended up with a script called weborphans (on github). Give it both a local directory for the files making up your website, and the URL of that website, for instance:
  $ weborphans /var/www/ http://localhost/ 
   
