# Flexbox in CSS

**Author:** Estelle Weyl  
**Full title:** Flexbox in CSS  
**Source:** #books #api_book #readwise

- the float property can still affect box generation by influencing the display property’s computed value 
   
- As the image is a flex item, the float is ignored. Even though images and text nodes are inline-level nodes, being flex items, as long as they are not absolutely positioned, they are blockified 
   
- positive non-null float value, if there is one, is the growth factor. 
   
- positive non-null float value, if there is one, is the growth factor. When the growth factor is omitted in the shorthand, it defaults to 1. 
   
- if neither flex nor flex-grow is included, it defaults to 0. 
   
- logic would also dictate that it makes no sense to have content overflowing its flex item if the flex container has the room for all the content, even if the basis is set to zero. 
   
- When the flex property declaration explicitly sets or defaults the flex-basis to 0 px and a flex item’s growth factor is 0, the length of the main-axis of the nongrowing flex items will shrink to the smallest width the content allows, or smaller. 
   
- If all items are allowed to grow, and the flex basis for each flex item is 0%, all of the space—the entire 750 px rather than just excess space—is distributed proportionally based on the growth factors. 
   
- a flex item’s size is impacted by its content and box-model properties and can be reset via the three components of the flex property. 
   
- None of the flex properties are inherited by default 
   
- Until support is complete, flex-basis: content;
  can be easily polly-filled as it is the equivalent of declaring flex-basis: auto; width: auto;
  on that flex item, or flex-basis: auto; height: auto; 
   
- Until the content value is supported everywhere, you can replicate it by setting (or defaulting) the width/height and basis to auto. 
   
- When there are no other properties setting the main-size of the flex items (there’s no width or even min-width set on these flex items), and flex-basis: auto;
  or flex: 0 1 auto;
  is set, the flex items will only be as wide as they need to be for the content to fit 
   
- main-start because the flex container’s justify-content defaults to flex-start. 
   
- The widths are overridden by the bases. 
   
- While the declared basis can override the main-size of flex items, the size can be impacted by other properties, such as min-width, min-height, max-width, and max-height. 
   
- Remember: when the flex basis is a percent value, the main-size is relative to the parent, which is the flex container. 
   
- negative space to remove proportionally among the 3 flex items. To figure out the ratio, we divide the available width of our flex container by the sum of widths of the flex items that they would have if they couldn’t shrink 
   
- If the basis of each of the flex items is 0, the “available” space is all the space, or main-size of the parent flex container. 
   
- flex: initial;
  flex: 0 1 auto; 
   
- flex: initial
  is the equivalent of flex: 0 1 auto
  . This means the flex items’ size will be based on its own width and height properties, or based on the contents if the main-size isn’t explicitly set (set or defaulting to auto). 
   
- Flex items, by default, are grouped at main start, as flex-start is the default value of for the justify-content property. 
   
- Flex items, by default, are grouped at main start, as flex-start is the default value of for the justify-content property. This is only noticable when the combined main-size of the flex items on a flex line are smaller than the main-size of the flex container. 
   
- Setting flex: none
  is equivalent to setting flex: 0 0 auto 
   
- With flex: n
  , the basis of the flex item is 0, not auto, so setting a width will not alter the appearance 
   
- The order should only be used for visual reordering of content. Your underlying markup should always reflect the logical order of your content 
   
- Remember, when flex basis is 0, the available space of the container (not just the extra space) is distributed proportionally based on the growth factors present. 
   
- In the case of flex-basis: auto;
  , the extra space is distributed proportionally based on the flex growth factors. 
   
- We limit the width of the layout to 75 rems, again, using rems to allow the layout to remain stable if the user grows or shrinks the font size 
   
- by default flex items stretch to be height of the flex line. 
   
- With the align-items, align-self, and justify-content properties, we can now vertically and horizontally center items. 
   
- By default, the width of the inline flex container is the width of the content. 
   
- the children of flex containers are flex items, including generated content. 
   
- remember, in a single multivalue property declaration, like flex, if any value is invalid, CSS requires the entire declaration be ignored 
   
- flex: content
  last, after the fallback of flex: auto
  , so that browsers supporting content will get the content, and older browsers will fall back to auto. 
   
