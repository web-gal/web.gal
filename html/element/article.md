---
title: '<article>: The Article Contents element'
tags:
  - Element
  - HTML
  - HTML sections
  - Reference
  - Web
permalink: html/element/article
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article'
browserCompact: html.elements.article
---
{{ HTMLRef }}

The **HTML `<article>` element** represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.

{{ EmbedInteractiveExample("pages/tabbed/article.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

A given document can have multiple articles in it; for example, on a blog that shows the text of each article one after another as the reader scrolls, each post would be contained in an `<article>` element, possibly with one or more `<section>`s within.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [sectioning content](/html/content_categories#sectioning_content), [palpable content](/html/content_categories#palpable_content) |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/en-US/docs/HTML/Content_categories#Flow_content). Note that an `<article>` element must not be a descendant of an [`address`](/html/element/address/) element. |
| Implicit ARIA role | `[article](/accessibility/aria/roles/article_role)` |
| Permitted ARIA roles | [`application`](https://w3c.github.io/aria/#application), [`document`](https://w3c.github.io/aria/#document), [`feed`](https://w3c.github.io/aria/#feed), [`main`](https://w3c.github.io/aria/#main), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation), [`region`](https://w3c.github.io/aria/#region) |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes "HTML/Global attributes").

## Usage notes

-   Each `<article>` should be identified, typically by including a heading ([`<h1>`-`<h6>`](/html/element/heading_elements) element) as a child of the `<article>` element.
-   When an `<article>` element is nested, the inner element represents an article related to the outer element. For example, the comments of a blog post can be `<article>` elements nested in the `<article>` representing the blog post.
-   Author information of an `<article>` element can be provided through the [`address`](/html/element/address/) element, but it doesn't apply to nested `<article>` elements.
-   The publication date and time of an `<article>` element can be described using the {{ htmlattrxref("datetime", "time") }} attribute of a [`time`](/html/element/time/) element. _Note that the {{ htmlattrxref("pubdate", "time") }} attribute of [`time`](/html/element/time/) is no longer a part of the [W3C](/glossary/w3c/) [HTML5](/glossary/html5/) standard._

## Examples

```html
<article class="film_review">
  <header>
    <h2>Jurassic Park</h2>
  </header>
  <section class="main_review">
    <p>Dinos were great!</p>
  </section>
  <section class="user_reviews">
    <article class="user_review">
      <p>Way too scary for me.</p>
      <footer>
        <p>
          Posted on
          <time datetime="2015-05-16 19:00">May 16</time>
          by Lisa.
        </p>
      </footer>
    </article>
    <article class="user_review">
      <p>I agree, dinos are my favorite.</p>
      <footer>
        <p>
          Posted on
          <time datetime="2015-05-17 19:00">May 17</time>
          by Tom.
        </p>
      </footer>
    </article>
  </section>
  <footer>
    <p>
      Posted on
      <time datetime="2015-05-15 19:00">May 15</time>
      by Staff.
    </p>
  </footer>
</article>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<article>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-article-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.1** The definition of '<article>' in that specification](https://www.w3.org/TR/html51/sections.html#the-article-element) | {{ Spec2('HTML5.1') }} |  |
| [**HTML 5** The definition of '<article>' in that specification](https://www.w3.org/TR/html52/sections.html#the-article-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.article") }}

## See also

-   Other section-related elements: [`body`](/html/element/body/), [`nav`](/html/element/nav/), [`section`](/html/element/section/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`hgroup`](/html/element/hgroup/), [`header`](/html/element/header/), [`footer`](/html/element/footer/), [`address`](/html/element/address/)
-   [Using HTML sections and outlines](/guide/html/using_html_sections_and_outlines)