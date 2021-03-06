- **Author:** [[Rachel Andrew]]
- **Tags:** #CSS Flexbox #[[Book Highlights]]
- **Source:** #MoonReader #CSS #Layout
- ---
- ## Foreword
    - Grid, flexbox, multicolumn, flow, writing modes, shapes, object fit, alignment, sizing, viewport units—these are the tools that now make up our full toolkit
    - You hold in your hands a technical introduction to this new world, a practical tour of what’s ahead. Absorb this CSS. Play with it. Don’t just ship the same old layouts with a different underlying technology
    - Everything about web page layout just changed. —Jen Simmons
- ## Chapter 1. Where we Came From
    - Early CSS layouts were a mixture of floats and positioned elements.
    - As we became better at building floated layouts, we continued to be frustrated by the lack of full-height columns.
    - By the time Marcotte detailed his responsive design ideas on A List Apart, many websites had already opted for a fixed-width approach. Larger screens meant that liquid websites stretched too wide, and reliance on methods such as faux columns made it very hard to create flexible grids.
    - The pragmatic solution many layout frameworks propose is to put each row of the grid in a wrapper, with a clearfix applied. This contains the floats and prevents any inhabitants of the second row from hopping up into the first row’s space.
    - One aspect of being inline is that inline elements preserve white space; if they didn’t, every word in a sentence would run together,
    - A legacy method for creating a multiple-column layout exists that can address this issue; it uses table layout on items that are not HTML tables.
    - Table Layout works this way because items in a table have a relationship. This concept of creating relationships between items in the layout is important in our newer layout methods, and we will return to it later in this book.
    - The techniques demonstrated in this chapter are our stock-in-trade as front-end developers. You will need to know these techniques for some time to come in order to deal with older browsers. Yet they are all essentially hacks that merely enable layout—not a designed-for-the-job layout system.
- ## Chapter 2. Where We Are
    - These tools range from a raft of varying “best practices” in CSS architecture to pre- and postprocessors. They also extend to frameworks, and to the recent interest in design systems and pattern libraries, and working with reusable components rather than with finished pages.
    - Rather than identifying an element according to its position in the document tree, they encourage identification by class alone. This fosters reusability
    - Pre- and postprocessors also enable maneuvers that, until recently, were impossible in CSS, such as setting variables for common colors, fonts, or sizing.
    - Formal architectures and preprocessors alike have helped enable a trend in web design of breaking things down into smaller components.
    - These methods constitute quite a departure from the early days of the web, when we typically thought in “pages” rather than in components.
    - because many front-end developers rarely write CSS outside of these frameworks, they risk being unable to think outside of them.
    - Let’s make sure that in our enthusiasm to embrace new techniques, we don’t build sites that are harder for people to use.
    - The existence of old browsers is a constant source of pain for web developers, and becomes an issue when large groups of users are “stuck” on some old browser version.
    - There was a time, perhaps ten years ago now, when the real job of a front-end developer was that of a browser-bugs expert
    - Today, our browsers are far less buggy, but we still have to contend with the limited CSS layout methods of the past, plus the new innovations of recent years.
- ## Chapter 3. The New Layout
    - The element that has become a new BFC must contain everything inside it, which is why the overflow: hidden trick works to contain floats.
    - methods, you can use float to do the things that float was designed to do.
    - position: relative has another advantage for us in layout: the item that has position: relative on it establishes a new containing block. This becomes helpful when looking at the next value of position, position: absolute.
    - The fixed-position item always remains relative to the position offset from the viewport.
    - Sticky positioning A newer value of position acts like a hybrid of static and fixed positioning.
    - An item with position: sticky acts as if it is static until the document scrolls to a certain point—at which time it acts as if it is fixed.
    - Multiple-column layout is a method of splitting up a chunk of content into columns, much as you might see in a newspaper.
    - items become flex items and start to take on some initial behavior of flexbox, spacing out in a row and stretching to the height of the flex container
    - As soon as we add display: flex to the parent, the child items become flex items and start to use some initial values of flexbox.
    - To prevent this, we can allow our flex items to wrap onto multiple lines with the flex-wrap property.
    - With six items in our container, the items wrap neatly into two rows and form a nice tidy grid (Fig 3.14). Don’t be fooled! If we remove one item from the list, the grid effect disappears;
    - Distribution of space happens across the row—our final row now contains only two items.
    - Flexbox won’t try to line the items up with items in rows above or below. We describe this as one-dimensional layout.
    - We are laying out our items in either a row or a column—we can’t control both at once using flexbox.
    - To try to make flexbox behave more like a grid, we need to prevent some of the flexibility that is key to flexbox.
    - CSS Grid Layout includes a grid-gap property to space items out. This property is shorthand for grid-column-gap and grid-row-gap, which can also be specified individually.
    - You can do a lot with very little CSS.
    - it enables the creation of grid layouts in CSS. This is two-dimensional layout—laying things out as a row and a column at the same time.  
    - `fr` - it represents a fraction of the space available in the grid container.
    - This is all we need to do to get the direct child of the container to display as a grid.
    - This is essentially how any flexbox-based grid framework functions, using some variation on the above. These systems use flexbox for the ability to align things and create equal height columns, but avoid using the space distribution features in favor of calculating the widths.
    - how the flex properties of flex-grow, flex-shrink, and [[flex-basis]] work. They can give you a lot of control over how your flex items behave.
    - By preventing our flex items from growing and shrinking, then setting a width, we can make flexbox behave like a grid.
- ## Chapter 4. Alignment Control
    - We have long lacked the means to precisely align items in our layouts.
    - Alignment works on items on the cross axis (also known as the block axis in CSS, and as the column axis in the Grid specification).
    - If we change the flex-direction to column, the cross axis becomes horizontal. Aligning our items to flex-end moves the column over to the right-hand side (
    - As we did with flexbox, we can use the align-self property to override alignment on individual items.
    - The justify-items and justify-self properties do not apply in flexbox because we only have one axis, and the main axis might have multiple items on it.
    - You can use align-items and justify-content on the same flex item, which makes it easy to properly center an element
    - when we use space-between, not only do our grid gaps appear to get wider, but so do any grid areas that span more than one track
    - We’ve already seen that justify-items is not part of flexbox because of its one-dimensional nature
    - The left, right, top, and bottom properties used as offsets in absolute positioning are known as physical properties: they explain where something is physically located on the screen
    - In layout, however, the writing mode of the document matters
    - The more I work with flexbox and Grid Layout, the more I find that an understanding of alignment is key to leveraging the power of these specifications.
- ## Chapter 5. Responsive by Default
    - ^^flexbox is one-dimensional.^^
    - ^^Grid works from the outside in. We define a grid, and then put items into it^^.
    - What I want to do is to say “as many as will fit” rather than 3, as the first value of repeat(). So instead of using the integer 3, I use the keyword auto-fill (Fig 5.4).
    - auto-fill vs. auto-fit There are two possible keywords to use in repeat(): auto-fill and auto-fit. They do the same thing insofar as they add as many column tracks as will fit into the container. The difference is that if you use auto-fill but don’t have enough items to fill the tracks, the tracks remain open, so you will get space at the end where the reserved column tracks are.
    - Keeping things in proportion in Grid Layout with fr units
    - The nice thing about fraction units is that, because they define a fraction of the available space, they can be mixed with tracks set using absolute units.
    - Use auto as your [[flex-basis]] and, if you’ve set a width on the item, that width will be used as the [[flex-basis]] value. If you haven’t set a width, auto resolves to the content size.
    - I would suggest using auto as your starting point for [[flex-basis]] unless you know that you have a specific requirement.
    - Although allowing rows to auto-size is generally desirable, in some cases, setting columns to auto may result in strange sizing if something in the track affects the widths. Something to keep in mind!
    - Because auto can generally be expected to mean “content-sized,” it can be usefully employed as the maximum in minmax().
    - the flex property rather than the individual components; the order of the values is as follows: flex-grow flex-shrink [[flex-basis]]
    - If you want space to be distributed evenly, set [[flex-basis]] to 0 (Fig 5.11).
    - Set flex-grow to 0 for equal distribution of all the available space.
    - In addition to accepting a length unit, [[flex-basis]] can take the keyword values of content and auto.
    - Use auto-fill if you want to maintain the tracks; use auto-fit if you want the content to fill the container (in case there are fewer items than tracks).
    - In Grid, we have the fr unit, which is used when creating track sizes.
    - The flex shorthand The specification advises that authors use the flex shorthand rather than the individual properties of flex-grow, flex-shrink, and [[flex-basis]]
- ## Chapter 6. Source Order and Display Order
    - The default behavior of flex items is to lay themselves out in document order—the order in which they appear in the source
    - Where Grid is most like flexbox is in the grid-auto-flow property. By default, this property is set to row. Therefore, when working in a left-to-right language, items start at the top left of the grid container and position themselves into cells working to the right, then move on to the next row
    - The flexbox and Grid specifications both deal with the issue of accessibility and reordering, and both state that visual reordering does not change the logical order of the document.
    - Léonie Watson’s “Flexbox & the keyboard navigation disconnect” ([http://bkaprt.com/ncl/06-04/](http://bkaprt.com/ncl/06-04/))
    - There is a final consideration to make when developing using flexbox and Grid, and that is to avoid the temptation to flatten out markup to make it easier for elements to become flex or Grid items.
    - If we then add display: contents to the rules for the ul, the boxes generated by the ul disappear and the li items now lay out on the grid
    - display: contents. Judicious use of this value can help prevent markup flattening and allow you to make items deeper in the markup part of a flex or Grid layout.
- ## Chapter 7. Embrace the Future
    - Which browser versions are people using? Crucially, which features do those browsers support? You may be surprised, and that data can help you plan your implementation.
    - It’s also worth digging into why they are focused on the site “looking the same.” What is their underlying concern?
    - Here, you can draw parallels with responsive design. A site viewed on a phone differs from the same site viewed on the desktop, yet it still conveys the appropriate identity and visual style—tailored for the way it is being viewed.
    - Put their mind at ease by explaining how, by serving a simpler layout to older browsers, they are less likely to run into these issues.
    - Progressive Enhancement with CSS Feature Queries
    - CSS provides an answer to this question in the shape of feature queries. Feature queries are part of the CSS Conditional Rules Module
    - We start with @supports; then, inside the brackets, we add the property and value we want to test for. Note that this works for prefixed properties, too.
    - This means that a lot of progressive enhancement involves writing old CSS, then writing the new CSS afterward, exploiting the fact that later CSS will overwrite earlier CSS in your stylesheet.
    - For both flexbox and Grid, the specification explains that float and clear have no effect on a flex or Grid item.
    - Resetting widths is one of the most common things you will do when creating layouts that work for old and new browsers. Rarely will you need to write two completely different sets of CSS
    - we would quite often use display: table-cell on the item itself, without adding any other table properties. As we discovered in Chapter 1, this is one way to create full-height columns, or centering on both axes in browsers, right back to IE8.
- ## Chapter 8. Where are We Going?
    - Brand-new CSS, such as Grid and flexbox, starts life at Level 1 because it never existed in the CSS 2 or 2.1 specifications.
    - If I can leave you with any advice, it is to make room for time to play with new things. Use your personal projects or just play in an environment like CodePen or JS Bin.
