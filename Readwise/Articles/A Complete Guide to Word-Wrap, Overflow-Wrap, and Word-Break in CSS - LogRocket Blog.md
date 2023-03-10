# A Complete Guide to Word-Wrap  Overflow-Wrap  and Word-Break in CSS - LogRocket Blog

**Author:** blog.logrocket.com  
**Full title:** A Complete Guide to Word-Wrap, Overflow-Wrap, and Word-Break in CSS - LogRocket Blog  
**URL:** https://blog.logrocket.com/complete-guide-word-wrap-overflow-wrap-word-break-css/  
**Source:** #articles #instapaper #readwise

- Broken layouts sometimes happen because certain words are too long to fit in their container. 
   
- apply appropriate styling to prevent content from overflowing their container. 
   
- overflow-wrap, or word-break CSS properties to wrap or break words that would otherwise overflow their container 
   
- word-wrap 
   
- How does content wrapping occur in browsers? 
   
- Browsers and other user agents perform content wrapping at allowed breakpoints referred to as “soft wrap” opportunities 
   
- In English and most similar writing systems, soft wrap opportunities occur by default at word boundaries in the absence of hyphenation. Because words are bounded by spaces and punctuation, that is where soft wraps occur. 
   
- content wrapping is dependent on the language or writing system. The value of the lang attribute you specify on the html element is mostly used to determine which language system is in use. 
   
- What is the difference between soft wrap break and forced line break? 
   
- Any text wrap that occurs at a soft wrap opportunity is referred to as a soft wrap break. 
   
- setting the value of white-space CSS property to nowrap will disable wrapping. 
   
- Forced line breaks, on the other hand, are due to explicit line breaking controls or line breaks marking the end or start of blocks of text. 
   
- Word-wrap and overflow-wrap CSS properties 
   
- The name word-wrap is the legacy name for the overflow-wrap CSS property 
   
- browsers should treat word-wrap as a legacy name alias of the overflow-wrap property for compatibility. 
   
- overflow-wrap property:
  This property specifies whether the browser may break at otherwise disallowed points within a line to prevent overflow when an otherwise-unbreakable string is too long to fit within the line box. 
   
- the values of the overflow-wrap CSS property 
   
- Normal 
   
- Applying the value normal will make the browser use the default line breaking behavior of the system. For English and other related writing systems, line breaks will therefore occur at white spaces and hyphens: 
   
- Anywhere 
   
- Using the value anywhere will break an otherwise unbreakable string at arbitrary points between two characters 
   
- It will not insert a hyphen character even if you apply the hyphens property on the same element. 
   
- The browser will break the word only if displaying the word on its line will result in an overflow. If the word still overflows when placed on its line, it will break the word at the point where an overflow would otherwise occur. 
   
- When you use anywhere, the browser will consider the soft wrap opportunities introduced by the word break when calculating min-content intrinsic sizes 
   
- The value anywhere is not yet supported by some browsers. The image below shows the browser support according to caniuse.com. 
   
- Break-word 
   
- The value break-word is similar to anywhere in terms of functionality. 
   
- If the browser can wrap the overflowing word to its line without overflowing, that is what it will do. 
   
- if the word still overflows its container even when it is on its line, the browser will break it at the point where the overflow would otherwise occur 
   
- The difference between anywhere and break-word is apparent when calculating the min-content intrinsic sizes. With break-word, the browser doesn’t consider the soft wrap opportunities introduced by the word break when calculating min-content intrinsic sizes, but it does with anywhere. 
   
- Unfortunately, you cannot say the same about their mobile counterpart. It is, therefore, safer to use the legacy word-wrap: break-word instead of the more recent overflow-wrap: break-word. 
   
- Word-break CSS Property 
   
- use this property to break a word at the exact spot where an overflow would occur and wrap it onto the following line. 
   
- This property specifies soft wrap opportunities between letters, i.e., where it is “normal” and permissible to break lines of text. It controls what types of letters the browser can glom together to form unbreakable “words” — causing CJK characters to behave like non-CJK text or vice versa. 
   
- Break-word is also a value of the word-break CSS property, though it is deprecated 
   
- browsers still support it for legacy reasons. Specifying this property has the same effect as word-break: normal and overflow-wrap: anywhere. 
   
- Break-all 
   
- The value break-all will insert a line break at the exact point where the text would otherwise overflow for non-Chinese, non-Japanese, and non-Korean writing systems. 
   
- Using break-all will break a word between two characters at the exact point where an overflow would occur in English and other related language systems. However, it won’t apply the same behavior to Chinese, Japanese, and Korean (CJK) texts. 
   
- Creating a line break between two characters arbitrarily just for the sake of avoiding overflow might significantly change the overall meaning of the text. For CJK systems, the browser will apply line breaks at the point where such breaks are allowed. 
   
- Keep-all 
   
- the browser will not apply word breaks to CJK texts even if there is content overflow. The effect of applying keep-all value is the same as that of normal for non-CJK writing systems 
   
# A Complete Guide to Word-Wrap  Overflow-Wrap  and Word-Break in CSS - LogRocket Blog

**Author:** Joseph Mawa  
**Full title:** A Complete Guide to Word-Wrap, Overflow-Wrap, and Word-Break in CSS - LogRocket Blog  
**URL:** https://blog.logrocket.com/guide-word-wrap-overflow-wrap-word-break-css/  
**Source:** #articles #instapaper #readwise

- Content overflow can occur when you are dealing with user-generated content you have no control over, such as the comments section of a blog post. Therefore, you need to apply styling to prevent content from overflowing their container 
   
- Using word-wrap, overflow-wrap, and word-break CSS properties 
   
- How does content wrapping occur in browsers? 
   
- A browser will wrap content at a soft wrap opportunity, if one exists, to minimize content overflow. 
   
- words are bound by spaces and punctuation, that is where soft wraps occur. 
   
- soft wrap break and forced line break 
   
- What is the difference between a soft wrap break and a force line break? 
   
- Word-wrap and overflow-wrap CSS properties 
   
- According to the draft CSS3 specification, browsers should treat word-wrap as a legacy name alias of the overflow-wrap property for compatibility 
   
- If you have a white-space property on an element, you need to set its value to allow wrapping for overflow-wrap to have an effect. 
   
- Normal in CSS
  Applying the value normal will make the browser use the default line-breaking behavior of the system. For English and other related writing systems, line breaks will therefore occur at white spaces and hyphens. 
   
- Anywhere 
   
- Using the value anywhere will break an otherwise unbreakable string at arbitrary points between two characters. It will not insert a hyphen character even if you apply the hyphens property on the same element. 
   
- Don’t use overflow-wrap: anywhere in production if you intend to have higher browser support 
   
- Break-word 
   
- The value break-word is like anywhere in terms of functionality 
   
- However, if the word still overflows its container even when it is on its line, the browser will break it at the point where the overflow would otherwise occur 
   
- The difference between overflow-wrap: anywhere and overflow-wrap: break-word is in the calculation of min-content intrinsic size 
   
- With break-word, the browser doesn’t consider the soft wrap opportunities introduced by the word break when calculating min-content intrinsic sizes, but it does with anywhere. 
   
- It is, therefore, safer to use the legacy word-wrap: break-word instead of the more recent overflow-wrap: break-word. 
   
- Word-break CSS property 
   
- Word-break is another CSS property you can use to specify soft wrap opportunities between characters 
   
- Setting word-break to Normal 
   
- styling word-break: normal to a block of text that contains a word longer than its container. What you see is the browser’s usual word-breaking rules in effect. 
   
- Break-all 
   
- break-all will insert a line break at the exact point where the text would otherwise overflow for non-Chinese, non-Japanese, and non-Korean writing systems. 
   
- The browser inserted a line break at the point where an overflow would occur and wrapped the remaining text to the following line. 
   
- Using break-all will break a word between two characters at the exact point where an overflow would occur in English and other related language systems 
   
- It doesn’t apply the same behavior for CJK texts because CJK writing systems have their own rules for applying breakpoints. Creating a line break between two characters arbitrarily just for the sake of avoiding overflow might significantly change the overall meaning of the text 
   
- Keep-all 
   
- If you use the value keep-all, the browser will not apply word breaks to CJK texts even if there is content overflow 
   
- What is the difference between overflow-wrap and word-break? 
   
- overflow-wrap and word-break to manage content overflow. However, there are differences in the way the two properties handle it. 
   
- Using overflow-wrap will wrap the entire overflowing word to its line if it can fit in a single line without overflowing its container. 
   
- The overflow-wrap property is relatively new therefore has limited browser support. You can use the legacy name word-wrap instead if you want higher browser support. 
   
- Using word-wrap: break-word will wrap the overflowing word onto a new line and goes ahead to break it between two characters if it still overflows its container. 
   
- Word-break will ruthlessly break the overflowing word between two characters even if placing it on its line will negate the need for word break. 
   
- Troubleshooting CSS content overflow with Chrome DevTools 
   
- Setting the value of overflow-wrap property to anywhere or break-word on a table content won’t break an overflowing word like in the examples above. The table will overflow its container and create a horizontal scroll if necessary. 
   
- To get the table to fit within its container and overflow-wrap to work, set the value of the table-layout property to fixed and set the table width to 100% or to some fixed value 
   
- The name overflow-wrap is an alias of the legacy word-wrap property. Therefore, you can use the two interchangeably 
   
- You are better off using word-wrap instead of overflow-wrap if you want near-universal browser support 
   
- You can also use word-break to break a word between two characters if the word overflows its container. Just like overflow-wrap, you need to tread with caution when using word-break because of limitations in the browser support 
   
