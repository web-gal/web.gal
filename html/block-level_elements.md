---
title: Block-level elements
tags:
  - Beginner
  - Development
  - Guide
  - HTML
  - HTML5
  - Web
permalink: html/block-level_elements
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements'
---
HTML (**Hypertext Markup Language**) elements historically were categorized as either "block-level" elements or "inline-level" elements. Since this is a presentational characteristic it is nowadays specified by CSS in the [Flow Layout](/css/css_flow_layout). A Block-level element occupies the entire horizontal space of its parent element (container), and vertical space equal to the height of its contents, thereby creating a "block". In this article, we'll examine HTML block-level elements and how they differ from [inline-level elements](/html/inline-level_elements).

Browsers typically display the block-level element with a newline both before and after the element. You can visualize them as a stack of boxes.

A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

The following example demonstrates the block-level element's influence:

## Block-level elements

### HTML

```html
<p>This paragraph is a block-level element; its background has been colored to display the paragraph's parent element.</p>
```

### CSS

```css
p { background-color: #8ABB55; }

```

{{ EmbedLiveSample('Block-level_Example')  }}

## Usage

-   Block-level elements may appear only within a [`body`](/html/element/body/) element.

## Block-level vs. inline

There are a couple of key differences between block-level elements and inline elements:

Content model
: Generally, block-level elements may contain inline elements and (sometimes) other block-level elements. Inherent in this structural distinction is the idea that block elements create "larger" structures than inline elements.

Default formatting
: By default, block-level elements begin on new lines, but inline elements can start anywhere in a line.

The distinction of block-level vs. inline elements was used in HTML specifications up to 4.01. In HTML5, this binary distinction is replaced with a more complex set of [content categories](/html/content_categories). While the "inline" category roughly corresponds to the category of [phrasing content](/html/content_categories#phrasing_content), the "block-level" category doesn't directly correspond to any HTML5 content category, but _"block-level" and "inline" elements combined together_ correspond to the [flow content](/html/content_categories#flow_content) in HTML5. There are also additional categories, e.g. [interactive content](/guide/html/content_categories#interactive_content).

## Elements

The following is a complete list of all HTML "block-level" elements (although "block-level" is not technically defined for elements that are new in HTML5).

[`address`](/html/element/address/)
: Contact information.

[`article`](/html/element/article/)
: Article content.

[`aside`](/html/element/aside/)
: Aside content.

[`blockquote`](/html/element/blockquote/)
: Long ("block") quotation.

[`details`](/html/element/details/)
: Disclosure widget.

[`dialog`](/html/element/dialog/)
: Dialog box.

[`dd`](/html/element/dd/)
: Describes a term in a description list.

[`div`](/html/element/div/)
: Document division.

[`dl`](/html/element/dl/)
: Description list.

[`dt`](/html/element/dt/)
: Description list term.

[`fieldset`](/html/element/fieldset/)
: Field set label.

[`figcaption`](/html/element/figcaption/)
: Figure caption.

[`figure`](/html/element/figure/)
: Groups media content with a caption (see [`figcaption`](/html/element/figcaption/)).

[`footer`](/html/element/footer/)
: Section or page footer.

[`form`](/html/element/form/)
: Input form.

[`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/)
: Heading levels 1-6.

[`header`](/html/element/header/)
: Section or page header.

[`hgroup`](/html/element/hgroup/)
: Groups header information.

[`hr`](/html/element/hr/)
: Horizontal rule (dividing line).

[`li`](/html/element/li/)
: List item.

[`main`](/html/element/main/)
: Contains the central content unique to this document.

[`nav`](/html/element/nav/)
: Contains navigation links.

[`ol`](/html/element/ol/)
: Ordered list.

[`p`](/html/element/p/)
: Paragraph.

[`pre`](/html/element/pre/)
: Preformatted text.

[`section`](/html/element/section/)
: Section of a web page.

[`table`](/html/element/table/)
: Table.

[`ul`](/html/element/ul/)
: Unordered list.

## See also

-   [Inline elements](/html/inline_elements "en/HTML/Inline_elements")
-   {{ cssxref("display") }}
-   [Block and Inline Layout in Normal Flow](/css/css_flow_layout/block_and_inline_layout_in_normal_flow)

{{ QuickLinksWithSubpages("/en-US/docs/Web/HTML/") }}