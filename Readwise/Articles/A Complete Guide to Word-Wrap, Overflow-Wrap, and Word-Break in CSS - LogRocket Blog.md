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
   
