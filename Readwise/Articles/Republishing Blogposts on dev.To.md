# Republishing Blogposts on dev.To

**Author:** sergevandenoever.nl  
**Full title:** Republishing Blogposts on dev.To  
**URL:** https://www.sergevandenoever.nl/republishing_blogposts_on_devto/  
**Source:** #articles #instapaper #readwise

- I put a lot of work in research and writing my blog posts, so have the hope that more people could be interested in them 
   
- Create a new post on https://dev.to by pressing the WRITE A POST and copy over the Markdown 
   
- Upload all images linked into your blog to https://dev.to by clicking the image button 
   
- Select all your images of your original blog post at once. You are then provided a text area with all Direct URLs. https://dev.to rewrites the names of your images, so it is difficult to correlate the new urls to your original images. 
   
- Press Ctrl-H to do replacements on the file and select the right option for regular expressions. In the top field type ^(.*)$ and in the bottom field type $1\n![]($1)<hr/> 
   
- Put your original post next to the post in the https://dev.to edit window and replace all old image urls to the new image urls created by https://dev.to as can be seen in the Markdown preview in Visual Studio code where you have the new url with the corresponding image. 
   
- set the Canonical URL to the url of your original blog post, and add a series name if relevant 
   
- If your post is correct in the preview press publish 
   
