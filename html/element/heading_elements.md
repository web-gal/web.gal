---
title: '<h1>–<h6>: The HTML Section Heading elements'
tags:
  - Element
  - HTML
  - HTML sections
  - Reference
  - Web
permalink: html/element/heading_elements
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements'
browserCompact: html.elements.h1
---
{{ HTMLRef }}

The **HTML `<h1>`–`<h6>` elements** represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.

{{ EmbedInteractiveExample("pages/tabbed/h1-h6.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), heading content, palpable content. |
| Permitted content | [Phrasing content](/guide/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/guide/html/content_categories#flow_content); don't use a heading element as a child of the [`hgroup`](/html/element/hgroup/) element — it is now deprecated. |
| Implicit ARIA role | [heading](/accessibility/aria/roles/heading_role) |
| Permitted ARIA roles | [`tab`](https://w3c.github.io/aria/#tab), [`presentation`](https://w3c.github.io/aria/#presentation) or [`none`](https://w3c.github.io/aria/#none) |
| DOM interface | {{ domxref("HTMLHeadingElement") }} |

## Attributes

These elements only include the [global attributes](/html/global_attributes).

The `align` attribute is obsolete; don't use it.

## Usage notes

-   Heading information can be used by user agents to construct a table of contents for a document automatically.
-   Avoid using heading elements to resize text. Instead, use the [CSS](/glossary/css/) {{ cssxref("font-size") }} property.
-   Avoid skipping heading levels: always start from `<h1>`, followed by `<h2>` and so on.
-   Use only one `<h1>` per page or view. It should concisely describe the overall purpose of the content.
-   Using more than one `<h1>` will not result in an error, but is not considered a best practice. It is beneficial for screenreader users, and [SEO](/glossary/seo/).
-   While HTML5 allows a `<h1>` per [sectioning element](/guide/html/using_html_sections_and_outlines#section_elements_in_html5), it is not considered best practice, and may subvert the expectations of how screen reader users navigate.

## Examples

### All headings

The following code shows all the heading levels, in use.

```html
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>

```

Here is the result of this code:

{{ EmbedLiveSample('All_headings', '280', '300', '')  }}

### Example page

The following code shows a few headings with some content under them.

```html
<h1>Heading elements</h1>
<h2>Summary</h2>
<p>Some text here...</p>

<h2>Examples</h2>
<h3>Example 1</h3>
<p>Some text here...</p>

<h3>Example 2</h3>
<p>Some text here...</p>

<h2>See also</h2>
<p>Some text here...</p>

```

Here is the result of this code:

{{ EmbedLiveSample('Example_page', '280', '480', '')  }}

## Accessibility concerns

### Navigation

A common navigation technique for users of screen reading software is jumping from heading to heading to quickly determine the content of the page. Because of this, it is important to not skip one or more heading levels. Doing so may create confusion, as the person navigating this way may be left wondering where the missing heading is.

#### Don't

```html
<h1>Heading level 1</h1>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>

```

#### Do

```html
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>

```

#### Nesting

Headings may be nested as subsections to reflect the organization of the content of the page. Most screen readers can also generate an ordered list of all the headings on a page, which can help a person quickly determine the hierarchy of the content:

1.  `h1` Beetles
    1.  `h2` Etymology
    2.  `h2` Distribution and Diversity
    3.  `h2` Evolution
        1.  `h3` Late Paleozoic
        2.  `h3` Jurassic
        3.  `h3` Cretaceous
        4.  `h3` Cenozoic
    4.  `h2` External Morphology
        1.  `h3` Head
            1.  `h4` Mouthparts
        2.  `h3` Thorax
            1.  `h4` Prothorax
            2.  `h4` Pterothorax
        3.  `h3` Legs
        4.  `h3` Wings
        5.  `h3` Abdomen

When headings are nested, heading levels may be "skipped" when closing a subsection.

-   [Headings • Page Structure • WAI Web Accessibility Tutorials](https://www.w3.org/WAI/tutorials/page-structure/headings/)
-   [MDN Understanding WCAG, Guideline 1.3 explanations](/accessibility/understanding_wcag/perceivable#guideline_1.3_—_create_content_that_can_be_presented_in_different_ways)
-   [Understanding Success Criterion 1.3.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html)
-   [MDN Understanding WCAG, Guideline 2.4 explanations](/accessibility/understanding_wcag/operable#guideline_2.4_—_navigable_provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are)
-   [Understanding Success Criterion 2.4.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html)
-   [Understanding Success Criterion 2.4.6 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-descriptive.html)
-   [Understanding Success Criterion 2.4.10 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-headings.html)

### Labeling section content

Another common navigation technique for users of screen reading software is to generate a list of [sectioning content](/html/element#content_sectioning) and use it to determine the page's layout.

Sectioning content can be labeled using a combination of the `[aria-labelledby](/accessibility/aria/aria_techniques/using_the_aria-labelledby_attribute)` and {{ htmlattrxref("id") }} attributes, with the label concisely describing the purpose of the section. This technique is useful for situations where there is more than one sectioning element on the same page.

#### Example

```html
<header>
  <nav aria-labelledby="primary-navigation">
    <h2 id="primary-navigation">Primary navigation</h2>
    <!-- navigation items -->
  </nav>
</header>

<!-- page content -->

<footer>
  <nav aria-labelledby="footer-navigation">
    <h2 id="footer-navigation">Footer navigation</h2>
    <!-- navigation items -->
  </nav>
</footer>

```

In this example, screen reading technology would announce that there are two [`nav`](/html/element/nav/) sections, one called "Primary navigation" and one called "Footer navigation". If labels were not provided, the person using screen reading software may have to investigate each `nav` element's contents to determine their purpose.

-   [Using the aria-labelledby attribute](/accessibility/aria/aria_techniques/using_the_aria-labelledby_attribute)
-   [Labeling Regions • Page Structure • W3C WAI Web Accessibility Tutorials](https://www.w3.org/WAI/tutorials/page-structure/labels/#using-aria-labelledby)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '-h2' in that specification](https://html.spec.whatwg.org/multipage/sections.html#the-h1) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<h1>' in that specification](https://www.w3.org/TR/html52/sections.html#the-h1-h2-h3-h4-h5-and-h6-elements) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<h1>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.5.5) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.h1") }}

## See also

-   [`p`](/html/element/p/)
-   [`div`](/html/element/div/)
-   [`section`](/html/element/section/)