# Trillo project notes

## 68. overview of flexbox

how flex items are laid out is determined by main axis and cross axis. these terms will come up a lot

we got many css attributes for flex container and flex items. most of it I already know. but below is a small review of the ones that i might have forgotten or rarely used?

- Container properties

  `flex-wrap`. default value is nowrap. this means if there is no space for items they won't take up new row/column. if it's wrap they will form new row/column and take the given width.
  `justify-content` is for axis cross. `align-items` is for cross axis. but how about `align-content`? it's also used for cross axis since in its name it has the word 'align'. but it only works when there is more than 1 row and it controls how items are aligned along the cross axis.

- Item properties
  flex item properties help us define css for each item in the flex container. it also helps to override the values given by the container.
  `align-self` is self explanatory so is `order` but need to test them.
  `flex-grow`, `flex-shrink`, `flex-basis` helps to decide on the width of an item. with `flex-grow` and `flex-shrink` we decide how much an item grows and shrinks. 0 means no growing or shrinking while 1 means yes growing or shrinking. and with `flex-basis` we can decide how much an initial width of an item should be. auto means whatever its parent gave it. instead of using all 3 of them (`flex-grow`, `flex-shrink`, `flex-basis`) we use shorthand property which is like: `flex: 0 1 auto`.

initial value of `align-items` is `stretch`. `baseline` value aligns the content on the same line. this comes in handy when items are not at the same height.

default value of `order` property is 0. and by default, flex items are laid out in the source order.

`flex-grow` is the ability of an element to grow and we specifiy an integer as a value. defeault value is 0 which means they will take up space as much as the content needs and not any more than that. if we give different numbers to all child elements the space they take up is determined by the ratio of their `flex-grow` value to total sum of all the values.
`flex-basis` sets the width of a flex item. default value is auto.
`flex-shrink` default value is 1. which means it will shrink
`align-content` helps to align the content when we have too much heigh or too much width.
