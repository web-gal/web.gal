---
title: Inline elements
tags:
  - Beginner
  - Elements
  - HTML
  - HTML Elements
  - 'HTML:Element Reference'
  - Layout
  - Reference
permalink: html/inline_elements
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements'
---
HTML (**Hypertext Markup Language**) elements historically were categorized as either "block-level" elements or "inline-level" elements. Since this is a presentational characteristic it is nowadays specified by CSS in the [Flow Layout](/css/css_flow_layout). Inline elements are those which only occupy the space bounded by the tags defining the element, instead of breaking the flow of the content. In this article, we'll examine HTML inline-level elements and how they differ from [block-level elements](/html/block-level_elements).

An inline element does not start on a new line and only takes up as much width as necessary.

## Inline vs. block-level elements: a demonstration

This is most easily demonstrated with a simple example. First, some simple CSS that we'll be using:

```css
.highlight {
  background-color:#ee3;
}
```

### Inline

Let's look at the following example which demonstrates an inline element:

```html
<div>The following span is an <span class="highlight">inline element</span>;
its background has been colored to display both the beginning and end of
the inline element's influence.</div>
```

In this example, the [`div`](/html/element/div/) block-level element contains some text. Within that text is a [`span`](/html/element/span/) element, which is an inline element. Because the `<span>` element is inline, the paragraph correctly renders as a single, unbroken text flow, like this:

{{ EmbedLiveSample("Inline", 600, 80) }}

For looks, this CSS (not displayed in standard reading mode) is also used:

```css
body {
  margin: 0;
  padding: 4px;
  border: 1px solid #333;
}

.highlight {
  background-color:#ee3;
}
```

### Block-level

Now let's change that `<span>` into a block-level element, such as [`p`](/html/element/p/):

```html
<div>The following paragraph is a <p class="highlight">block-level element;</p>
its background has been colored to display both the beginning and end of
the block-level element's influence.</div>
```

The CSS (not displayed in standard reading mode) is also used:

```css
body {
  margin: 0;
  padding: 4px;
  border: 1px solid #333;
}

.highlight {
  background-color:#ee3;
}
```

Rendered using the same CSS as before, we get:

{{ EmbedLiveSample("Block-level", 600, 150) }}

See the difference? The `<p>` element totally changes the layout of the text, splitting it into three segments: the text before the `<p>`, then the `<p>`'s text, and finally the text following the `<p>`.

### Changing element levels

You can change the _visual presentation_ of an element using the CSS {{ cssxref("display") }} property. For example, by changing the value of `display` from `"inline"` to `"block"`, you can tell the browser to render the inline element in a block box rather than an inline box, and vice versa. However, doing this will not change the _category_ and the _content model_ of the element. For example, even if the `display` of the `span` element is changed to `"block"`, it still would not allow to nest a `div` element inside it.

## Conceptual differences

In brief, here are the basic conceptual differences between inline and block-level elements:

Content model
: Generally, inline elements may contain only data and other inline elements. You can't put block elements inside inline elements.

Formatting
: By default, inline elements do not force a new line to begin in the document flow. Block elements, on the other hand, typically cause a line break to occur (although, as usual, this can be changed using CSS).

## List of "inline" elements

The following elements are inline by default (although block and inline elements are no longer defined in HTML 5, use [content categories](/guide/html/content_categories) instead):

[`a`](/html/element/a/)
[`abbr`](/html/element/abbr/)
[`acronym`](/html/element/acronym/)
[`audio`](/html/element/audio/) (if it has visible controls)
[`b`](/html/element/b/)
[`bdi`](/html/element/bdi/)
[`bdo`](/html/element/bdo/)
[`big`](/html/element/big/)
[`br`](/html/element/br/)
[`button`](/html/element/button/)
[`canvas`](/html/element/canvas/)
[`cite`](/html/element/cite/)
[`code`](/html/element/code/)
[`data`](/html/element/data/)
[`datalist`](/html/element/datalist/)
[`del`](/html/element/del/)
[`dfn`](/html/element/dfn/)
[`em`](/html/element/em/)
[`embed`](/html/element/embed/)
[`i`](/html/element/i/)
[`iframe`](/html/element/iframe/)
[`img`](/html/element/img/)
[`input`](/html/element/input/)
[`ins`](/html/element/ins/)
[`kbd`](/html/element/kbd/)
[`label`](/html/element/label/)
[`map`](/html/element/map/)
[`mark`](/html/element/mark/)
[`meter`](/html/element/meter/)
[`noscript`](/html/element/noscript/)
[`object`](/html/element/object/)
[`output`](/html/element/output/)
[`picture`](/html/element/picture/)
[`progress`](/html/element/progress/)
[`q`](/html/element/q/)
[`ruby`](/html/element/ruby/)
[`s`](/html/element/s/)
[`samp`](/html/element/samp/)
[`script`](/html/element/script/)
[`select`](/html/element/select/)
[`slot`](/html/element/slot/)
[`small`](/html/element/small/)
[`span`](/html/element/span/)
[`strong`](/html/element/strong/)
[`sub`](/html/element/sub/)
[`sup`](/html/element/sup/)
[`svg`](/html/element/svg/)
[`template`](/html/element/template/)
[`textarea`](/html/element/textarea/)
[`time`](/html/element/time/)
[`u`](/html/element/u/)
[`tt`](/html/element/tt/)
[`var`](/html/element/var/)
[`video`](/html/element/video/)
[`wbr`](/html/element/wbr/)

## See also

-   [Block-level elements](/html/block-level_elements)
-   [HTML element reference](/html/element)
-   {{ cssxref("display") }}
-   [Content categories](/guide/html/content_categories)
-   [Block and Inline Layout in Normal Flow](/css/css_flow_layout/block_and_inline_layout_in_normal_flow)

{{ QuickLinksWithSubpages("/en-US/docs/Web/HTML/") }}