## 6. building the header part 1

learned new css property which is `clip-path`. as a value it can accept some built in funcs such as `polygon()`. there is a resource that i can use to plot the point visually instead of trying to find out in my mind. resource: bennettfeely.com/clippy

## 7. building the header part 2

new discovery: img tags are inline! but they behave more like inline-block in regards to width and height. an answer that i found on SO states like this:

```js
img elements are inline, meaning that unless they are floated they will flow horizontally with text and other inline elements.

they are "block" elements in that they have a width and a height. but they behave more like "inline-block" in that respect.
```

and as Jonas states it's better to place img inside a div container and style that div to make it easier to handle imgs tags

when specifying width or height of an img, we just need to give only one (width or height) the other one is automatically figured out by the browser. so if we specify height with a certain unit, its width is figured out by the browser
