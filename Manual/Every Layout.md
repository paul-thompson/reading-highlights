# Every Layout

**Author:** Heydon Pickering & Andy Bell  
**Full title:** Debugging CSS  
**Source:** #CSS #JavaScript #Layout (Moon+ Reader)  
**URL:** https://every-layout.dev/  


- ## Boxes
    - The box model is the formula upon which layout boxes are based, and comprises content, padding, border, and margin.
    - Block elements follow ‘flow direction’, and inline elements follow writing direction.
    - Thinking typographically, it could be said that block elements are like paragraphs, and inline elements are like words.
    - When you apply display: flex or display: grid to a
    - it continues to behave like a block element, using display: block. However, it changes the way its child elements behave.
    - Formatting contexts are the basis of many of the layouts
    - different formatting contexts can be nested, to create composite layouts.
    - The web is a conduit for primarily textual information supplemented by media such as images and videos, often referred to collectively as content.
    - The web is responsive largely by default.
    - Content makes inline elements grow horizontally, and block elements grow vertically. Left to its own devices, the area of a box is determined by the area of the content it contains.
    - The lesson here is the dimensions of our elements should be largely derived from their inner content and outer context.
    - The CSS of suggestion is at the heart of algorithmic layout design.
- ## Composition
    - The purpose of Every Layout is to identify and document what each of these smaller layouts are. Together, we call them primitives.
    - intrinsically responsive. That is, it will wrap and reconfigure internally to make sure the content is visible (and well-spaced) to fit any context/screen.
    - The primitives each have a simple responsibility: “space elements vertically”, “pad elements evenly”, “separate elements horizontally”, etc. They are designed to be used in composition, as parents, children, or siblings of one another.
- ## Units
    - The notion of 1px is fuzzier than how it’s often portrayed.
    - So there are pixels, and then there are pixels of pixels.
    - false premise: that pixel perfection is both attainable and desirable.
    - there are more users who adjust their default font size in browser settings than there are users of the browsers Edge or Internet Explorer. That is: disregarding users who adjust their default font size is as impactful as disregarding whole browsers.
    - Your paragraph elements should always be 1rem, because they represent body text. You don’t need to set 1rem explicitly, because it’s the default value.
    - While the units em, rem, ch, and ex are all measurements of text, they can of course be applied to the margin, padding, and border properties (among others). It’s just that text is the basis of the web medium, and these units are a convenient and constant reminder of this fact.
    - In Every Layout, we eschew width-based @media queries
    - The em unit is to the rem unit what a container query is to a @media query.
    - As a rule of thumb, em units are better for sizing inline elements, and rem units are better for block elements.
    - The ch and ex units pertain to the (approximate) width and height of one character respectively.
    - Since measure is a question of characters per line, ch (short for character) is the only appropriate unit for this styling task.
    - line of text is extrapolated from the relationship between the rem-based font-size and ch-based max-width. By delegating an algorithm to determine this value
- ## Global and local styling
    - it’s much easier to separate branding/aesthetic from layout, and treat the two as separate concerns.
    - we’ve made the custom properties themselves globally available by attaching them to the :root (
    - ) element:
    - For consistency across the design, your sizes should probably be derived from a modular scale. See Modular scale for more.
    - The id selector, inline styles, and Shadow DOM all have drawbacks
- ## Modular scale
    - when we talk about the musicality of typesetting it is because typesetting and music share a mathematical basis.
    - In CSS, you can describe a modular scale using custom properties and the calc() function, which supports simple arithmetic.
    - Our scale variables are placed on the :root element, making them globally available. And by global, we mean truly global. Custom properties are available to JavaScript and also “pierce” Shadow DOM boundaries to affect the CSS of a shadowRoot stylesheet.
    - The custom elements used to implement Every Layout’s layouts do not use Shadow DOM because they are designed to more fully leverage ‘global’ styles
    - balanced design is seeded by simple axioms like the modular scale ratio.
- ## Axioms
    - Unless your design is founded on axioms, your output will be inconsistent and malformed.
    - In Global and local styling we set out three main tiers of styling: Universal (including inherited) styles Layout primitives Utility classes
    - Fixed widths (and heights!) are anathema to responsive design, as we established in Boxes and again here. Instead, we should deal in tolerances.
    - there is no relationship between character length and pixel width, we do not have an algorithm that can guarantee the correct maximum measure value.
    - Using ch enables us to enforce the axiom independent of font-size, allowing it to be highly pervasive and in no danger of “going wrong”
    - element particularly tends to be used as a generic container/wrapper
- ## The Stack
    - Flow elements require space (sometimes referred to as white space) to physically and conceptually separate them from the elements that come before and after them. This is the purpose of the margin property.
    - The trick is to style the context, not the individual element(s). The Stack layout primitive injects margin between elements via their common parent:
    - The key `* + *` construct is known as the owl.
    - The vertical spacing of your design should be based on your standard line-height because text dominates most pages’ layout, making one line of text a natural denominator.
    - [[CSS]] works best as an exception-based language.
    - You write far-reaching rules, then use the cascade to override these rules in special cases
    - Inherited styles have no specificity.
    - It is important the Stack is given no other purpose than to insert vertical margins.
    - In other words, it’s a question of separating concerns. Just as in computer science, in visual design it benefits your system to give each working part a dedicated and unique responsibility. The design emerges through composition.
    - it is more efficient to apply default (or ‘base’) styles and later make exceptions than to style everything like it is a special case.
    - Conveniently, global styles tend to be branding related styles — styles that affect the aesthetics but not the proportions of the subject element(s).
    - Width and height should also be inferred, either by an extrinsic value (such as the width calculated by [[flex-basis]], flex-grow, and flex-shrink working together) or by the nature of the content held inside the Box.
    - Like padding, border should be applied on all sides or none at all.
    - In cases where borders are used to separate elements, they should be applied contextually, via a parent
    - Changing the background-color often requires you to change the color to ensure the content is still legible. This can be made easier by applying color: inherit to any elements inside that Box.
    - By forcing inheritance, you can change the color—along with the background-color—in one place: on the Box itself.
- ## The Box
- ## The Center
    - The auto keyword, as its name suggests, instructs the browser to calculate the margin for you.
- ## The Cluster
    - grids are an appropriate framework for laying out content, because you want that content to align strictly to the horizontal and vertical lines that are those row and column boundaries.
    - Cluster components suit any groups of elements that differ in length and are liable to wrap. Buttons that appear together at the end of forms are ideal candidates, as well as lists of tags, keywords, or other meta information
- ## The Sidebar
    - The term intrinsic connotes introspective processes; calculations made by the layout pattern about itself.
    - Generally, we should err on the side of intrinsic sizing.
- ## The Switcher
    - it’s better to provide suggestions rather than diktats about the way the visual design is laid out
    - A declaration of width: 20rem means just that: make it 20rem wide — regardless of circumstance. But [[flex-basis]]: 20rem is more nuanced. It tells the browser to consider 20rem as an ideal or ‘target’ width. It is then free to calculate just how closely the 20rem target can be resembled given the content and available space.
    - ^^A negative [[flex-basis]] value is invalid, and dropped. Thanks to CSS’s resilent error handling this means just the [[flex-basis]] line is ignored^^, and the rest of the CSS is still applied. The erroneous negative [[flex-basis]] value is corrected to 0 and—because flex-grow is present—each element grows to take up an equal proportion of horizontal space.
    - #snippet
        ```css
		.switcher > * {
		  display: flex;
		  flex-wrap: wrap;
		}

		.switcher > * > * {
		  flex-grow: 1;
		  flex-basis: calc((30rem - 100%) * 999);
		}
		```
- ## The Cover
    - Perhaps the most robust method is to combine Flexbox’s justify-content: center (horizontal) and align-items: center (vertical). Y
    - the .centered element’s height is determined by the height of its content (implicitly, height: auto). This is something sometimes referred to as intrinsic sizing
    - Instead, we can set a min-height. This way, the element will expand vertically to accommodate the content, wherever the natural (auto) height happens to be more than the min-height
    - the provision of some vertical padding ensures the centered content does not meet the edges.
    - Only set what you need to set.
    - there should only be one
    - element per page. This is the page’s main heading to screen reader users
- ## The Grid
    - A ‘grid first’ approach to layout is only really tenable where two things are known ahead of time: The space The content
    - Each card shares ^^the same height, regardless of its content, because the default value for align-items is stretch.^^ This is fortuitous since few would expect different sized cards, or the unsightly gaps the unequal heights would create.
- ## The Frame
    - You find the aspect ratio by dividing the width of an image by its height.
    - The img element is a replaced element; it is an element replaced by the externally loaded source to which it points.
    - Making your images responsive is a matter of ensuring they don’t overflow their container. A max-width value of 100% does just that.
    - Importantly, the height—in either case—is determined by the aspect ratio. It’s the same as writing width: auto, but that explicit declaration isn’t needed by modern, compliant browsers.
    - an intrinsic ratio technique first written about as far back as 2009. The technique capitalizes on the fact that padding, even in the vertical dimension, is relative to the element’s width
