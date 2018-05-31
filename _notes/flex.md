To use the Flexbox model, you must make a parent element a flex
container.
You do this by setting display: flex or display: inline-flex.
```
    /* Make parent element a flex container */
    ul {
        display: flex; /*or inline-flex*/ 
    }
```
As soon as you set the display property to flex, the unordered list
automatically becomes the **flex container** and the child elements (in
this case, the list elements li) become **flex items**.

## Main-axis vs Cross-axis

## The Flex Container Properties
1. flex-direction: controls the direction in which the flexitems
are laid along the main axis

2.  flex-wrap
flex-wrap property defaults to nowrap. This causes the flex container keep on accommodating more flex items on a single line.
wrap means when the available space within the
flex-container can no longer house the flex-items in their default
widths, break unto multiple lines.
wrap-reverse cause flex items break unto multiple lines, but in the reverse
direction.

3. flex-flow
flex-flow is a shorthand property which takes flex-direction and flex-wrap values
```
    ul {
        flex-flow: row wrap; /*direction row and wrap the items.*/
    }
```

4. justify-content: defines how flex items are laid out on the **main** axis.

justify-content values: flex-start || flex-end || center || space-between || space-around


5. align-items: how flex-items are laid out on the **cross** axis
align-items values: flex-start || flex-end || center || *stretch || baseline

6. align-counent: is used on multi-line flex-containers, it controls how the flex-items are aligned in a multi-line flex container.
align-counent values: flex-start || flex-end || center || *stretch || baseline





## The Flex Item Properties
1. order

2. flex-grow and flex-shrink: control how much a flex-item should "grow" (extend) if there are extra spaces, or "shrink" if there are no "extra" spaces.
By default, the flex-grow property is set to 0. By implication, the flexitem does NOT grow to fit the entire space available.
By default, the shrink property is set to 1. Which means the flexshrink switch is also turned on!

3. flex-basis : specifies the initial size of a flex-item. Before the flex-grow or flex-shrink properties adjust it’s size to fit the container or not.
The default value is flex-basis: auto. This means if you increased the content in the flex-item, it
automatically resizes to fit.
Flex-basis can take on any values you’d use on the normal width property. That is, percentages|| ems || rems || pixels etc

4. flex shorthand: flex-grow, flex-shrink, flex-basis
    1. flex: 0 1 auto (same as flex: default)
        The flex items don’t grow. The width is computed automatically, and they shrink upon resizing the browser if necessary.
    2. flex: 0 0 auto (same as flex: none)
        the width of flex items are computed automatically BUT the flex item does NOT grow or shrink
    3. flex: 1 1 auto
    
    4. flex: positive nmber

    5. align-self: affect a particular targeted item.