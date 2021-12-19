# How to Fix Issues With CSS Position Sticky Not Working

**Author:** Daniyal Hamid  
**Full title:** How to Fix Issues With CSS Position Sticky Not Working?  
**URL:** https://www.designcise.com/web/tutorial/how-to-fix-issues-with-css-position-sticky-not-working  
**Source:** #articles #instapaper #readwise

- Checking if a Threshold Has Been Specified 
   
- A sticky element requires a threshold to be specified by setting value (other than auto) for at least one of the top, right, bottom, or left properties. 
   
- .sticky {
  position: sticky;
  top: 0;
  } 
   
- Checking Vendor Prefix for Safari 
   
- .sticky {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  } 
   
- Checking if an Ancestor Element Has overflow Property Set 
   
- If any parent/ancestor of the sticky element has any of the following overflow properties set, position: sticky won't work:
  overflow: hidden
  overflow: scroll
  overflow: auto 
   
- let parent = document.querySelector('.sticky').parentElement;
  while (parent) {
  const hasOverflow = getComputedStyle(parent).overflow;
  if (hasOverflow !== 'visible') {
  console.log(hasOverflow, parent);
  }
  parent = parent.parentElement;
  } 
   
- How to Make position: sticky Work With the overflow Property? 
   
- specifying a height on the overflowing container, you should be able to make position: sticky work whilst having the container element have the overflow property set. 
   
- Checking if height Property Is Not Set on Parent 
   
- If the parent element has no height set then the sticky element won't have any area to stick to when scrolling. 
   
- the sticky element is meant to stick/scroll within the height of a container. 
   
- Checking if a Parent Element Is a Flexbox 
   
- If the Sticky Element Has align-self: auto Set 
   
- align-items: stretch set, then it means the height of the sticky element would stretch to fill the entire available space. This would leave no room for the sticky element to scroll within the parent. 
   
- If the Sticky Element Has align-self: stretch Set 
   
- In this case, the sticky element would stretch to the height of the parent, and would not have any area to scroll within 
   
- You could simply set the value of the align-self property to align-self: flex-start. This would put the sticky element at the start and won't stretch it. 
   
