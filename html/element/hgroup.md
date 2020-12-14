---
title: <hgroup>
tags:
  - Element
  - Experimental
  - HTML
  - HTML sections
  - HTML5
  - Reference
  - Web
permalink: html/element/hgroup
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hgroup'
browserCompact: html.elements.hgroup
---
{{ HTMLRef }}

The **HTML `<hgroup>` element** represents a multi-level heading for a section of a document. It groups a set of `[<h1>–<h6>](/html/element/heading_elements)` elements.

{{ EmbedInteractiveExample("pages/tabbed/hgroup.html", "tabbed-standard") }}

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), heading content, palpable content. |
| Permitted content | One or more [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), and/or [`h6`](/html/element/h6/). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes).

## Usage notes

The `<hgroup>` element has been removed from the HTML5 (W3C) specification, but it still is in the WHATWG version of HTML. It is partially implemented in most browsers, though, so is unlikely to go away.  
However, given that a key purpose of the `<hgroup>` element is to affect how headings are displayed by [the outline algorithm defined in the HTML specification](/guide/html/using_html_sections_and_outlines#the_html5_outline_algorithm)—but **the HTML outline algorithm is not implemented in any browsers**—then the `<hgroup>` semantics are in practice only theoretical.  
So the HTML5 (W3C) specification provides advice on how to mark up [Subheadings, subtitles, alternative titles and taglines](https://www.w3.org/TR/html52/common-idioms-without-dedicated-elements.html#common-idioms-without-dedicated-elements) without using `<hgroup>`.

The `<hgroup>` element allows the primary heading for a document section to be grouped with any secondary headings—such as subheadings or alternative titles—to form a _multi-level_ heading.

In other words, the `<hgroup>` element prevents any of its secondary `[<h1>–<h6>](/html/element/heading_elements)` children from creating separate sections of their own in the outline—as those `[<h1>–<h6>](/html/element/heading_elements)` elements otherwise normally would if they were not children of any `<hgroup>`.

So in the abstract outline produced by the [HTML outline algorithm defined in the HTML specification](/guide/html/using_html_sections_and_outlines#the_html5_outline_algorithm), the `<hgroup>` as a whole forms a single logical heading, with the entire set of `[<h1>–<h6>](/html/element/heading_elements)` children of the `<hgroup>` going into the outline as one _multi-level_ unit, to comprise that single logical heading in the abstract outline.

To produce any (non-abstract) _rendered_ view of such an outline, some choice must be made in the design of the rendering tool about how to render `<hgroup>` headings in such a way as to convey their multi-level nature. There are a variety of ways an `<hgroup>` might be shown in a rendered outline; for example:

-   an `<hgroup>` might be shown in a rendered outline in with a colon character and space (“`:` ”) or other such punctuation after the primary heading and before the first secondary heading (and with the same or similar punctuation before any other secondary headings
-   an `<hgroup>` might be shown in a rendered outline in with the primary heading followed by parentheses around the secondary heading(s)

Consider the following HTML document:

```html
<!DOCTYPE html>
<title>HTML Standard</title>
<body>
  <hgroup id="document-title">
    <h1>HTML</h1>
    <h2>Living Standard — Last Updated 12 August 2016</h2>
  </hgroup>
  <p>Some intro to the document.</p>
  <h2>Table of contents</h2>
  <ol id=toc>...</ol>
  <h2>First section</h2>
  <p>Some intro to the first section.</p>
</body>
```

A rendered outline for that document might look like the following:

![](https://mdn.mozillademos.org/files/14599/outline-colon.png)

That is, the rendered outline might show the primary title, _HTML_, followed by a colon and space, followed by the secondary title, _Living Standard — Last Updated 12 August 2016_.

Or, the rendered outline for that document might instead look like the following:

![Rendered outline that includes an <hgroup> element, with parens around the secondary heading](https://mdn.mozillademos.org/files/14601/outline-paren.png)

That is, the rendered outline might show the primary title, _HTML_, followed by the secondary title shown in parentheses: _(Living Standard — Last Updated 12 August 2016)_.

## Examples

```html
<hgroup id="document-title">
  <h1>HTML</h1>
  <h2>Living Standard — Last Updated 12 August 2016</h2>
</hgroup>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<hgroup>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-hgroup-element) | {{ Spec2('HTML WHATWG') }} |  |

## Browser compatibility

{{ Compat("html.elements.hgroup") }}

## See also

-   Others section-related elements: [`body`](/html/element/body/), [`article`](/html/element/article/), [`section`](/html/element/section/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`nav`](/html/element/nav/), [`header`](/html/element/header/), [`footer`](/html/element/footer/), [`address`](/html/element/address/);
-   [Sections and outlines of an HTML5 document](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document "Sections and Outlines of an HTML5 document").