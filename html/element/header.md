---
title: <header>
tags:
  - Element
  - HTML
  - HTML sections
  - Reference
permalink: html/element/header
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header'
browserCompact: html.elements.header
---
{{ HTMLRef }}

The **HTML `<header>` element** represents introductory content, typically a group of introductory or navigational aids. It may contain some heading elements but also a logo, a search form, an author name, and other elements.

{{ EmbedInteractiveExample("pages/tabbed/header.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [palpable content](/guide/html/content_categories#palpable_content). |
| Permitted content | [Flow content](/html/content_categories#flow_content), but with no `<header>` or [`footer`](/html/element/footer/) descendant. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). Note that a `<header>` element must not be a descendant of an [`address`](/html/element/address/), [`footer`](/html/element/footer/) or another [`header`](/html/element/header/) element. |
| Implicit ARIA role | [banner](/accessibility/aria/roles/banner_role), or [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) if a descendant of an `[article](/html/element/article)`, `[aside](/html/element/aside)`, `[main](/html/element/main)`, `[nav](/html/element/nav)` or `[section](/html/element/section)` element, or an element with `role=[article](/accessibility/aria/roles/article_role)`, `[complementary](/accessibility/aria/roles/complementary_role)`, `[main](/accessibility/aria/roles/main_role)`, `[navigation](/accessibility/aria/roles/navigation_role)` or `[region](/accessibility/aria/roles/region_role)` |
| Permitted ARIA roles | [`group`](https://w3c.github.io/aria/#group), [`presentation`](https://w3c.github.io/aria/#presentation) or [`none`](https://w3c.github.io/aria/#none) |
| DOM interface | {{ domxref("HTMLElement") }} |

## Usage notes

The `<header>` element is not sectioning content and therefore does not introduce a new section in the [outline](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document). That said, a `<header>` element is intended to usually contain the surrounding section's heading (an `h1`–`h6` element), but this is **not** required.

### Historical Usage

Although the `<header>` element didn't make its way into specifications until [HTML5](/glossary/html5/), it actually existed at the very beginning of HTML. As seen in [the very first website](http://info.cern.ch/), it was originally used as the `<head>` element. At some point, it was decided to use a different name. This allowed `<header>` to be free to fill a different role later on.

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Examples

### Page Header

```html
<header>
  <h1>Main Page Title</h1>
  <img src="mdn-logo-sm.png" alt="MDN logo">
</header>

```

### Article Header

```html
<article>
  <header>
    <h2>The Planet Earth</h2>
    <p>Posted on Wednesday, <time datetime="2017-10-04">4 October 2017</time> by Jane Smith</p>
  </header>
  <p>We live on a planet that's blue and green, with so many things still unseen.</p>
  <p><a href="https://janesmith.com/the-planet-earth/">Continue reading....</a></p>
</article>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<header>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-header-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<header>' in that specification](https://www.w3.org/TR/html52/sections.html#the-header-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.header") }}

## See also

-   Other section-related elements: [`body`](/html/element/body/), [`nav`](/html/element/nav/), [`article`](/html/element/article/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`hgroup`](/html/element/hgroup/), [`footer`](/html/element/footer/), [`section`](/html/element/section/), [`address`](/html/element/address/).
-   [Using HTML sections and outlines](/guide/html/using_html_sections_and_outlines)