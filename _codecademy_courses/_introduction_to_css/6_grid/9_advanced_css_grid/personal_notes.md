# Class 9: Advanced CSS grid

In the previous lesson, we san the basics of how to build a grind on CSS. Now, we will see some additional properties to enhance our layouts.

## Concepts

### The `grid-template-areas` property

We can use this property to name the areas of the grid. Considering this code:

        HTML:
        <div class="container">
            <header></header>
            <nav></nav>
            <section class="info"></section>
            <section class="services"></section>
            <footer></footer>
        </div>

        CSS:
        .container{
            grid-template: 150px 200px 600px 200px / 200px 400px;
        }

Here we have a container with five elements inside, and divided into four rows and two columns. Now let's use the `grid-template-areas` property:

        .container{
            grid-template: 150px 200px 600px 200px / 200px 400px;
            grid-template-areas: "header header"
                                 "nav nav"
                                 "info services"
                                 "footer footer"
        }

By doing this, each cell of the grid is now named, the two columns of the first-row named "header", the second-row "nav", the third-row "info" and "services", and the last row "footer". Now we can assign each element to the names areas:

        header{
            grid-area: "header"
        }
        nav{
            grid-area: "nav"
        }
        .info{
            grid-area: "info"
        }
        .services{
            grid-area: "services"
        }
        footer{
            grid-area: "footer"
        }

Now each element will occupy the area with the name that they were assigned. Note that the `<header>` element will occupy the two columns named `"header"`, the `<nav>` will occupy the `"nav"` area, the `.info` and `.services` will occupy one cell each on the third row, and the `<footer>`, the last row.

### The `justify-items` and `justify-content` properties

By default, the element size will be adjusted to fill the cell, but if we set its width or height to a smaller size than the cell, there will be a blank space, and the element will be positioned to the left side of the cell. We can change this behavior using the `justify-items` property. The most common values are `start`, `center`, `end`, and `stretch`. We can also use the `justify-content` to position the entire grid inside its parent element.

### `align-items` and `align-content`

Similarly, we can use the `align-items` and `align-content` properties to align the elements on the grid.

### `justify-self` and `align-self`

These properties work just like the previous ones but apply the value to a single element.

### The implicit grid

The concepts we've been seeing this far works great when we know how much content will be inside the grid, but if we don't know this information, we can use the concept of "Implicit Grid", which is an algorithm that calculates how many rows or columns will be needed to fit all elements. To this, we can use the `grid-auto-rows` and `grid-auto-columns` to say to the CSS to use the implicit grid. We can also use the `grid-auto-flow` to determine if the flow of the implicit grid will be based on new rows(default), new columns, or an auto-completion.
