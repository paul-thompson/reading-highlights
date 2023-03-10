# How the CSS Box-Sizing Property Works

**Author:** Andy Bell  
**Full title:** How the CSS Box-Sizing Property Works  
**URL:** https://andy-bell.co.uk/how-the-css-box-sizing-property-works/  
**Source:** #articles #reader #readwise

- it’s visually a circle—by proxy of [border-radius](https://css-tricks.com/almanac/properties/b/border-radius/)—but it’s still a box, as far as the browser is concerned. 
   
- When we add padding and borders to an element: by default, their **values will be combined with the computed `width` and `height`**. This is because the **`width` is applied to the content box** in the default box model. 
   
- When you toggle the `box-sizing: border-box` switch to **on**, the **content box**, **padding box** and **border box** values are effectively ingested by the content box, because the `width` property is **applied to the border box, rather than the content box**. 
   
- As you toggle the `box-sizing` value, the computed dimensions of the box model are affected. The default state combines content width, padding and border. The `border-box` value *pushes* these back into the box. 
   
- /* Reset rule */ *, *::before, *::after { box-sizing: border-box; } /* Box component */ .box { width: 100px; padding: 10px; border: 10px solid; } 
   
- Setting global styles like this is a great way to keep your CSS as simple as possible, because that’s how it’s designed to work. 
   
