# Introduction to CSS Grid

CSS Grid Layout is the most powerful layout system available in CSS. It brings a two-dimensional layout tool to the web, with the ability to place items in rows and columns. With this powerful layout system available in CSS, it can replace float layouts, using less, more readable, and logical HTML and CSS.

To work with CSS Grid Layout, we need to apply CSS rules both to a parent element (which becomes the Grid Container) and to that element's children (which becomes the Grid Items).

## CSS Grid Terminology

Before diving into the concepts of CSS Grid, it is important to understand the terminology as the terms are conceptually similar. Thus, to avoid confusion, it is worthwhile spending a few minutes understanding the CSS Grid Terminology.

- **Grid Container**
```
Parent element that holds the entire CSS Grid.
```

- **Grid Item**
```
Element that is the direct child of the Grid Container.
```

- **Grid Line**
```
The vertical and horizontal lines that divide the Grid and separate the columns and rows.
```

- **Gutter**
```
The space between rows and columns in a Grid.
```

- **Grid Cell**
```
The space between two adjacent row and two adjacent column Grid lines. To sum up, it is a single unit of the Grid.
```

- **Grid Row**
```
A horizontal track of a Grid.
```

- **Grid Column**
```
A vertical track of a Grid.
```

- **Grid Track**
```
The space between two adjacent Grid lines. This space can be horizontal or vertical.
```

- **Grid Area**
```
A rectangular space surrounded by four grid lines. A grid area can contain any number of grid cells.
```

- **Explicit Grid**
```
Grid that are explicitly defined by template rows and template columns.
```

- **Implicit Grid**
```
Grid that are not defined by template rows and template columns.
```

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

## CSS Grid Properties

<img src="./img/CSS Properties.PNG" width="1000px" height="500px" title="CSS Properties Image">

## CSS Grid Methods

- **Base Method**

    Basic way to create a grid is to declare **grid-template-column**. The property of **grid-template-column** helps to determine the number of items in a row. 
    
    The Grid items will automatically populate the grid container from top left to bottom right, based on the HTML source order, and will add rows as necessary. 

- **List Method**

    Using the **base method** and the **repeat()** function, it is easy to achieve a list sequence of items in a grid. 
    
    (The amount of items in a row can be determined easily for every responsive design breakpoint)

- **Dynamic List Method**

    This method is similar to the **List Method**, except that in the **Dynamic List Method**, the number of items in each row is dynamic, and may change according to the width of the view-port.

- **Positioning with Numbers Method**

- **Positioning with Names Method**

- **Grid Areas Method**

- **Carousel Method**

    In CSS Grid, the default flow of the items is to create a new row when there isn’t enough space in the current row, but this default behavior is changeable, and we can change it from row to column.

    ```
    grid-auto-flow: column;
    ```

    Assuming a Grid is declared with **grid-auto-flow: column;**. Without declaring any rows, all the items will be in one straight long line as the number of rows have not been pre-defined.

    This method is the CSS Grid equivalent of the no-wrap property, providing a quick and simple way of creating an image carousel.