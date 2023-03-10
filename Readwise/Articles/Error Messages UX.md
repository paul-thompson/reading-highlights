# Error Messages UX

**Author:** ,  
**Full title:** Error Messages UX  
**URL:** https://mailchi.mp/smashingmagazine.com/your-upcoming-ux-training-with-vitaly-friedman-final-details-1134093?e=43c418848e  
**Source:** #articles #instapaper #readwise

- Error messages can make or break the experience in situations when things go south. 
   
- 1. Never Rely On Color Alone 
   
- With error messages, we almost subconsciously think of bold red text 
   
- Due to color vision deficiencies, it’s a good idea to always complement error messages with an icon, 
   
- 2. Never Cover User’s Input 
   
- the ability to consult the error as the error is being fixed. 
   
- When a tooltip is open, users might lose sight of both the error message and the input. 
   
- We can fix it relatively easily. First of all, we avoid tooltips that open on hover, and display the tooltip text only once tapped or clicked. 
   
- 3. In Forms, Display Error Messages Above Input 
   
- Displaying error messages above input fields typically helps us avoid accessibility issues 
   
- The cost of it, though, are layout shifts: with every new error appearing dynamically, the entire form has to shift vertically 
   
- 4. In Tables, Display Error Messages Inline 
   
- One of the simpler patterns is to display the error message in the same row where the content lives 
   
- Lengthy error messages could be collapsed and expanded with an accordion. 
   
- If the same error affects multiple rows, we might want to highlight the rows that contain errors and display an error message at the very top of the page 
   
- 5. Don’t Rely on Toast Error Messages 
   
- might be uncommon for forms, but they frequently appear in tables and enterprise dashboards. 
   
- Users often don’t get a chance to fully read or understand the error message before it has disappeared, and there is no way to restore it or keep it floating. 
   
- Toast messages typically appear on the edges of the screen, and usually it’s quite far away from the erroneous input. There is a disconnect between the error message and the input 
   
- With toasts, we usually don’t have enough space to provide a detailed help using images or videos, and have to rely on plain text and links to external help pages. 
   
- Personally, I’d definitely stay away from error messages as toasts, even if they are persistent. 
   
- 6. Allow Users to Override Error Messages 
   
- Aggressive validators cost money. Especially when they come in tandem with disabled buttons that literally block users without telling them what exactly needs to be done to fix the issue 
   
