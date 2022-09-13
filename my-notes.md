# section 3

## 32

when we set some general css in body or some general parent container for all child elements to inherit not all of the css rules are inherited. only the ones that make sense will get inherited: color, font-family... inheriting border would be impractical. the ones that get inherited are: font-family, font-size, font-weight, font-style, color, line-height, letter-spacing, text-align, text-transform, text-shadow, list-style ...

## 34 css box model

content - padding - border - margin
these are the usual suspects. new one i learned
is fill area - area that gets filled with background image/color
final width and heigh of the element includes
border, padding and content width/height

## 39. CSS Theory #4: Types of Boxes

both display: block and display: inline has their problems. so just use display: inline-block.
one problem that comes to mind quickly is that margin top and bottom doesn't work for inline elements

## 53. Flexbox terminology

we got main axis. we also got cross axis. main axis is the main one, while cross axis is the secondary one.

## 54. Spacing and Aligning items

justify-content aligns items across the main axis. by default that means horizontally
align-items aligns items across the cross axis. by default that means vertically
we have align-items which aligns all items. if we want to align
one specific item we can use align-self on that child element. the property values are the same.
we can also use order property on child element to change the
order that they are in. by default all the child elements have
value of 0 for order. if we assign a value less than 0 to one
child element, it gets in the first place. if we assign greater than 0 it changes its position
to the last place.

## 55. The flex property

flex property is a shorthand for flex-grow, flex-shrink and flex-basis. they work on flex items
not on flex container. also shorthands can be used individually
default values:
flex-grow: 0
flex-shrink: 1
flex-basis: auto

flex: flex-grow(0) flex-shrink(1) flex-basis(auto);

## WEB DESIGN RULES

## 68. web design ingredients and personalities

We can all create good looking websites just by following design rules. For that we don't need to be an artist or creative. All we need to do is to follow those rules and guidelines and follow some system!.
What are INGREDIENTS? they are parts of rules that focus on specific things in web design layout that helps for the design to be considered as good. there are 10 ingredients accoriding to Jonas and each of them has rules we need to follow
