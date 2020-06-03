# Class 8: CSS grid essentials

In this class, we will see come concepts about the CSS grid.

## Concepts

To setup a grid in CSS, you need both a container element, and grid items inside the container:

        <div class='container>
            <div class='grid-item'>Content</div>
            <div class='grid-item'>Content</div>
            <div class='grid-item'>Content</div>
            <div class='grid-item'>Content</div>
        </div>

The `.container` element must have its `display` set to `grid` or `inline-grid`.
To create columns on our grid, we use the `grid-template-columns` propertie: 

        div.container{
            display: grid;
            grid-template-columns: 50% 50%;
        }

In this case, we have set two columns of 50% width, considering the total width of the container. We can use any unit to determine the width of the columns.

Similarly, we can use the `grid-template-rows` to determine the height of the rows. We also can simplify the code using the `grid-template` property: 

        div.container{
            display: grid;
            grid-template: 200px 50% 100px / 50% 50%; 
        }

All values before the slash are corresponding to the rows configuration, and the values after the slash are the columns configuration. In the case above, we had set three rows with 200px, 50%, and 100px height respectively, and two columns with 50% width each.

To determine the rows and columns sizes, CSS have a sizing unit that helps us fractionize the available space on the container. This unit is `fr`(stands for fraction). Let's see an example:

        div.container{
            display: grid;
            width: 400px;
            height: 600px;
            grid-template: 1fr 2fr 1fr / 1fr 2fr 2fr;
        }

In this case, we had set the height to 600px and divided it into 3 rows. To calculate the height of each row, the browser gets the total fractions that were requested in the CSS (4 in this case, 1fr+2fr+1fr) and divides the container in this number of fractions. We get then each fraction with 150px (600px / 4), so we have two rows with 150px, and one with 300px. The same happens to the width of the column, given the 5 fractions, and the container width of 400px, we have the fraction value of 80px, and one column with 80px, and two with 160px.

### The repeat() function

We can use the function `repeat()` to define the numbers of rows or columns:

        div.container{
            display: grid;
            grid-template: repeat(2, 1fr) / repeat(3, 1fr 2fr)
        }

The `repeat()` function receives two parameters, the first is the number of times the repetition will occur, and the second is the column or row configuration. In the case above, the row function will repeat two times, using 1fr as valor. This will create 2 rows with 1fr each. The column function will repeat 3 times, with 1fr 2fr as value, so we will have 4 columns, with 1fr 2fr 1fr 2fr of width.

### The minmax() function

The `minmax()` function tels the browser a minimum and a maximum valor for a column or a row:

        div.container{
            display: grid;
            grid-template: minmax(100px, 300px) 200px / 50% minmax(80px, 120px);
        }

In the code above, we have two rows, the first one will have its height between 100px and 300px, depending on the screen size. The second one will have a fixed height on 200px. The columns size will be fixed 50%, and between 80px and 120px, respectively. To the `minmax()` function work, the container must not have a fixed declared size.

### The grid gap

We can set a gap within the elements of the grid like this:

        div.container{
            display: grid;
            grid-gap: 20px 50px;
        }

In this case, we will have a gap of 20px between each row, and a gap of 50px between each column.

### Modifying items sizes

We can use some attributes to change how many rows or columns an element will occupy. They are: `grid-row-start`, `grid-row-end`, `grid-column-start`, and `grid-column-end`.

        div.grid-item{
            grid-row-start: 1;
            grid-row-end: 3;
            grid-column-start: 1;
            grid-column-end: 4;
        }

This item will occupy 2 rows and 3 columns. We can also use the short attributes `grid-row` and `grid-column`:

        div.grid-item{
            grid-row: 1 / 3;
            grid-column: 1 / 4;
        }

Both codes above have the exact same output. We also have the `span` keyword, that tells the browser that elements must occupy a determined number of rows or columns after the starting point:

    div.grid-item{
        grid-row: 3 / span 2;
    }

This element will start on row three, and occupy two rows of space.

To finish, we can minimize the code even more using the `grid-area` attribute:

        div.grid-item{
            grid-area: 2 / 3 / 1 / span 2;
        }

This will be the same than:

        div.grid-item{
            grid-row-start: 2;
            grid-column-start: 1;
            grid-row-end: 3;
            grid-column-end: span 2;
        }
