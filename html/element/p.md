---
title: '<p>: The Paragraph element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - Reference
  - Web
permalink: html/element/p
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p'
browserCompact: html.elements.p
---
{{ HTMLRef }}

The **HTML `<p>` element** represents a paragraph. Paragraphs are usually represented in visual media as blocks of text separated from adjacent blocks by blank lines and/or first-line indentation, but HTML paragraphs can be any structural grouping of related content, such as images or form fields.

Paragraphs are [block-level elements](/html/block-level_elements), and notably will automatically close if another block-level element is parsed before the closing `</p>` tag. See “Tag omission” below.

{{ EmbedInteractiveExample("pages/tabbed/p.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | The start tag is required. The end tag may be omitted if the [`p`](/html/element/p/) element is immediately followed by an [`address`](/html/element/address/), [`article`](/html/element/article/), [`aside`](/html/element/aside/), [`blockquote`](/html/element/blockquote/), [`div`](/html/element/div/), [`dl`](/html/element/dl/), [`fieldset`](/html/element/fieldset/), [`footer`](/html/element/footer/), [`form`](/html/element/form/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`header`](/html/element/header/), [`hr`](/html/element/hr/), [`menu`](/html/element/menu/), [`nav`](/html/element/nav/), [`ol`](/html/element/ol/), [`pre`](/html/element/pre/), [`section`](/html/element/section/), [`table`](/html/element/table/), [`ul`](/html/element/ul/) or another [`p`](/html/element/p/) element, or if there is no more content in the parent element and the parent element is not an [`a`](/html/element/a/) element. |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLParagraphElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

**Note:** The `align` attribute on `<p>` tags is obsolete and shouldn't be used.

## Example

### HTML

```html
<p>This is the first paragraph of text.
  This is the first paragraph of text.
  This is the first paragraph of text.
  This is the first paragraph of text.</p>
<p>This is the second paragraph.
  This is the second paragraph.
  This is the second paragraph.
  This is the second paragraph.</p>

```

### Result

{{ EmbedLiveSample('Example') }}

## Styling paragraphs

By default, browsers separate paragraphs with a single blank line. Alternate separation methods, such as first-line indentation, can be achieved with [CSS](/glossary/css/):

### HTML

```html
<p>Separating paragraphs with blank lines is easiest
for readers to scan, but they can also be separated
by indenting their first lines. This is often used
to take up less space, such as to save paper in print.</p>

<p>Writing that is intended to be edited, such as school
papers and rough drafts, uses both blank lines and
indentation for separation. In finished works, combining
both is considered redundant and amateurish.</p>

<p>In very old writing, paragraphs were separated with a
special character: ¶, the <i>pilcrow</i>. Nowadays, this
is considered claustrophobic and hard to read.</p>

<p>How hard to read? See for yourself:
  <button data-toggle-text="Oh no! Switch back!">Use pilcrow for paragraphs</button>
</p>

```

### CSS

```css
p {
  margin: 0;
  text-indent: 3ch;
}

p.pilcrow {
   text-indent: 0;
   display: inline;
}
p.pilcrow + p.pilcrow::before {
  content: " ¶ ";
}
```

### JavaScript

```js
document.querySelector('button').addEventListener('click', function (event) {
  document.querySelectorAll('p').forEach(function (paragraph) {
    paragraph.classList.toggle('pilcrow');
  });
  var newButtonText = event.target.dataset.toggleText;
  var oldText = event.target.innerText;
  event.target.innerText = newButtonText;
  event.target.dataset.toggleText = oldText;
});
```

### Result

{{ EmbedLiveSample('Styling_paragraphs') }}

## Accessibility concerns

Breaking up content into paragraphs helps make a page more accessible. Screen-readers and other assistive technology provide shortcuts to let their users skip to the next or previous paragraph, letting them skim content like how white space lets visual users skip around.

Using empty `<p>` elements to add space between paragraphs is problematic for people who navigate with screen-reading technology. Screen readers may announce the paragraph's presence, but not any content contained within it — because there is none. This can confuse and frustrate the person using the screen reader.

If extra space is desired, use [CSS](/glossary/css/) properties like {{ cssxref("margin") }} to create the effect:

```css
p {
  margin-bottom: 2em; // increase white space after a paragraph
}

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<p>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-p-element) | {{ Spec2('HTML WHATWG') }} | No change since the latest [W3C](/glossary/w3c/) snapshot [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of '<p>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-p-element) | {{ Spec2('HTML5 W3C') }} | `align` attribute is obsolete |
| [**HTML 4.01 Specification** The definition of '<p>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.3.1) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.p") }}

## See also

-   [`hr`](/html/element/hr/)
-   [`br`](/html/element/br/)