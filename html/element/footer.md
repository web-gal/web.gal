---
title: <footer>
tags:
  - Element
  - HTML
  - HTML sections
  - Reference
permalink: html/element/footer
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer'
browserCompact: html.elements.footer
---
{{ HTMLRef }}

The **HTML `<footer>` element** represents a footer for its nearest [sectioning content](/guide/html/content_categories#sectioning_content) or [sectioning root](/guide/html/using_html_sections_and_outlines#sectioning_root) element. A footer typically contains information about the author of the section, copyright data or links to related documents.

{{ EmbedInteractiveExample("pages/tabbed/footer.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), palpable content. |
| Permitted content | [Flow content](/html/content_categories#flow_content), but with no `<footer>` or [`header`](/html/element/header/) descendants. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). Note that a `<footer>` element must not be a descendant of an [`address`](/html/element/address/), [`header`](/html/element/header/) or another `<footer>` element. |
| Implicit ARIA role | [contentinfo](/accessibility/aria/roles/contentinfo_role), or [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) if a descendant of an [article](/html/element/article), [aside](/html/element/aside), [main](/html/element/main), [nav](/html/element/nav) or [section](/html/element/section) element, or an element with `role=[article](/accessibility/aria/roles/article_role)`, [complementary](/accessibility/aria/roles/complementary_role), [main](/accessibility/aria/roles/main_role), [navigation](/accessibility/aria/roles/navigation_role) or [region](/accessibility/aria/roles/region_role) |
| Permitted ARIA roles | [`group`](https://w3c.github.io/aria/#group), [`presentation`](https://w3c.github.io/aria/#presentation) or [`none`](https://w3c.github.io/aria/#none) |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

-   Enclose information about the author in an [`address`](/html/element/address/) element that can be included into the `<footer>` element.
-   The `<footer>` element is not sectioning content and therefore doesn't introduce a new section in the [outline](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document "Sections and Outlines of an HTML5 document").

## Examples

```html
<footer>
  Some copyright info or perhaps some author
  info for an &lt;article&gt;?
</footer>

```

## Accessibility concerns

Prior to the release of Safari 13, the `contentinfo` [landmark role](/en-US/docs/Learn/Accessibility/WAI-ARIA_basics#SignpostsLandmarks) was not properly exposed by [VoiceOver](https://help.apple.com/voiceover/info/guide/). If needing to support legacy Safari browsers, add `role="contentinfo"` to the `footer` element to ensure the landmark will be properly exposed.

-   Related: [WebKit Bugzilla: 146930 – AX: HTML native elements (header, footer, main, aside, nav) should work the same as ARIA landmarks, sometimes they don't](https://bugs.webkit.org/show_bug.cgi?id=146930)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<footer>' in that specification](https://html.spec.whatwg.org/multipage/#the-footer-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<footer>' in that specification](https://www.w3.org/TR/html52/sections.html#the-footer-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.footer") }}

## See also

-   Other section-related elements: [`body`](/html/element/body/), [`nav`](/html/element/nav/), [`article`](/html/element/article/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`hgroup`](/html/element/hgroup/), [`header`](/html/element/header/), [`section`](/html/element/section/), [`address`](/html/element/address/);
-   [Using HTML sections and outlines](/guide/html/using_html_sections_and_outlines)
-   [ARIA: Contentinfo role](/accessibility/aria/roles/contentinfo_role)