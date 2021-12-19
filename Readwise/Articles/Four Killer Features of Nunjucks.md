# Four Killer Features of Nunjucks

**Author:** css-tricks.com  
**Full title:** Four Killer Features of Nunjucks  
**URL:** https://css-tricks.com/killer-features-of-nunjucks/  
**Source:** #articles #instapaper #readwise

- Nunjucks calls itself “A rich and powerful templating language for JavaScript” 
   
- It’s a full-on language, packed with all kinds of stuff you might want when writing templates. 
   
- It’s just HTML 
   
- was really just HTML with {{ handlebars }}-like templating syntax inside 
   
- 2. Includes 
   
- {% include "_header.njk 
   
- Extends / Blocks 
   
- Extends take includes to the next level 
   
- Extends allow you to define a template document with “blocks” inside of it that are meant to take chunks of content. 
   
- Macros 
   
- Macros are like imports with parameters. Like functions! You give it some values and it returns some stuff for you. 
   
- Nunjucks with Gulp 
   
- gulp.task('default', () =>
  gulp.src('index.html')
  .pipe(nunjucks.compile({
  my_data: "is here"
  }))
  .pipe(gulp.dest('dist'))
  ); 
   
