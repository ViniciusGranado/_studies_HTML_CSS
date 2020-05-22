# Class 3: HTML tables

## Concepts

Tables are two-dimensional structures that are often used to present data of some sort. They contain columns, rows, and cells so that you can organize the content in the way you want, but all these elements need to be created in HTML. This is an example of a table:

| First Heading |Second heading|
|---------------|--------------|
|  Content cell | Content cell |
|  Content cell | Content cell |

Tables are created using the tag `<table>`, all content, being columns or rows, are placed inside this tag. Table rows are inserted with the tag `<tr>`, table content , with the tag `<td>`, and table headings, with the tag `<th>`. Bellow you can see an example of code to implement the table above:

    <table>
        <tr>
            <th scope='col'>First Heading</th>
            <th scope='col'>Second Heading</th>
        </tr>
        
        <tr>
            <td>Content cell</td>
            <td>Content cell</td>
        </tr>
        
        <tr>
            <td>Content cell</td>
            <td>Content cell</td>
        </tr>       
    </table>

Notice that the headings(`<th>`) have the attribute `scope`. It is used to indicate if the heading is relative to a column(`scope='col'`) or a row(`scope='row`). An example of heading of scope row would be this:

<table>
    <tr>
        <th scope='row'>First Heading</th>
        <td>Content cell</td>
        <td>Content cell</td>
    </tr>
    <tr>
        <th scope='row'>Second Heading</th>
        <td>Content cell</td>
        <td>Content cell</td>
    </tr>
</table>

And the code: 

    <table>
        <tr>
            <th scope='row'>First Heading</th>
            <td>Content cell</td>
            <td>Content cell</td>        
        </tr>
        
        <tr>
            <th scope='row'>Second Heading</th>
            <td>Content cell</td>
            <td>Content cell</td>
        </tr>
    </table>

You can also use the attributes `colspan` and `rowspan` to declare how many cells a data content will occupy:

<table>
    <tr>
        <th scope='row'>First Heading</th>
        <td>Content cell</td>
        <td>Content cell</td>
        <td>Content cell</td>
        <td rowspan='2'>Content cell</td>
    </tr>
    <tr>
        <th scope='row'>Second Heading</th>
        <td colspan='2'>Content cell</td>
        <td>Content cell</td>
    </tr>
</table>

And the code:

    <table>
        <tr>
            <th scope='row'>First Heading</th>
            <td>Content cell</td>
            <td>Content cell</td> 
            <td>Content cell</td>      
            <td rowspan='2'>Content cell</td> 
        </tr>
        <tr>
            <th scope='row'>Second Heading</th>
            <td colspan='2'>Content cell</td>
            <td>Content cell</td>
        </tr>
    </table>

To finish, we have the tags `<thead>`, `<tbody>`, and `<tfoot>`. They are responsible for telling the browser if some part of the table is a heading, a body(main content), or a foot. Lets see some example:

<table>
    <tr>
        <th scope='col'>Name</th>
        <th scope='col'>Age</th>
    </tr>
    <tr>
        <td>John Hopkins</td>
        <td>28</td>
    </tr>
    <tr>
        <td>Claire Hunter</td>
        <td>37</td>
    </tr>
    <tr>
        <td>Marie Ling</td>
        <td>19</td>
    </tr>
    <tr>
        <th scope='row'>Age average</th>
        <td>28</td>
    </tr>
</table>

Here we have a table with these 3 elements, the head, where the headings are(`Name`and `Age`), the body, where the main data is(the proper names and age), and finally, the foot, where we have the table conclusion(the heading `Age average` and the data `28`). The code then, is represented this way:

    <table>
        <tr>
            <th scope='col'>Name</th>
            <th scope='col'>Age</th>
        </tr>
        <tr>
            <td>John Hopkins</td>
            <td>28</td>
        </tr>
        <tr>
            <td>Claire Hunter</td>
            <td>37</td>
        </tr>
        <tr>
            <td>Marie Ling</td>
            <td>19</td>
        </tr>
        <tr>
            <th scope='row'>Age average</th>
            <td>28</td>
        </tr>               
    </table>

You can also stylish the table, adding borders, colors , font size, and other features using CSS, which we will be seeing on next classes.

---

## Elements saw in this class:

### Tags

- `<table>`: Indicates to the browser that te content inside of it is a table. Also indicates the beginning and the end of the table.

- `<tr>`: Indicates a table row.

- `<td>`: Indicates the content of a table cell. It's where the data is put.

- `<th>`: Indicates a heading of a row or column. It's used with the attribute `scope`.

- `<tbody>`: Indicates the heading part of a table.
- `<thead>`: Indicates the main content part of a table.
- `<tfoot>`: Indicates the final part of a table, often containing some kind of conclusion data.

### HTML Attributes

- `scope`: It's used to associate a heading cell to a row or column. It's the link between heading and data cells.

- `colspan`: Indicates how many columns a cell will occupy.

- `rowspan`: Indicates how many rows a cell will occupy.
