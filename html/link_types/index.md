---
title: Link types
tags:
  - Attribute
  - HTML
  - Link
  - Link types
  - Reference
permalink: html/link_types
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types'
browserCompact: html.elements.link.rel
---
In HTML, link types indicate the relationship between two documents, in which one links to the other using an [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/), or [`link`](/html/element/link/) element.

List of the defined link types and their significance in HTML
| Link Type | Description | Allowed in these elements | Not allowed in these elements |
| --- | --- | --- | --- |
| `alternate` | 
-   If the element is [`link`](/html/element/link/) and the {{ HTMLAttrxRef("rel", "link") }} attribute also contains the `stylesheet` type, the link defines an [alternative style sheet](/en-US/docs/Alternative_style_sheets); in that case the {{ HTMLAttrxRef("title", "link") }} attribute must be present and not be the empty string.
-   If the {{ HTMLAttrxRef("type","link") }} is set to `application/rss+xml` or `application/atom+xml`, the link defines a [syndication feed](/en-US/docs/RSS/Getting_Started/Syndicating). The first one defined on the page is the default.
-   Otherwise, the link defines an alternative page, of one of these types:
    -   for another medium, like a handheld device (if the {{ HTMLAttrxRef("media","link") }} attribute is set)
    -   in another language (if the {{ HTMLAttrxRef("hreflang","link") }} attribute is set),
    -   in another format, such as a PDF (if the {{ HTMLAttrxRef("type","link") }} attribute is set)
    -   a combination of these

 | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `archives` {{ Obsolete_Inline }} | Defines a hyperlink to a document that contains an archive link to this one. For example, a blog entry could link to a monthly index page this way.  
  
**Note:** Although recognized, the singular `archive` is incorrect and must be avoided. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `author` | Defines a hyperlink to a page describing the author or providing a way to contact the author.  
  
**Note:** This may be a `mailto:` hyperlink, but this is not recommended on public pages as robot harvesters will quickly lead to a lot of spam sent to the address. In that case, it is better to lead to a page containing a contact form.  
  
Although recognized, the {{ HTMLAttrxRef("rev", "link") }} attribute on [`a`](/html/element/a/), [`area`](/html/element/area/) or[`link`](/html/element/link/) elements with a link type of `made` is incorrect and should be replaced by the {{ HTMLAttrxRef("rel", "link") }} attribute with this link type. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `bookmark` | Indicates that the hyperlink is a [permalink](/en-US/docs/Permalink) for the nearest ancestor [`article`](/html/element/article/) element. If none, it is a permalink for the [section](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document) that the element is most closely associated to.  
  
This allows for bookmarking a single article in a page containing multiple articles, such as on a monthly summary blog page, or a blog aggregator. | [`a`](/html/element/a/), [`area`](/html/element/area/) | [`link`](/html/element/link/), [`form`](/html/element/form/) |
| `canonical` | From Wikipedia, the free encyclopedia: [Canonical_link_element](https://en.wikipedia.org/wiki/Canonical_link_element)  
A canonical link element is an HTML element that helps webmasters prevent duplicate content issues by specifying the "canonical" or "preferred" version of a web page as part of search engine optimization. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `[dns-prefetch](/html/link_types/dns-prefetch)` {{ Experimental_Inline }} | Hints to the browser that a resource is needed, allowing the browser to do a DNS lookup and protocol handshaking before a user clicks the link. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `external` | Indicates that the hyperlink leads to a resource outside the site of the current page; that is, following the link will make the user leave the site. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) | [`link`](/html/element/link/) |
| `first` {{ Obsolete_Inline }} | Indicates that the hyperlink leads to the first resource of the _sequence_ the current page is in.  
  
**Note:** Other link types related to linking resources in the same sequence are `last`, `prev`, `next`.  
  
Although recognized, the synonyms `begin` and `start` are incorrect and must be avoided. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `help` | 

-   If the element is [`a`](/html/element/a/) or [`area`](/html/element/area/), it indicates that the hyperlink leads to a resource giving further help about the parent of the element, and its descendants.
-   If the element is [`link`](/html/element/link/) it indicates that the hyperlink leads to a resource giving further help about the page as a whole.

 | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/), [`link`](/html/element/link/) | _None._ |
| `icon` | Defines a resource for representing the page in the user interface, usually an icon (auditory or visual). In the browser, it is usually referred to as the [favicon](/glossary/favicon/).  
  
If there are multiple `<link rel="icon">`s, the browser uses their {{ HTMLAttrxRef("media","link") }}, {{ HTMLAttrxRef("type","link") }}, and {{ HTMLAttrxRef("sizes","link") }} attributes to select the most appropriate icon. If several icons are equally appropriate, the last one is used. If the most appropriate icon is later found to be inappropriate, for example because it uses an unsupported format, the browser proceeds to the next-most appropriate, and so on.  
  
**Note:** Apple's iOS does not use this link type, nor the {{ HTMLAttrxRef("sizes","link") }} attribute, like others mobile browsers do, to select a webpage icon for Web Clip or a start-up placeholder. Instead it uses the non-standard [`apple-touch-icon`](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html#//apple_ref/doc/uid/TP40002051-CH3-SW4) and [`apple-touch-startup-image`](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html#//apple_ref/doc/uid/TP40002051-CH3-SW6) respectively.  
  
The `shortcut` link type is often seen before `icon`, but this link type is non-conforming, ignored and **web authors must not use it anymore**. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `import` {{ Experimental_Inline }} | [HTML Imports](/web_components/html_imports) | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `index` {{ Obsolete_Inline("HTML5") }} | Indicates that the page is part of a _hierarchical_ structure and that the hyperlink leads to the top level resource of that structure.  
  
If one or several `up` link types are also present, the number of these `up` indicates the depth of the current page in the hierarchy. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `last` {{ Obsolete_Inline }} | Indicates that the hyperlink leads to the _last_ resource of the _sequence_ the current page is in.  
  
**Note:** Other link types related to linking resources in the same sequence are `first`, `prev`, `next`.  
  
Although recognized, the synonym `end` is incorrect and must be avoided. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `license` | Indicates that the hyperlink leads to a document describing the licensing information. If not inside the [`head`](/html/element/head/) element, the standard doesn't distinguish between a hyperlink applying to a specific part of the document or to the document as a whole. Only the data on the page can indicate this.  
  
**Note:** Although recognized, the synonym `copyright` is incorrect and must be avoided. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/), [`link`](/html/element/link/) | _None._ |
| `[manifest](/html/link_types/manifest)` | Indicates that the linked file is a [Web App Manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest). | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `[modulepreload](/html/link_types/modulepreload)` | Initiates early (and high-priority) loading of module scripts. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `next` | Indicates that the hyperlink leads to the _next_ resource of the _sequence_ the current page is in.  
  
**Note:** Other link types related to linking resources in the same sequence are `first`, `prev`, `last`. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/), [`link`](/html/element/link/) | _None._ |
| `nofollow` | Indicates that the linked document is not endorsed by the author of this one, for example if it has no control over it, if it is a bad example or if there is commercial relationship between the two (sold link). This link type may be used by some search engines that use popularity ranking techniques. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) | [`link`](/html/element/link/) |
| `[noopener](/html/link_types/noopener)` | 

Instructs the browser to open the link without granting the new browsing context access to the document that opened it — by not setting the {{ DOMxRef("Window.opener") }} property on the opened window (it returns `null`).  
  
This is especially useful when opening untrusted links, in order to ensure they cannot tamper with the originating document via the {{ DOMxRef("Window.opener") }} property (see [About rel=noopener](https://mathiasbynens.github.io/rel-noopener/) for more details), while still providing the `Referer` HTTP header (unless `noreferrer` is used as well).

Note that when `noopener` is used, nonempty target names other than `_top`, `_self`, and `_parent` are all treated like `_blank` in terms of deciding whether to open a new window/tab.

 | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) | [`link`](/html/element/link/) |
| `noreferrer` | 

Prevents the browser, when navigating to another page, to send this page address, or any other value, as referrer via the `Referer:` HTTP header.  
(In Firefox, before Firefox 37, this worked only in links found in pages. Links clicked in the UI, like "Open in a new tab" via the contextual menu, ignored this).

 | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) | [`link`](/html/element/link/) |
| `opener` {{ Experimental_Inline }} | 

Reverts implicit `rel="noopener"` addition on links with `target="_blank"` (See [related HTML spec discussion](https://github.com/whatwg/html/issues/4078), [WebKit change](https://trac.webkit.org/changeset/237144/webkit/), and [Firefox bug discussion](https://bugzilla.mozilla.org/show_bug.cgi?id=1503681)).

 | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) | [`link`](/html/element/link/) |
| `pingback` | Defines an external resource URI to call if one wishes to make a comment or a citation about the webpage. The protocol used to make such a call is defined in the [Pingback 1.0](http://www.hixie.ch/specs/pingback/pingback) specification.  
  
**Note:** if the `X-Pingback:` HTTP header is also present, it supersedes the [`link`](/html/element/link/) element with this link type. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `[preconnect](/html/link_types/preconnect)` {{ Experimental_Inline }} | Provides a hint to the browser suggesting that it open a connection to the linked web site in advance, without disclosing any private information or downloading any content, so that when the link is followed the linked content can be fetched more quickly. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `[prefetch](/html/link_types/prefetch)` | Suggests that the browser fetch the linked resource in advance, as it is likely to be requested by the user. Starting with Firefox 44, the value of the {{ HTMLAttrxRef("crossorigin", "link") }} attribute is taken into consideration, making it possible to make anonymous prefetches.  
  
**Note:** The [Link Prefetch FAQ](/en-US/docs/Link_prefetching_FAQ) has details on which links can be prefetched and on alternative methods. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `[preload](/html/link_types/preload)` | Tells the browser to download a resource because this resource will be needed later during the current navigation. See [Preloading content with rel="preload"](/html/preloading_content) for more details. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `[prerender](/html/link_types/prerender)` {{ Experimental_Inline }} | Suggests that the browser fetch the linked resource in advance, and that it also render the prefetched content offscreen so it can be quickly presented to the user once needed. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `prev` | Indicates that the hyperlink leads to the _preceding_ resource of the _sequence_ the current page is in.  
  
**Note:** You can also use the `next` keyword to specify a link to the next page in the sequence.  
  
Although recognized, the synonym `previous` is incorrect and must be avoided. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/), [`form`](/html/element/form/) | _None._ |
| `search` | Indicates that the hyperlink references a document whose interface is specially designed for searching in this document, or site, and its resources.  
  
If the {{ HTMLAttrxRef("type","link") }} attribute is set to `application/opensearchdescription+xml` the resource is an [OpenSearch plugin](/en-US/docs/Creating_OpenSearch_plugins_for_Firefox) that can be easily added to the interface of some browsers like Firefox or Internet Explorer. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/), [`form`](/html/element/form/) | _None._ |
| `shortlink` | [`shortlink` Specification](https://code.google.com/archive/p/shortlink/wikis/Specification.wiki)  
From Wikipedia, the free encyclopedia: [URL shortening](https://en.wikipedia.org/wiki/URL_shortening)  
Some websites create short links to make sharing links via instant messaging easier. | [`link`](/html/element/link/) | ??? |
| `sidebar` {{ Non-standard_Inline }}{{ Obsolete_Inline("Gecko63") }} | Indicates that the hyperlink leads to a resource that would be better suited for a secondary browsing context, like a _sidebar_. Browsers, that don't have such a context will ignore this keyword.  
  
While once part of the HTML specification, this has been removed from the spec and is only implemented by versions of Firefox prior to Firefox 63. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |
| `stylesheet` | Defines an external resource to be used as a stylesheet. If the `type` is not set, the browser should assume it is a `text/css` stylesheet until further inspection.  
  
If used in combination with the `alternate` keyword, it defines an [alternative style sheet](/en-US/docs/Alternative_style_sheets); in that case the {{ HTMLAttrxRef("title", "link") }} attribute must be present and not be the empty string. | [`link`](/html/element/link/) | [`a`](/html/element/a/), [`area`](/html/element/area/), [`form`](/html/element/form/) |
| `tag` | Indicates that the hyperlink refers to a document describing a _tag_ that applies to this document.  
  
**Note:** This link type should not be set on links to a member of a tag cloud as these do not apply to a single document but to a set of pages. | [`a`](/html/element/a/), [`area`](/html/element/area/) | [`link`](/html/element/link/), [`form`](/html/element/form/) |
| `up` {{ Obsolete_Inline }} | Indicates that the page is part of a _hierarchical_ structure and that the hyperlink leads to the higher level resource of that structure.  
  
The number of `up` link types indicates the depth difference between the current page and the linked resource. | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | [`form`](/html/element/form/) |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**Preload** The definition of 'preload' in that specification](https://w3c.github.io/preload/#x2.link-type-preload) | {{ Spec2("Preload") }} | Added `preload`. |
| [**Resource Hints** The definition of 'preconnect' in that specification](https://www.w3.org/TR/resource-hints/#dfn-preconnect) | {{ Spec2("Resource Hints") }} | Added `dns-prefetch`, `preconnect`, and `prerender` values. |
| [**HTML Living Standard** The definition of 'link types' in that specification](https://html.spec.whatwg.org/multipage/links.html#linkTypes) | {{ Spec2("HTML WHATWG") }} | Added `opener` and made `noopener` the default behavior for `target="_blank"` links. |
| [**HTML 5** The definition of 'link types' in that specification](https://www.w3.org/TR/html52/links.html#linkTypes) | {{ Spec2("HTML5 W3C") }} | Added `tag`, `search`, `prefetch`, `noreferrer`, `nofollow`, `icon`, and `author`.  
Renamed `copyright` to `license`.  
Removed `start`, `chapter`, `section`, `subsection`, and `appendix` |
| [**HTML 4.01 Specification** The definition of 'link types' in that specification](https://www.w3.org/TR/html401/types.html#type-links) | {{ Spec2("HTML4.01") }} | Added `alternate`, `stylesheet`, `start`, `chapter`, `section`, `subsection`, `appendix`, and `bookmark`.  
Renamed `previous` to `prev`.  
Removed `top`, and `search`. |
| [**HTML3.2** The definition of '<link>' in that specification](https://www.w3.org/TR/2018/SPSD-html32-20180315/#link) | Obsolete | Added `top`, `contents`, `index`, `glossary`, `copyright`, `next`, `previous`, `help`, and `search`. |
| [RFC 1866: HTML 2.0](https://tools.ietf.org/html/rfc1866) | Obsolete | Initial definition. |

## Browser compatibility

{{ Compat("html.elements.link.rel") }}