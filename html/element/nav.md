---
title: '<nav>: The Navigation Section element'
tags:
  - Element
  - HTML
  - HTML sections
  - Links
  - Navigation
  - Reference
  - Sections
  - Web
  - nav
permalink: html/element/nav
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav'
browserCompact: html.elements.nav
---
{{ HTMLRef }}

The **HTML `<nav>` element** represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.

{{ EmbedInteractiveExample("pages/tabbed/nav.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/en-US/docs/HTML/Content_categories) | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), [sectioning content](/en-US/docs/HTML/Content_categories#Sectioning_content), palpable content. |
| Permitted content | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Implicit ARIA role | `[navigation](/accessibility/aria/roles/navigation_role)` |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes).

## Usage notes

-   It's not necessary for all links to be contained in a `<nav>` element. `<nav>` is intended only for major block of navigation links; typically the [`footer`](/html/element/footer/) element often has a list of links that don't need to be in a [`nav`](/html/element/nav/) element.
-   A document may have several [`nav`](/html/element/nav/) elements, for example, one for site navigation and one for intra-page navigation. `[aria-labelledby](/accessibility/aria/aria_techniques/using_the_aria-labelledby_attribute)` can be used in such case to promote accessibility, see [example](/html/element/heading_elements#labeling_section_content).
-   User agents, such as screen readers targeting disabled users, can use this element to determine whether to omit the initial rendering of navigation-only content.

## Examples

In this example, a `<nav>` block is used to contain an unordered list ([`ul`](/html/element/ul/)) of links. With appropriate CSS, this can be presented as a sidebar, navigation bar, or drop-down menu.

```html
<nav class="menu">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<nav>' in that specification](https://html.spec.whatwg.org/multipage/sections.html#the-nav-element) | {{ Spec2('HTML WHATWG') }} | No change since latest W3C snapshot. |
| [**HTML 5** The definition of '<nav>' in that specification](https://www.w3.org/TR/html52/sections.html#the-nav-element) | {{ Spec2('HTML5 W3C') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.nav") }}

## See also

-   Other section-related elements: [`body`](/html/element/body/), [`article`](/html/element/article/), [`section`](/html/element/section/), [`aside`](/html/element/aside/), [`h1`](/html/element/h1/), [`h2`](/html/element/h2/), [`h3`](/html/element/h3/), [`h4`](/html/element/h4/), [`h5`](/html/element/h5/), [`h6`](/html/element/h6/), [`hgroup`](/html/element/hgroup/), [`header`](/html/element/header/), [`footer`](/html/element/footer/), [`address`](/html/element/address/);
-   [Sections and outlines of an HTML5 document](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document "Sections and Outlines of an HTML5 document").
-   [ARIA: Navigation role](/accessibility/aria/roles/navigation_role)