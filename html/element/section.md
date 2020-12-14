---
title: '<section>: The Generic Section element'
tags:
  - Element
  - HTML
  - HTML sections
  - Reference
  - Section
  - Web
permalink: html/element/section
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section'
browserCompact: html.elements.section
---
{{ HTMLRef }}

The **HTML `<section>` element** represents a standalone section — which doesn't have a more specific semantic element to represent it — contained within an HTML document. Typically, but not always, sections have a heading.

{{ EmbedInteractiveExample("pages/tabbed/section.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

As an example, a navigation menu should be wrapped in a [`nav`](/html/element/nav/) element, but a list of search results and a map display and its controls don't have specific elements, and could be put inside a `<section>`.

**Note:** If the contents of the element would make sense syndicated as a standalone piece, the [`article`](/html/element/article/) element may be a better choice.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [Sectioning content](/html/content_categories#sectioning_content), palpable content. |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). Note that a `<section>` element must not be a descendant of an [`address`](/html/element/address/) element. |
| Implicit ARIA role | `[region](/accessibility/aria/roles/region_role)` if the element has an [accessible name](https://developer.paciellogroup.com/blog/2017/04/what-is-an-accessible-name/), otherwise [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`alert`](https://w3c.github.io/aria/#alert), [`alertdialog`](https://w3c.github.io/aria/#alertdialog), [`application`](https://w3c.github.io/aria/#application), [`banner`](https://w3c.github.io/aria/#banner), [`complementary`](https://w3c.github.io/aria/#complementary), [`contentinfo`](https://w3c.github.io/aria/#contentinfo), [`dialog`](https://w3c.github.io/aria/#dialog), [`document`](https://w3c.github.io/aria/#document), [`feed`](https://w3c.github.io/aria/#feed), [`log`](https://w3c.github.io/aria/#log), [`main`](https://w3c.github.io/aria/#main), [`marquee`](https://w3c.github.io/aria/#marquee), [`navigation`](https://w3c.github.io/aria/#navigation), [`none`](https://w3c.github.io/aria/#none), [`note`](https://w3c.github.io/aria/#note), [`presentation`](https://w3c.github.io/aria/#presentation), [`search`](https://w3c.github.io/aria/#search), [`status`](https://w3c.github.io/aria/#status), [`tabpanel`](https://w3c.github.io/aria/#tabpanel) |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

-   Each `<section>` should be identified, typically by including a heading ([`h1`](/html/element/h1/)-[`h6`](/html/element/h6/) element) as a child of the `<section>` element.
-   If it makes sense to separately syndicate the content of a `<section>` element, use an [`article`](/html/element/article/) element instead.
-   Do not use the `<section>` element as a generic container; this is what [`div`](/html/element/div/) is for, especially when the sectioning is only for styling purposes. A rule of thumb is that a section should logically appear in the outline of a document.

## Example

### Before

```html
<div>
  <h1>Heading</h1>
  <p>Bunch of awesome content</p>
</div>
```

### After

```html
<section>
  <h1>Heading</h1>
  <p>Bunch of awesome content</p>
</section>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<section>' in that specification](https://html.spec.whatwg.org/multipage/sections.html#the-section-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.1** The definition of '<section>' in that specification](https://www.w3.org/TR/html51/sections.html#the-section-element) | {{ Spec2('HTML5.1') }} |  |
| [**HTML 5** The definition of '<section>' in that specification](https://www.w3.org/TR/html52/sections.html#the-section-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.section") }}

## See also

-   Other section-related elements: [`body`](/html/element/body/), [`nav`](/html/element/nav/), [`article`](/html/element/article/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`hgroup`](/html/element/hgroup/), [`header`](/html/element/header/), [`footer`](/html/element/footer/), [`address`](/html/element/address/)
-   [Using HTML sections and outlines](/guide/html/using_html_sections_and_outlines)
-   [ARIA: Region role](/accessibility/aria/roles/region_role)