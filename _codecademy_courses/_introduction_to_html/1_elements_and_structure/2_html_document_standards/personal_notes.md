# Class 1: HTML document standards

## Concepts

### Basic structure of an HTML document

HTML documents are always saved in a file with an `.html` extension.

This is it's basic structure:

    <!DOCTYPE html>
    <html>
        <head>
        </head>
        
        <body>
        </body>
    </html>  

Here we have a brief description of each element: 

- `<!DOCTYPE html>`: It declares to the browser that the document is indeed an HTML document. It must always be placed on the first line of the document. The browsers by the default interpret that, if using this element, the document is written on the current version of HTML (HTML5 now in 2020).

- `<html>`: It's the primary HTML tag. Involves all other tags and content of an HTML file, and tells the browser where the document ends and starts. It's also called 'root element'.

- `<head>`: Contains the metadata of the web page. Metadata is the information that is not displayed on the page, such as description, title, information, and configuration tags. 

- `<body>`: Represent the content of the HTML document. It's where we put all content tags, such as headings, paragraphs, lists, images, etc.

### Document formatting
As HTML documents start getting bigger, they can become really difficult to read. That's why we use formatting to help us visualize the content in a better way. The two primary elements of formatting are indentation and white spaces. White spaces on an HTML document are not interpreted as content for the browser, so we can use it to help us visualize the document elements. For example: 

    <div><img src='url_here'><h1>Important title</h1><p>Some text</p></div>
    
The browser can understand this code perfectly, but it's really hard for us humans to read it, so we can format it like this:

    <div>
        <img src='url_here'>
        <h1>Important title</h1>
        <p>Some text</p>
    </div>   

This way it becomes really easier for us to interpret what's written, and identify the code elements. Note that we used both white spaces and indentation to format the code (for more details of indentation, see notes on class 1).

### Comments
Another important element of the HTML document's structure are the comments. They are text that describes what the code is doing, so the developer can better understand what's written. Comments are written like this:

    <!-- Comment here -->
    
Using the `<!-- -->` structure, the browser knows that the content inside it is a comment, and ignore it on the page exhibition. They are really useful for team working, and remembering yourself of what this old code is about. Here is a practical example:

    <!-- This is the article header -->
    <h1>How to write HTML</h1>
    <h2>A quick guide</h2>
    
    <!-- Here begins the article itself -->
    <p>HTML is a markup language........</p>
    
Comments also let you test parts of your code. By putting some portion of the code inside a comment, it will not work on code execution. This will help you isolate parts of code and find bugs for example.

## Elements saw in this class:

###Tags

- `<title>`: It's placed inside the `<head>`element. Represents the title of the page, that is displayed in the tab on the top of the browser.

- `<a>`: Stands for 'anchor'. Represents a link to an URL, whether it's an absolute HTTP path(an URL to a web page) a relative path(when the URL is a path to a directory on the server machine), or a path to the same page(using element's `id`). It's used to create links to other pages or parts of your page. The content can be a simple text or other elements such as images or buttons. Utilizes the attribute `href` for link reference(see below).

### HTML Attributes

- `href`: Stands for Hyperlink Reference. It's used on tags that need an URL to work, like the tag `<a>`. Example:

        <a href='https://github.com/ViniciusGranado'>This is a link</a>
        
It's important to say that it must contain a full URL, with the `http://` part included(unless it's a directory URL or an element's `id`).

- `target`: It defines whether a link must be opened on the same page, or another tab or window. The most common values are:

  - `_self`: It's the default value. Opens the link on the same tab that the user is in
  
  - `_blank`: Opens the link on a new tab or window. Used mostly for opening external pages.
  


