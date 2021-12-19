# 5 Eleventy Tweaks That Make My Sites Better (And Maybe Yours) · Jens Oliver Meiert

**Author:** meiert.com  
**Full title:** 5 Eleventy Tweaks That Make My Sites Better (And Maybe Yours) · Jens Oliver Meiert  
**URL:** https://meiert.com/en/blog/5-eleventy-tweaks/  
**Source:** #articles #instapaper #readwise

- Centrally Defined Layouts 
   
- Staying with the Eleventy base blog, instead of defining post.njk as the layout in each post, you extend the respective posts.json so that it, instead, sets the layout 
   
- {
  "layout": "post.njk",
  "tags": [
  "posts"
  ]
  } 
   
- Title Sorting 
   
- eleventyConfig.addFilter("sortByTitle", values => {
  return values.slice().sort((a, b) => a.data.title.localeCompare(b.data.title))
  }) 
   
- call this filter through sortByTitle 
   
- Easy Hiding of Posts 
   
- you can define an “alias” (here hidden) quite easily by adding or modifying eleventyComputed.js in the _data folder 
   
- module.exports = {
  eleventyExcludeFromCollections: data => (data.eleventyExcludeFromCollections || data.hidden)
  }; 
   
- I prefer the global alias, allowing me to hide content using hidden: true 
   
- Localized Date Formatting 
   
- Eleventy’s readableDate filter to make use of .setLocale() together with an adjusted date format 
   
- eleventyConfig.addFilter("readableDate", dateObj => {
  return DateTime.fromJSDate(dateObj, {zone: "utc+1"}).setLocale("de").toFormat("d. MMMM yyyy");
  }); 
   
- Versioned Output 
   
- The key to me is output monitoring—understanding exactly what goes live and what changed with each update 
   
