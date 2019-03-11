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
The horizontal and vertical lines that divides and separate the Grid into rows and columns.
```

- **Gutter**
```
The space between the rows and columns in a Grid.
```

- **Grid Cell**
```
The space between two adjacent row and two adjacent column Grid lines. To sum up, it is a single unit of the Grid.
```

- **Grid Track**
```
The space between two adjacent Grid lines. This space can be horizontal or vertical.
```

- **Grid Row**
```
A horizontal track of a Grid.
```

- **Grid Column**
```
A vertical track of a Grid.
```

- **Grid Area**
```
A rectangular space surrounded by four Grid lines. A Grid area can contain any number of Grid cells.
```

- **Explicit Grid**
```
Grid that are explicitly defined by template rows and template columns.
```

- **Implicit Grid**
```
Grid that are not defined by template rows and template columns.
```

## CSS Grid Properties

<img src="./img/CSS Properties.PNG" width="1000px" height="500px" title="CSS Properties Image">

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
grid-row: 1 / 3;                                  // Position elements from 1st Row to 3rd Row

grid-column: 1 / 3;                               // Position elements from 1st Column to 3rd Column
```

## CSS Grid Methods

- **Base Method**

    Basic way to create a Grid is to declare **grid-template-column**. By using the property of **grid-template-column**, it helps to determine the number of items in a row for a CSS Grid. 
    
    Once the number of items in a row is specified, the Grid items will be automatically populated in the Grid container from top left to bottom right, based on the HTML source order. If the Grid item exceeds the number of rows specified, CSS Grid will automatically add rows when necessary. 

- **List Method**

    This method comprises of the **base method** and the **repeat() function**. With this method, it is easier to achieve a list sequence of items in a Grid, making it useful for responsive web design as the amount of items in a row can be determined easily for every responsive design breakpoint.

- **Dynamic List Method**

    This method is similar to the **List Method**, except that in the **Dynamic List Method**, the number of items in each row is dynamic, and may change according to the width of the view-port.

    For this method, 2 new functions of CSS Grid will be used, the **repeat() function** and the **minmax() function**, together with new values of **auto-fit**, **auto-fill** and the stretching fractional unit, **fr**.

- **Positioning with Numbers Method**

    In every CSS Grid, Grid lines are created automatically. With these Grid lines, the position of Grid items can be easily positioned in any square of the CSS Grid by defining 4 grid lines for **grid-column** and **grid-row**.

    By default, the Grid lines of CSS Grid are numbered. Thus, without making any changes, the numbers can be used to define the Starting and Ending line for a Grid item.

    ```
    grid-column: 1 / 4;                           // 1 is the Starting line and -1 is the Ending line
    grid-row: 1 / 4;                              // 1 is the Starting line and -1 is the Ending line
    ```

- **Positioning with Names Method**

    Compared to **Positioning with Numbers Method**, this method differs by giving meaningful names for each individual line. By doing so, users will have a better understanding of what each Grid line represents. Thereby, giving users an easier time defining the Starting and Ending line for a Grid item.

    To name Grid lines, the code of **grid-template-rows** and **grid-template-columns** needs to be edited. The following code shows an example of how Grid lines can be named.

    ```
    grid-template-rows: [header-start] 100px [header-end box-start] 200px [box-end];
    grid-template-columns: repeat(3, [col-start] 1fr [col-end]) 200px [grid-end];
    ```

    After naming the lines in **grid-template-rows** and **grid-template-columns**, the Grid line name can then be used to define the Starting and Ending line for a Grid item.

    ```
    grid-column: col-start 1 / grid-end;
    grid-row: header-start / footer-end;
    ```

- **Grid Areas Method**

    Areas Method is the most important grid method of all. This utilization of CSS grid is basically the main reason CSS gird was invented. It’s the easiest way to create complex grid systems.

    We start by creating the grid with the “base method”, defining the grid and the columns in each row.

    And now comes the fun part! We create a “CSS Map” according to the amount of columns we defined.

    We select a name for each area.

    To populate these areas, we connect the grid items to the grid-area names.

- **Carousel Method**

    In CSS Grid, the default flow of the items is to create a new row when there isn’t enough space in the current row, but this default behavior is changeable, and we can change it from row to column.

    ```
    grid-auto-flow: column;
    ```

    Assuming a Grid is declared with **grid-auto-flow: column;**. Without declaring any rows, all the items will be positioned in one straight long line as the number of rows have not been pre-defined.

    This method is the CSS Grid equivalent of the no-wrap property, providing a quick and simple way of creating an image carousel.