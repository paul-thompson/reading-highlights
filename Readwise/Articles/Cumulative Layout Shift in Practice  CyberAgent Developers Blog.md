# Cumulative Layout Shift in Practice   CyberAgent Developers Blog

**Author:** Writer  
**Full title:** Cumulative Layout Shift in Practice | CyberAgent Developers Blog  
**URL:** https://developers.cyberagent.co.jp/blog/archives/27752/  
**Source:** #articles #instapaper #readwise

- Layout Shift Has UX Problems 
   
- Cumulative Layout Shifts is a score for measuring the UX problem. 
   
- The score requires user interaction such as scrolling down to the bottom of the page or tapping some elements to open a drawer. This means developers should collect the value from dynamic actions. 
   
- Finding Layout Shift Reasons 
   
- The first step to find the layout shift reason is to detect each layout shift with the performance observer. 
   
- Throttling to a slow network can be useful to find elements that do not have placeholder content. Blocking a response can detect elements that do not have fallback content. 
   
- Strategy For Layout Shift Improvements 
   
- You should start improvements from the most important pages for your site. 
   
- Ideally the score gets 0, but improvement from 0.3 to 0.1 has a big UX benefit. Small improvements always ensure a better quality experience for your users. 
   
- Layout Shift Patterns 
   
- Unsized media 
   
- TIPS: The predicted minimum height can also help reduce CLS value when the element height is variable. 
   
- the height might be from 260px to 350px. The maximum CLS is around 0.2 on a 740px height screen if the element has no height, but the value can be reduced to around 0.03 if you set the minimum height like min-height: 40vw in CSS 
   
- Placeholder and Fallback 
   
- You can create the skeleton while the data is being requested, and display a message with a retry button when the request has been failed. 
   
