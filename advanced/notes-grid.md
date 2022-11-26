# GRID

## 92. Grid basics

used css properties for grid:
display: grid;

grid-template-rows
grid-template-columns

grid-row-gap
grid-column
grid-gap

## 93. Grid basics

values for grid-template-columns/row can be %, px ... and new ones are fr ie 1fr or 2fr and the util function is repeat() ie repeat(2, 1fr) is equal to 1fr 1fr.

## 94. Grid positions

new but not new term is source order. which means what's defined in html (order of tags defined).
grid items are ordered based on source order unless specified by grid rules.

if we want to change the positions(order) of grid item we can define which column or row the item should start and end. this grid property is used on grid item. dev tools can show us the row line and column lines and their numbers.

```css
grid-row-start: 2;
grid-row-end: 3;
```

OR / OR BOTH

```css
grid-column-start: 2;
grid-column-end: 3;
```

above will change the order of the item. shorthand for these are:

```css
grid-row: 2 / 3;
grid-column: 2 / 3;
```

when we use negative value for above it means the last column/row number. this comes in handy when we have many column/rows. we don't have to count it and instead we can just type like -1 and it means the end line

we even got shorthand for above as well which is `grid-area`.
this is what its values are:
`grid-area: grid-row-start / grid-column-start / grid-row-end / grid-column-end;`

```css
grid-row-start: 2;
grid-row-end: 3;
grid-column-start: 1;
grid-column-end: 4;

grid-area: 2 / 1 / 3 / 4;
```

## 95. spanning grid items

if we want a grid item take up space from column 1 up until column 3 we can say: grid-column: 1 / 3. this means our item takes up 3 column spaces which means it starts at col 1 and spans 2 more columns ending at col 3. this can be coded in css like this grid-column: 1 / span 2. this and earlier example are the same.

## 98. naming grid lines

we can give a name to grid rows and column. we can use this technique for repeat function as well. let's start with defining columns/rows individually.

```css
    grid-template-rows: [first-row-start] 200px [first-row-end second-row-start] 300px [second-row-end]
    grid-template-columns: [first-col-start] 500 [first-col-end second-col-start] 400px [second-col-end]
```

above is how we define it. we can also give multiple names to a line inside array.

this is how we give names to grid lines:

```css
grid-template-rows:
  [f-l-start] 200px [f-l-end] [box-start] repeat(2, 1fr)
  [box-end last-l-start] 100px [last-l-end];
```

as can be seen from above example before and after repeat function we give names, but since we usually have multiple areas for repeat function we need to give numbers when we use it. below is the example for how we can use those line names

```css
grid-row: first-row-start / first-row-end;
grid-column: box-start 1 / box-end 2;
```

because we have 2 in repeat function line names are: `box-start 1`, `box-start 2` and `box-end 1`, `box-end 2`

we can also define grid areas literally ie giving names to each cell. `grid-template-areas` is used for container and `grid-area` is used for grid item.

```css
grid-template-areas:
  ". head head ."
  "box-1 box-2 box-3 side"
  "main main main side"
  "foot foot foot foot";
```

in grid-template-areas, we can use . (dot) if we want to leave an empty space

## 100. explicit and implicit grid items

if we have more items than items that can fit inside predefined grid cells, grid automatically places those items to below (to the lower side of the column, this should be logical). The reason why this adds overflown items to the end of the column(down side) instead of to the end of the row (right side) is because `grid-auto-flow` is set to row. if we set it to column then new items are added to the right side. flow also changes from left to right. and if we want to style those overflown items we can use either `grid-auto-rows` or `grid-auto-columns` depending on the `grid-auto-flow`. by the way, if we have unknown number of cells to display but the column is known we can use grid-auto-rows to give it a width value and set the number of columns using grid-template-colums.

## 101. aligning grid items to grid areas

for centering items vertically and horizontally we have `align-items` (vertically) and `justify-items` (horizontally). these properties are both grid container properties. for grid item we have `aling-self` and `justify-self`.

## 102. aligning grid items to grid track

we can use `justify-content` and `align-content` for grid as well. what it does is to align grid items along the grid track. grid tack is the space between 2 adjascent grid lines. if we have some empty cells when we use different grid properties but we don't want to leave open space we can use `dense` keyword

```css
grid-auto-flow: row dense;
```
