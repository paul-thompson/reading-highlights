# The Section Element - HTMHell

**Author:** htmhell.dev  
**Full title:** The Section Element - HTMHell  
**URL:** https://www.htmhell.dev/tips/the-section-element/  
**Source:** #articles #instapaper #readwise

- Use the <section> element to mark up a grouping of related content, typically introduced with a heading 
   
- Implicit region and exposed role 
   
- By default, there’s no difference between a <section> and a <div> regarding the semantic information exposed to assistive technology 
   
- <section>
  <h2>Services and information</h2>
  …
  </section>
  <div>
  <h2>Services and information</h2>
  …
  </div> 
   
- <section> is no replacement for the <div> element and must not be used for styling purposes only. 
   
- Labelling it using these attributes turns it into a landmark, which exposes a different role (region) and gives screen reader users easier access to the section. 
   
- Labelling it using these attributes turns it into a landmark, which exposes a different role (region) and gives screen reader users easier access to the section. (Note: Safari doesn’t expose the region role when named via title 
   
- A general rule is that the section element is appropriate only if the element’s contents would be listed explicitly in the document’s outline 
   
- The <section>’s exposed role and purpose change when you label it using aria-label, aria-labelledby or with the title attribute. 
   
- Labelling it using these attributes turns it into a landmark 
   
- Other landmarks are, for example, <header>, <main> or <footer>, important sections of the page. 
   
- only promote a <section> to a landmark if it plays an important part in the current page. 
   
- If you’re not sure whether to use a <section>, it’s probably best to not bother with it. It’s much more important that you create a sound document outline. 
   
