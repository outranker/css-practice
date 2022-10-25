# NOTES for Advanced css course on udemy

## SECTION 2 Setting up Natours project and first steps

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

## 10. building complex animation on button part 2

new css property learned. `animation-fill-mode`. the value for this property is which we used `backwards`. what this css prop does is to determine what before and after state is for the animation execution

## SECTION 3 How css works. a look behind the scenes

## 12. three pillars of writing good html and css

**1. Responsive Design** is standard already. it inlcudes fluid layouts, media queries, responsive images, correct units and desktop-first vs mobile-first aspects. i believe they are crystal clear for me as i have already learned about them in intermediate css course by Jonas

**2. Maintainable and scalable code** is more for Dev than end user. it includes clean code, easy-to understand code, code growth, reusable code, how to organise files, how to name classes, how to structure html aspects

**2. Web Performance** means making the website to load faster and smaller size. to achieve this we can also do below things: make fewer http requests, less code, compressing code, using css preprocessor, fewer images or smaller size images, compressing images
