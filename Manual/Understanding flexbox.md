- **Author:** [[Ohans Emmanuel]]
- **Tags:** #CSS Flexbox
- **Source:** #MoonReader #PDF
- ---
- ## Flex-container properties
    - there are 6 different properties the flex container can take on
    - In layman’s terms again, the main-axis’ default direction feels like “horizontal”. From left-to-right. The cross-axis feels like “vertical”. From top-to-down.
    - The Flex-direction property controls the direction in which the flexitems are laid along the main axis.  
    - The order property allows for reordering the flex items within a container. 
- ## Flex-item properties
    - It’s worth noting that flex items are re-ordered based on the number values of the order property. From lowest to highest.
    - The beauty of flex items is being “flexible”. The flex-grow and flex-shrink properties allow us play around this ‘flexibility’ even more
    - The flex-grow and flex-shrink properties control how much a flex-item should “grow” (extend) if there are extra spaces, or “shrink” if there are no “extra” spaces.
    - By default, the flex-grow property is set to 0.
    - Remember how I said the beauty of the flex-items is being “flexible”? Well, it appears you also have a control over that. 
    - The flex shorthand allows you set the flex-grow, flex-shrink and [[flex-basis]] properties all at once. 
    - Flex-grow first, then flex-shrink, and then [[flex-basis]]. The acronym, GSB may help.
    - if you set only the flex-grow and flex-shrink values, [[flex-basis]]would default to zero.
    - By default, the flex-direction property is set to row and it aligns the flex-item(s) along the main axis.
    - The flex-flow is a shorthand property which takes flex-direction and Flex-wrap values
    - The justify content property defines how flex items are laid out on the main axis.
    - It defines how flex-items are laid out on the cross axis. This is the difference between the align-items property and justify-content.
    - The default value is stretch. This will ‘stretch’ the flex-items so they fill the entire height of the flex container.
    - The align-content property is used on multi-line flex-containers
    - Like flex-containers, a couple alignment properties are also made available on all flex-items too. 
    - ```css
/*this is an absolute flex item*/
li {
	flex: 1 1; /*[[Flex-basis]] defaults to 0*/ 
}

/*this is a relative flex item*/
li {
  flex-basis: 200px; /*only [[Flex-basis]] is set*/
}
```
    - `flex: 0 1 auto; ` This is same as writing flex: default and it’s the default behavior of all flex items. 
    - The [[flex-basis]] is set to auto, which means the initial width of the flex-item will be automatically determined based on the size of the contents.
    - This says, “compute initial width automatically, but grow to fit the entire available space and shrink if necessary”
    - values e.g. 0px What really happens is, the widths of the flex items are computed based on the ratios of the flex-grow value.
    - What really happens is, the widths of the flex items are computed based on the ratios of the flex-grow value.
    - They both expand to fill up the available space, but in some proportion. 
    - Basic mathematics ratio. individual ratio / total ratio.
    - he widths are not based on the content size, but the grow values.
    - What if you wanted to change the position of a single flex-item along the cross-axis, without affecting the neighboring flex-items? The align-self property comes to the rescue. 
- ## Absolute and Relative Flex
    - **Absolute and Relative flex-items**
        - What really is the difference between an absolute and relative flex-item?
            - The major difference between these two is got to do with spacing and how they are computed.
    - The spacing within a relative flex item is computed based on it’s content size. In an absolute flex item, it is based solely on “flex” NOT content.
    - the initial widths of the flex-items are automatically computed [[flex-basis]]: auto, and then they “grow” to fit the available space flex-grow: 1.
    - When flex-items have their widths computed automatically, [[flex-basis]]: auto, it is based on the size of the content contained within the flex-item.
    - The flex-items in the example above do NOT have contents of the same size. Hence, the sizes of the flex-items would be unequal. Since the individual widths weren’t equal in the first place (it was based off of content), when the items grow, the widths also stay unequal. The flex-items in the example above are relative flex-items.
    - Do you see both flex-items have the same widths this time? 
        - The initial widths of the flex-items is zero [[flex-basis]]: 0, and then they ‘grow’ to fit the available space. When there are two or more flex-items with zero based [[flex-basis]] values, they share the spacing available based on the flex-grow values. 
        - Now the widths aren’t computed based on content size. The widths are based on the flex value specified.
    - Absolute flex-items have their widths based solely on flex, while relative flex items have their widths based on content size. 
- ## Auto Margin Alignment
    - When you use margin:auto on a flex-item, the direction (left, right or both) that has the value auto will take up any empty spaces available.
    - Now the space is distributed across both sides of the flex-item. So, is there a trade off with the cool auto-margin alignment? It appears there’s one. It can be a source of frustration if you don’t pay attention too. When you use the auto-margin alignment on a flex-item, the justify-content property no longer works on the flex-items. 
- ## Switching Flex Direction
    - When you use flex-direction: column, the main and cross axis are changed as seen below.
    - The “flex” in Flexbox means flexible. Flex-containers are by default flexible, kind off responsive. 
    - The workaround to this bug is to keep the flex-shrink value at NOT the default, 1 and also set the [[flex-basis]] property to auto. It’s like saying: “Please compute the size of the flex item automatically, but never shrink.” 
    - The workaround to this bug is to keep the flex-shrink value at 0 NOT the default, 1 and also set the [[flex-basis]] property to auto. It’s like saying: “Please compute the size of the flex item automatically, but never shrink.” With this shorthand
- ## Responsive Design
    - **Media Queries**
        - Media queries are at the heart of responsive design. They let you target specific screen sizes and specify codes to be run on the devices alone.
