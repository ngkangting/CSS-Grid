# Introduction to CSS Grid

CSS Grid Layout is a brand new module available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows. With this powerful layout system available in CSS, float layouts are no longer required to lay out web pages.

To work with CSS Grid Layout, we apply CSS rules both to a parent element (which becomes the Grid Container) and to that element's children (which become Grid Items).

## Getting Started

To use CSS Grid, we just need to define the container element as a grid.

```
display: grid;
```

Then, we need to define the column and row sizes in the container element.

```
grid-template-rows: repeat(3, 1fr);             // Creates 3 Rows

grid-template-columns: repeat(3, 1fr);          // Creates 3 Columns
```

Lastly, we need to position the child elements into the grid.

```
grid-row: 1 / 3;                                // Position elements from 1st Row to 3rd Row

grid-column: 1 / 3;                             // Position elements from 1st Column to 3rd Column
```

## CSS Grid Terminology

## CSS Grid Methods

- Base Method ()
- Line Numbers
- Line Names
- Name Grid Areas