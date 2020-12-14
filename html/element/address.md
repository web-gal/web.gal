---
title: '<address>: The Contact Address element'
tags:
  - Address
  - Author
  - Contact
  - Contact Information
  - Element
  - Email
  - Email Address
  - HTML
  - HTML sections
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - Reference
  - Web
permalink: html/element/address
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address'
browserCompact: html.elements.address
---
{{ HTMLRef }}

The **HTML `<address>` element** indicates that the enclosed HTML provides contact information for a person or people, or for an organization.

{{ EmbedInteractiveExample("pages/tabbed/address.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The contact information provided by an `<address>` element's contents can take whatever form is appropriate for the context, and may include any type of contact information that is needed, such as a physical address, URL, email address, phone number, social media handle, geographic coordinates, and so forth. The `<address>` element should include the name of the person, people, or organization to which the contact information refers.

`<address>` can be used in a variety of contexts, such as providing a business's contact information in the page header, or indicating the author of an article by including an `<address>` element within the [`article`](/html/element/article/).

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), palpable content. |
| Permitted content | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), but with no nested `<address>` element, no heading content ([`hgroup`](/html/element/hgroup/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/)), no sectioning content ([`article`](/html/element/article/), [`aside`](/html/element/aside/), [`section`](/html/element/section/), [`nav`](/html/element/nav/)), and no [`header`](/html/element/header/) or [`footer`](/html/element/footer/) element. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/en-US/docs/HTML/Content_categories#Flow_content), but always excluding `<address>` elements (according to the logical principle of symmetry, if `<address>` tag, as a parent, can not have nested `<address>` element, then the same `<address>` content can not have `<address>` tag as its parent). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} Prior to Gecko 2.0 (Firefox 4), Gecko implemented this element using the {{ domxref("HTMLSpanElement") }} interface |

## Attributes

This element only includes the [global attributes](/html/global_attributes "HTML/Global attributes").

## Usage notes

-   It used to be the case that an `<address>` element was only supposed to be used to represent the contact information of the document's author. In the latest spec versions however, its definition has been updated so it can now be used to mark up arbitrary addresses.
-   This element should not contain more information than the contact information, like a publication date (which belongs in a [`time`](/html/element/time/) element).
-   Typically an `<address>` element can be placed inside the [`footer`](/html/element/footer/) element of the current section, if any.

## Examples

This example demonstrates the use of `<address>` to demarcate the contact information for an article's author.

```html
  <address>
    You can contact author at <a href="http://www.somedomain.com/contact">
    www.somedomain.com</a>.<br>
    If you see any bugs, please <a href="mailto:webmaster@somedomain.com">
    contact webmaster</a>.<br>
    You may also want to visit us:<br>
    Mozilla Foundation<br>
    331 E Evelyn Ave<br>
    Mountain View, CA 94041<br>
    USA
  </address>

```

### Result

{{ EmbedLiveSample("Examples", "300", "200") }}

Although it renders text with the same default styling as the [`i`](/html/element/i/) or [`em`](/html/element/em/) elements, it is more appropriate to use `<address>` when dealing with contact information, as it conveys additional semantic information.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<address>' in that specification](https://html.spec.whatwg.org/multipage/sections.html#the-address-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<address>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-address-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<address>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.5.6) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.address") }}

## See also

-   Others section-related elements: [`body`](/html/element/body/), [`nav`](/html/element/nav/), [`article`](/html/element/article/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`hgroup`](/html/element/hgroup/), [`footer`](/html/element/footer/), [`section`](/html/element/section/), [`header`](/html/element/header/);
-   [Sections and outlines of an HTML5 document](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document "Sections and Outlines of an HTML5 document").