# Headings and Landmarks

**Author:** Rob Dodson  
**Full title:** Headings and Landmarks  
**URL:** https://web.dev/headings-and-landmarks/  
**Source:** #articles #instapaper #readwise

- Use headings to outline the page 
   
   - Note: Use h1-h6 elements to create a structural outline for your page
   
- Use h1-h6 elements to create a structural outline for your page. 
   
- The goal is to create a skeleton or scaffold of the page such that anyone navigating by headings can form a mental picture. 
   
- Don't skip heading levels 
   
- Instead of relying on the browser's default font-sizing for headings, use your own CSS, and don't skip levels. 
   
- it does not matter if visually h3's and h4's are larger than their h2 or h1 counterparts. What matters is the outline conveyed by the elements and elements' ordering. 
   
- You can use Lighthouse to check if your page skips any heading levels 
   
- Developers often skip heading levels to use the browser's default styles that closely match their design. This is considered an anti-pattern because it breaks the outline model. 
   
- Use landmarks to aid navigation 
   
- HTML5 elements such as main, nav, and aside act as landmarks, or special regions on the page to which a screen reader can jump. 
   
- Lighthouse recommends manually auditing your site to check that "HTML5 landmark elements are used to improve navigation." You can use this list of landmark elements to check your page. 
   
- Bypass repetitive content with skip links 
   
- A skip link is an offscreen anchor that is always the first focusable item in the DOM. 
   
- Because it is the first element in the DOM, it only takes a single action from assistive technology to focus it and bypass repetitive navigation. 
   
- Run the Accessibility audit (Lighthouse > Options > Accessibility) and look for the results of the Headings don't skip levels audit. 
   
- <a class="skip-link" href="#main">Skip to main</a>
  …
  <main id="main">
  [Main content]
  </main>
  .skip-link {
  position: absolute;
  top: -40px;
  left: 0;
  background: #000000;
  color: white;
  padding: 8px;
  z-index: 100;
  }
  .skip-link:focus {
  top: 0;
  } 
   
- Lighthouse can help you check if your page contains a skip link. Run the Accessibility audit again and look for the results of the The page contains a heading, skip link, or landmark region audit. 
   
