---
title: <main>
tags:
  - Element
  - HTML
  - HTML sections
  - Reference
  - main
permalink: html/element/main
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main'
browserCompact: html.elements.main
---
{{ HTMLRef }}

The **HTML `<main>` element** represents the dominant content of the [`body`](/html/element/body/) of a document. The main content area consists of content that is directly related to or expands upon the central topic of a document, or the central functionality of an application.

{{ EmbedInteractiveExample("pages/tabbed/main.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

A document mustn't have more than one `<main>` element that doesn't have the {{ htmlattrxref("hidden") }} attribute specified.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), palpable content. |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | None; both the starting and ending tags are mandatory. |
| Permitted parents | Where [flow content](/html/content_categories#flow_content) is expected, but only if it is a [hierarchically correct `main` element](https://html.spec.whatwg.org/multipage/grouping-content.html#hierarchically-correct-main-element). |
| Implicit ARIA role | `[main](/accessibility/aria/roles/main_role)` |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/en-US/docs/HTML/Global_attributes).

## Usage notes

The content of a `<main>` element should be unique to the document. Content that is repeated across a set of documents or document sections such as sidebars, navigation links, copyright information, site logos, and search forms shouldn't be included unless the search form is the main function of the page.

`<main>` doesn't contribute to the document's outline; that is, unlike elements such as [`body`](/html/element/body/), headings such as [`h2`](/html/element/h2/), and such, `<main>` doesn't affect the [DOM's](/glossary/dom/) concept of the structure of the page. It's strictly informative.

## Example

```html
<!-- other content -->

<main>
  <h1>Apples</h1>
  <p>The apple is the pomaceous fruit of the apple tree.</p>

  <article>
    <h2>Red Delicious</h2>
    <p>These bright red apples are the most common found in many
    supermarkets.</p>
    <p>... </p>
    <p>... </p>
  </article>

  <article>
    <h2>Granny Smith</h2>
    <p>These juicy, green apples make a great filling for
    apple pies.</p>
    <p>... </p>
    <p>... </p>
  </article>
</main>

<!-- other content -->
```

## Accessibility concerns

### Landmark

The `<main>` element behaves like a [`main` landmark](/accessibility/aria/roles/main_role) role. [Landmarks](/accessibility/aria/aria_techniques#landmark_roles) can be used by assistive technology to quickly identify and navigate to large sections of the document. Prefer using the `<main>` element over declaring `role="main"`, unless there are [legacy browser support concerns](/html/element/main#browser_compatibility).

### Skip navigation

Skip navigation, also known as "skipnav", is a technique that allows an assistive technology user to quickly bypass large sections of repeated content (main navigation, info banners, etc.). This lets the user access the main content of the page faster.

Adding an {{ htmlattrxref("id") }} attribute to the `<main>` element lets it be a target of a skip navigation link.

```html
<body>
  <a href="#main-content">Skip to main content</a>

  <!-- navigation and header content -->

  <main id="main-content">
    <!-- main page content -->
  </main>
</body>

```

-   [WebAIM: "Skip Navigation" Links](https://webaim.org/techniques/skipnav/)

### Reader mode

Browser reader mode functionality looks for the presence of the `<main>` element, as well as [heading](/html/element/heading_elements) and [content sectioning elements](/html/element#content_sectioning) when converting content into a specialized reader view.

-   [Building websites for Safari Reader Mode and other reading apps.](https://medium.com/@mandy.michael/building-websites-for-safari-reader-mode-and-other-reading-apps-1562913c86c9)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<main>' in that specification](https://html.spec.whatwg.org/multipage/#the-main-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.1** The definition of '<main>' in that specification](https://www.w3.org/TR/html51/grouping-content.html#the-main-element) | {{ Spec2('HTML5.1') }} | No change from [**HTML 5**](https://www.w3.org/TR/html52/). |
| [**HTML 5** The definition of '<main>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-main-element) | {{ Spec2('HTML5 W3C') }} | Initial definition. |

## Browser compatibility

The `<main>` element is widely supported. For Internet Explorer 11 and lower, it's suggested that an [ARIA](/glossary/aria/) role of `"main"` be added to the `<main>` element to ensure it is accessible (screen readers like JAWS, used in combination with older versions of Internet Explorer, understand the semantic meaning of the `<main>` element when this `role` attribute is included).

```html
<main role="main">
  ...
</main>

```

{{ Compat("html.elements.main") }}

## See also

-   Basic structural elements: [`html`](/html/element/html/), [`head`](/html/element/head/), [`body`](/html/element/body/)
-   Section-related elements: [`article`](/html/element/article/), [`aside`](/html/element/aside/), [`footer`](/html/element/footer/), [`header`](/html/element/header/), or [`nav`](/html/element/nav/)
-   [ARIA: Main role](/accessibility/aria/roles/main_role)