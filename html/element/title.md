---
title: '<title>: The Document Title element'
tags:
  - Element
  - HTML
  - HTML document metadata
  - 'HTML:Metadata content'
  - Page Name
  - Page Title
  - Reference
  - Tab Name
  - Tab Title
  - Title
  - Web
  - Window Name
  - Window Title
permalink: html/element/title
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title'
browserCompact: html.elements.title
---
{{ HTMLRef }}

The **HTML Title element** (**`<title>`**) defines the document's title that is shown in a [browser](/glossary/browser/)'s title bar or a page's tab. It only contains text; tags within the element are ignored.

```html
<title>Grandma's Heavy Metal Festival Journal</title>
```

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Metadata content](/html/content_categories#metadata_content). |
| Permitted content | Text that is not inter-element [whitespace](/glossary/whitespace/). |
| Tag omission | Both opening and closing tags are required. Note that leaving off `</title>` should cause the browser to ignore the rest of the page. |
| Permitted parents | A [`head`](/html/element/head/) element that contains no other [`title`](/html/element/title/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted. |
| DOM interface | {{ domxref("HTMLTitleElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

The `<title>` element is always used within a page's [`head`](/html/element/head/) block.

### Page titles and SEO

The contents of a page title can have significant implications for search engine optimization ([SEO](/glossary/seo/)). In general, a longer, descriptive title performs better than short or generic titles. The content of the title is one of the components used by search engine algorithms to decide the order in which to list pages in search results. Also, the title is the initial "hook" by which you grab the attention of readers glancing at the search results page.

A few guidelines and tips for composing good titles:

-   Avoid one- or two-word titles. Use a descriptive phrase, or a term-definition pairing for glossary or reference-style pages.
-   Search engines typically display about the first 55–60 characters of a page title. Text beyond that may be lost, so try not to have titles longer than that. If you must use a longer title, make sure the important parts come earlier and that nothing critical is in the part of the title that is likely to be dropped.
-   Don't use "keyword blobs." If your title is just a list of words, algorithms often reduce your page's position in the search results.
-   Try to make sure your titles are as unique as possible within your own site. Duplicate—or near-duplicate—titles can contribute to inaccurate search results.

## Example

```html
<title>Awesome interesting stuff</title>

```

This example establishes a page whose title (as displayed at the top of the window or in the window's tab) as "Awesome interesting stuff".

## Accessibility concerns

It is important to provide a `title` value that describes the page's purpose. 

A common navigation technique for users of assistive technology is to read the page title and infer the content the page contains. This is because navigating into a page to determine its content can be a time consuming and potentially confusing process.

### Example

```
<title>Menu - Blue House Chinese Food - FoodYum: Online takeout today!</title>

```

To help the user, update the page `title` value to reflect significant page state changes (such as form validation problems).

### Example

```
<title>2 errors - Your order - Blue House Chinese Food - FoodYum: Online takeout today!</title>

```

-   [MDN Understanding WCAG, Guideline 2.4 explanations](/accessibility/understanding_wcag/operable#guideline_2.4_—_navigable_provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are)
-   [Understanding Success Criterion 2.4.2 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-title.html)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<title>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-title-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<title>' in that specification](https://www.w3.org/TR/html52/document-metadata.html#the-title-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<title>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.4.2) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.title") }}