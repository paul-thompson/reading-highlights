# Filter UX Design Patterns - Analysis & Best Practices

**Author:** FannyV  
**Full title:** Filter UX Design Patterns - Analysis & Best Practices  
**URL:** https://pencilandpaper.io/articles//ux-pattern-analysis-enterprise-filtering/  
**Source:** #articles #instapaper #readwise

- In most enterprise applications, when filtering is needed, it’s because the data is complex and oftentimes user-generated. 
   
- When are filters used in enterprise contexts? 
   
- Filters are relevant for any screen where many of the same element can be found. This is true for data table interfaces, card-based views or any list-type page 
   
- Why filters matter 
   
- An excellent user experience for filtering means that users don’t have to ‘learn how to filter’. 
   
- Filters and their properties also double as discoverability agents that educate users about the data and what the overall system can offer. 
   
- Things to consider 
   
- What are your data made of? 
   
- you need to be very aware of your data structure. 
   
- Mirror all data points 
   
- Ex. if you show “Last modified: Date” in the entry or list-item, your users will expect to be able to filter by modified date. 
   
- Understand your user’s priorities 
   
- Which fields tend to be more looked at, modified most often? Those high-traffic properties deserve quicker access and higher visibility in your filter component. 
   
- Statuses are better prioritized in order of urgency whereas location lists are more easily scannable in alphabetical order. 
   
- Know when to stop 
   
- make sure the depth of your filters reflects the depth and volume of the data itself. 
   
- How will your system handle fetching?
  Or rather how fast can it be? 
   
- Anatomy of a filter 
   
- The identifier is the targeted property or category 
   
- The value is the specific value 
   
- The relative is the intended relation 
   
- The combo of identifier + relative + value creates a variable (a.k.a a condition or a criteria) 
   
- Selecting the relative is often not up to the user and therefore needs to be thoughtfully prescribed by the system, a.k.a you. 
   
- Toggl offers multiple preset options in their date range picker 
   
- Positioning 
   
- It can either be as a left-hand vertical sidebar, directly inline with the content at hand, or as a horizontal filter bar. The decision depends on your context and scalability needs. 
   
- Sidebar 
   
- Level of context: 🔴 Low (Global: affects the whole page)
  Scalability: 🟢 High 
   
- Inline 
   
- Level of context: 🟢 High (contextualized at the component-level)
  Scalability: 🔴 Low 
   
- Filter bar 
   
- Level of context: 🟡 Hybrid (can affect the whole page, or can affect one section at a time)
  Scalability: 🟡 Medium 
   
- When to fetch? 
   
- Live-filtering 
   
- As soon as you’re dealing with multi-select filters or more complex inputs, you might need added friction like with a secondary trigger. 
   
- Per-filter 
   
- The intermediate option here is to apply the filters one at a time 
   
- pick and choose what they need without the distraction of the results updating automatically. Then, when they’re done with that particular identifier, they can trigger the results 
   
- Batch-filtering 
   
- when all their desired filters have been input, then they would click a global ‘Apply’ button. This method works best for very heavy datasets or low-performing apps 
   
- Patterns you can use 
   
- Expandable sections 
   
- For a filter sidebar, expandable sections are a go-to. You can have a few items visible by default and provide a “Show All” mechanism. This increases discoverability and 
   
- You also have the option to place the “Apply” button at the section level, as well as at the top-level, depending on what fetching type your system can afford. 
   
- Dropdown menus 
   
- If you’re including search, make sure that as soon as the dropdown menu or expandable section has been clicked on, it’s possible for the user to start typing right away. 
   
- Table header filtering 
   
- you’re maintaining the highest level of context for your users as they see the results change directly under the input. 
   
- Additive lozenges 
   
- when we ask the system to add a variable on top of another and to exclude anything that doesn’t match the combined filter), lozenges or pills are a great way to convey that meaning. 
   
- they should be easy to remove. 
   
- Date picker 
   
- ‘Clear all’ interaction 
   
- No matter what pattern you decide fits your data and users best, don’t forget to include an easily accessible ‘Clear All’ option 
   
- Advanced filters as formulas 
   
- If your product is targeted to highly technical users, you might need to invest some time in mapping out the flow for advanced filtering. 
   
- Typically, advanced filtering is when filters become additive formulas more than simply selecting a value per identifier 
   
