# What Is Cumulative Layout Shift (CLS)  and How to Optimize It   Onely Blog

**Author:** onely.com  
**Full title:** What Is Cumulative Layout Shift (CLS), and How to Optimize It | Onely Blog  
**URL:** https://www.onely.com/blog/cumulative-layout-shift/  
**Source:** #articles #instapaper #readwise

- For Google, User Experience is clearly a priority, and various Chrome team members have been talking about layout shift for years now. 
   
- Cumulative Layout Shift (CLS) is a Core Web Vitals metric calculated by summing all layout shifts that aren’t caused by user interaction. 
   
- Moreover, CLS correlates with user behavior metrics. While Google claims it doesn’t use metrics like dwell time or bounce rate for ranking purposes, other search engines, like Bing, admit using those metrics in their ranking algorithms. 
   
- How CLS is calculated 
   
- There are two factors that go into CLS: impact fraction and distance fraction 
   
- Impact Fraction 
   
- Impact region defines the area affected by the layout shift. Google identifies all affected elements and combines the original area with the shifted version, defining the impact region. 
   
- impact fraction. 
   
- To define the impact fraction you divide the area of impact region by the area of the viewport (part of the page visible on the screen without scrolling down) 
   
- area of impact region / area of viewport = impact fraction 
   
