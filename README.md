# Introduction to CSS Grid

CSS Grid Layout is the most powerful layout system available in CSS. It brings a two-dimensional layout tool to the web, with the ability to place items in rows and columns. With this powerful layout system available in CSS, it can replace float layouts, using less, more readable, and logical HTML and CSS.

To work with CSS Grid Layout, we need to apply CSS rules both to a parent element (which becomes the Grid Container) and to that element's children (which becomes the Grid Items).

## CSS Grid Terminology

Before diving into the concepts of CSS Grid, it is important to understand the terminology as the terms are conceptually similar. Thus, to avoid confusion, it is worthwhile spending a few minutes understanding the CSS Grid Terminology.

- Grid Container

```
Parent element that holds the entire CSS Grid
```

- Grid Item

```
Element that is the direct child of the Grid Container
```

- Grid Line

```
The vertical and horizontal lines that divide the grid and separate the columns and rows.
```

![Grid Line Image](../master/img/Grid Line.png)

- Grid Track

- Grid Cell

- Grid Area

## Getting Started with CSS Grid

To use CSS Grid, we just need to define the container element as a Grid.

```
display: grid;
```

Then, we need to define the column and row sizes in the container element.

```
grid-template-rows: repeat(3, 150px);             // Creates 3 Rows

grid-template-columns: repeat(3, 150px);          // Creates 3 Columns
```

Lastly, we need to position the child elements in the Grid.

```
grid-row: 1 / 3;                                // Position elements from 1st Row to 3rd Row

grid-column: 1 / 3;                             // Position elements from 1st Column to 3rd Column
```

## CSS Grid Methods

- Base Method ()
- Line Numbers
- Line Names
- Name Grid Areas