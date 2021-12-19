# On Buttons and Links

**Author:** abeautifulsite.net  
**Full title:** On Buttons and Links  
**URL:** https://www.abeautifulsite.net/posts/on-buttons-and-links/  
**Source:** #articles #instapaper #readwise

- Semantically Different 
   
- A <button> and a <link> are semantically different HTML elements 
   
- Emotions aside, this often leads to developers producing two separate button and link components with the same styles and logic, and consumers end up misusing them just like <button> and <a> 
   
- I propose that a custom element such as <my-button> should render the same "button" visually, but based on the presense of an optional href attribute, it will use a <button> or an <a> under the hood. 
   
- if it goes somewhere, it becomes a link. If not, it's remains a button. 
   
- Visually Different? 
   
- it falls apart in practice. Links will inevitably need to look like buttons from time to time. No, buttons and links are not semantically the same, but there are times when they need to be visually the same. 
   
- In web apps, the function of buttons and links is often blended 
   
- What Users Expect 
   
- If the user is presented with a set of actions, they don't care if you use buttons or links under the hood. 
   
- They care that it's consistent and that each control does what it's supposed to do. Remember that in all cases, each control's action is clearly inferred from its label. 
   
- I would recommend not making buttons and links look the same if you can reasonably expect the user will desire such behaviors 
   
