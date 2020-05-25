# Class 6: Semantic HTML

## Concepts

In this class, we will cover the concept of semantic HTML. Semantics is the study of meaning in a language. A semantic HTML is a code where the elements are used according to its meaning. That means that, we can write a paragraph inside a `<h1>` title tag instead of a `<p>`, but that wouldn't be semantic. The use of a good semantic is important for many reasons, including more accessibility on the page, better indexing on search engines, etc.

### Semantic Tags

Semantic tags are a category of elements that don't hold any visual or behavior effect on the page but are important for the meaning they bring for the code. Let's see some examples:

- `<header>`: As its name suggests, it defines a header area. It's an area on the page that usually contains a logo and some links to other parts of the page.

- `<nav>`: Defines a navigation menu. It must contain links to other parts of the page and are usually placed inside headers or side-bars.

- `<main>`: Describes the main portion of the page itself. It's where the content that is not generic to the page(headers, footers, sidebars) is placed.

- `<footer>`: It's an area on the bottom of the page, often containing links to social media, contact ways, terms of use, among other info.

- `<article>`: Encapsulates elements in a document that belongs to the same theme. An example of use would be containing a header and some paragraphs that belong to the same text.

- `<section>`: Represents an independent area of a page. It's a portion of elements that, if taken out of the page, would still make sense in its context itself. A blog article for example, can make sense even if not inside the blog that wrote it.

- `<aside>`: Represents additional information that can enhance the understanding of another element, but it's not required to the main content.
Examples would be bibliographies, comments, quotes, etc.

- `<figure>`: Encapsulates image content. It contains images and elements related to them, such as image descriptions.

- `<figcaption>`: It's an image caption. Represents an image description. It's placed inside a `<figure>`element.

- `<audio>`: Represents an audio element. It's used to play audio files from a web URL or a server's file. Uses the tag `<source src=''>` tag to identify the file URL. Also, it can use the `controls` attribute to display basic media controls on the screen. A sample code:

        <audio controls>
            <source src='URL'>
        </audio>

- `<embed>`: Embed external content media such as videos, audio files, gifs, etc.
