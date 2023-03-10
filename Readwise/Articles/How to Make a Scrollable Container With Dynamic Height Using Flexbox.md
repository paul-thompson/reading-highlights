# How to Make a Scrollable Container With Dynamic Height Using Flexbox

**Author:** Stephen Bunch  
**Full title:** How to Make a Scrollable Container With Dynamic Height Using Flexbox  
**URL:** https://medium.com/@stephenbunch/how-to-make-a-scrollable-container-with-dynamic-height-using-flexbox-5914a26ae336  
**Source:** #articles #instapaper #readwise

- One of the hidden features of Flexbox is the ability to make a flex child scrollable 
   
- The key is to use Flexbox for all containers that wrap the scrollable container, and give the outermost container a predefined height 
   
- There’s a special case where the min-height of flex items defaults to the content size rather than zero. According to the spec, this should only apply when overflow is set to visible. 
   
- for now, we have to explicitly set the min height to zero, or else the content will overflow its parent even though we’ve set it to scroll. This step needs to be done for every flex-item parent all the way up to the outermost flex-box. 
   
