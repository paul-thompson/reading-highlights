# Overflow Issues in CSS — Smashing Magazine

**Author:** smashingmagazine.com  
**Full title:** Overflow Issues in CSS — Smashing Magazine  
**URL:** https://www.smashingmagazine.com/2021/04/css-overflow-issues/  
**Source:** #articles #instapaper #readwise

- An overflow issue occurs when a horizontal scrollbar unintentionally appears on a web page, allowing the user to scroll horizontally 
   
- It could occur because of unexpectedly wide content or a fixed-width element that is wider than the viewport. 
   
- Scrolling to the Left or Right 
   
- The first way to discover an overflow issue is by scrolling the page horizontally 
   
- Using JavaScript to Find Elements Wider Than the Body 
   
- var docWidth = document.documentElement.offsetWidth;
  [].forEach.call(
  document.querySelectorAll('*'),
  function(el) {
  if (el.offsetWidth > docWidth) {
  console.log(el);
  }
  }
  ); 
   
- CSS Outline to the Rescue 
   
- * {
  outline: solid 1px red;
  } 
   
- [].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1 
   
- Overflow Label in Firefox 
   
- Firefox has a helpful feature that tells you which elements are causing overflow. 
   
- Deleting Page Elements 
   
- Another common way is to open the browser’s DevTools and start deleting elements one by one. Once the issue disappears, then the section you’ve just deleted is probably the cause 
   
- One of the most common causes of overflow is fixed-width elements. 
   
- Using Flexbox Without Wrapping 
   
- As useful as Flexbox is, not allowing items to wrap to a new line when no space is available is risky. 
   
- .parent {
  display: flex;
  /* Do this */
  flex-wrap: wrap;
  } 
   
- CSS Grid 
   
- use grid only when enough space is available. 
   
- @media (min-width: 400px) {
  .wrapper {
  grid-template-columns: 1fr 300px 1fr;
  }
  } 
   
- Long Words 
   
- .article-content p {
  overflow-wrap: break-word;
  } 
   
- Minimum Content Size in CSS Flexbox 
   
- “By default, flex items won’t shrink below their minimum content size (the length of the longest word or fixed-size element). To change this, set the min-width or min-height property.” 
   
- a flex item with a long word won’t shrink below its minimum content size. 
   
- .card__name {
  min-width: 0;
  overflow-wrap: break-word;
  } 
   
- Minimum Content Size in CSS Grid 
   
- As with Flexbox, we have the same concept of minimum content size with CSS Grid 
   
- .wrapper {
  display: grid;
  grid-template-columns: 248px minmax(0, 1fr);
  grid-gap: 40px;
  } 
   
- we need to use minmax() instead of 1fr. This way, the main element’s minimum content size won’t be auto. 
   
- Negative Margins 
   
- “UAs must clip the scrollable overflow area of scroll containers on the block-start and inline-start sides of the box (thereby behaving as if they had no scrollable overflow on that side).” 
   
- If positioning an element off screen is really necessary, make sure to apply overflow: hidden to the parent to avoid any overflow. 
   
- Images Without max-width 
   
- img {
  max-width: 100%;
  } 
   
- Viewport Units 
   
- Using 100vw does have a downside, which is that it can cause overflow when the scrollbar is visible 
   
- On Windows, scrollbars are always visible by default, so overflow will occur. 
   
- with the value 100vw, there is no awareness of the width of the browser’s vertical scrollbar. 
   
- function handleFullWidthSizing() {
  const scrollbarWidth = window.innerWidth - document.body.clientWidth
  document.querySelector('myElement').style.width = `calc(100vw - ${scrollbarWidth}px)`
  } 
   
- Injected Ads 
   
- Ads injected on page load can cause overflow if they’re wider than their parent. Add overflow-x: hidden to the parent element to prevent this. 
   
