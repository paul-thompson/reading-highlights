# Overflow-Wrap   CSS-Tricks

**Author:** @impressivewebs  
**Full title:** Overflow-Wrap | CSS-Tricks  
**URL:** https://css-tricks.com/almanac/properties/o/overflow-wrap/  
**Source:** #articles #instapaper #readwise

- The overflow-wrap property in CSS allows you to specify that the browser can break a line of text inside the targeted element onto multiple lines in an otherwise unbreakable place 
   
- Values 
   
- normal: the default. The browser will break lines according to normal line breaking rules. Words or unbroken strings will not break, even if they overflow the container 
   
- break-word: words or strings of characters that are too large to fit inside their container will break in an arbitrary place to force a line break. A hyphen character will not be inserted, even if the hyphens property is used. 
   
- inherit: the targeted element must inherit the value of the overflow-wrap property defined on its immediate parent. 
   
- overflow-wrap is useful when applied to elements that contain unmoderated user-generated content (like comments sections). This can prevent long URLs and other unbroken strings of text (e.g. vandalism) from breaking a web page’s layout. 
   
- Similarities to the word-break Property 
   
- overflow-wrap is generally used to avoid problems with long strings causing broken layouts due to text flowing outside a container. 
   
- word-break specifies soft wrap opportunities between letters commonly associated with languages like Chinese, Japanese, and Korean (CJK). 
   
- word-break is best used with non-English content that requires specific word-breaking rules, and that might be interspersed with English content, while overflow-wrap should be used to avoid broken layouts due to long strings, regardless of the language used. 
   
- The Historical word-wrap Property 
   
- overflow-wrap is the standard name for its predecessor, the word-wrap property 
   
