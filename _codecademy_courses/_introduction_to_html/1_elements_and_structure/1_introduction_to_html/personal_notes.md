# Class 1: Elements and structures

## Concepts
Html is a markup language and is considered the skeleton of the web. It stands for HyperText Markup Language. HiperText is a text that provides access to another text through links. These are the links we see on the web every day. 

Content in HTML is structured in tags. Tags define the type of content inside them. They are represented this way: 

    <tag>Content here</tag>` 

We have an opening tag (`<tag>`) and a closing tag (`</tag>`). The only visual difference between them is the slash on the closing tag. An 'element' is the whole structure, opening tag, content, and closing tag.

- `<tag>Content here</tag>` This is an element.
- `<tag>` This is an opening tag.
- `Content here` This is the content.
- `</tag>` This is n closing tag.
 
### HTML structure
HTML is structured in a tree form, with elements inside each other. Elements inside others are called child of the outside element, called parent. Example:

    <html>
        <body>
            <p>This is a paragraph</p>
        </body>
    </html>

In this case, `p` is a child element of its parent `body`. In the same way, `body` is considered child of parent element `html`, and `p` is considered grand-child of `html` element.

### Indentation
You can notice that in the previous code, some lines were wrote in a different alignment than others. This is called indentation.

    <html>
    ****<body>
    ********<h1>This is a heading</h1>
    ********<p>This is a paragraph</p>
    ****</body>
    </html>
    
    The indentation here is represented by the * characters.

The indentation helps the developer to understand and visualize the code better. The alignment represents which elements are inside another. In this example, we can visualize that the `body` element is inside `html`, and `h1` is inside `body`, but `p` is in the same level of `h1`, so they have the same parent. 

### HTML attributes
HTML attributes provide information or functions to a tag.
They are represented this way:

    <tag attribute_name="attribute_value">Content here</tag>
   
- `<tag>` is the proper tag.
- `attribute_name` is the name of the attribute.
- `"attribute_value"` is the attribute value.

A real case:

        <p class="first_paragraph">This is a paragraph</p>
        
In this case, `p` is the tag, `class` is the attribute, and `first_paragraph` is the attribute value.       
There are innumerous attributes, some of them are `class`, `id`, and `src`. You can see their description in the section below.

## Elements saw in this class:

###Tags
- `<body>`: Defines the content part of the code. Everything in an HTML document that is content related is put inside this tag.
 
- `<h1>`-`<h6>`: They are heading tags, and defines a title. They are used in order of importance, `<h1>` being a main title, and `<h2>` being a subtitle of `<h1>`. Example:

        <h1>Apple Pie</h1> - This is a title
        <h2>An easy recipe for your weekend</h2> - This is a subtitle
        
    
- `<p>`: Defines a paragraph. Example:

        <p>Apple pie is a delicious recipe.</p> - This is a paragraph
        <p>See bellow an easy way to do it:</p> - This is another paragraph
   
- `<div>`: Short for 'division'. It's used to group HTML elements. There's no semantic value, and it's used mostly for styling purposes. Work like a block of content.

- `<span>`: It's similar to `<div>`, but groups a line of content, instead of a block. It's also used for styling purposes, but mostly for text content only.

- `<em>`: Short from 'emphasis'. It's used to emphasize a word or text portion. Its importance is more related to accessibility purposes, as it emphasizes text read by Visually Impaired tools.

- `<strong>`: Indicates important text. Its use is similar to `<em>`, being more related to accessibility purposes.

- `<br>`: Defines a break of line. More used on texts where the line break is an important part of the text itself, like poems.

- `<img>`: Defines an image on the document. It's used with `src` and `alt` attributes(see below). It doesn't require a closing tag.

- `<video>`: Define a video on the document. Also use the `<src>` attribute, along with `width`, `height`, and `controls`. Requires a closing tag. If content is put inside tags, it'll be displayed if the browser is unable to load the video. 

- `<ul>`: Unordered list. Defines a list where the elements don't have an important order. An example would be a list of ingredients on a recipe. The order of the presentation of the ingredients doesn't matter to the actual recipe. Examples bellow.

 


- `<ol>`: Ordered list. Defines a list where the element's order **does** matter. An example would be the steps of a recipe. If done in a wrong order, the recipe doesn't work. Examples bellow.

- `<li>`: List item. Defines items of a list, both ordered and unordered.

Examples on lists:

    <h1>Lemonade<h1> - This is a title
    <h2>Ingredients> - This is a subtitle
    
    <ul>  - This is an unordered list. The order of the content doesn't matter.
        <li>1/2 cup of sugar</li> 
        <li>1 cup of water</li>
        <li>1 cup lemon juice</li>
     </ul>
            
    <h2>Method</h2> - This is another subtitle
    
    <ol> - This is an ordered list. The order of the content does matter.
        <li>Place the water and the lemon juice on a glass pitcher</li> 
        <li>Mix with the sugar</li>
        <li>Refrigerate for two hours.</li>
    </ol>

### HTML Attributes

- `id` and `class`: Are identity attributes. They are used to identify tags for styling purposes.

- `src`: Defines a URL for some content. Used to implement images, videos, or external files.

- `alt`: Define alternative information for an image. Used for image descriptions for visually impaired tools. Even though it's using is not mandatory, it's considered good practice. 

- `width` and `height`: Defines the width and height of a video player.

- `controls`: Declares to the browser that it must show basic controls to a video player(play, pause, and stop).
