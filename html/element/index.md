---
title: HTML elements reference
tags:
  - Basic
  - Element
  - HTML
  - Reference
  - Web
  - 'l10n:priority'
permalink: html/element
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element'
---
This page lists all the [HTML](/glossary/html/) [elements](/glossary/element/), which are created using [tags](/glossary/tag/). They are grouped by function to help you find what you have in mind easily. An alphabetical list of all elements is provided in the sidebar on every element's page as well as this one.

For more information about the basics of HTML elements and attributes, see [the section on elements in the Introduction to HTML article](/guide/html/introduction#elements_%e2%80%94_the_basic_building_blocks).

## Main root

{{ HTMLRefTable("HTML Root Element") }}

## Document metadata

Metadata contains information about the page. This includes information about styles, scripts and data to help software ([search engines](/glossary/search_engine/), [browsers](/glossary/browser/), etc.) use and render the page. Metadata for styles and scripts may be defined in the page or link to another file that has the information. 

{{ HTMLRefTable("HTML Document Metadata") }}

## Sectioning root

{{ HTMLRefTable("Sectioning Root Element") }}

## Content sectioning

Content sectioning elements allow you to organize the document content into logical pieces. Use the sectioning elements to create a broad outline for your page content, including header and footer navigation, and heading elements to identify sections of content.   

{{ HTMLRefTable("HTML Sections") }}

## Text content

Use HTML text content elements to organize blocks or sections of content placed between the opening [`body`](/html/element/body/) and closing `</body>` tags. Important for [accessibility](/glossary/accessibility/) and [SEO](/glossary/seo/), these elements identify the purpose or structure of that content.     

{{ HTMLRefTable("HTML Grouping Content") }}

## Inline text semantics

Use the HTML inline text semantic to define the meaning, structure, or style of a word, line, or any arbitrary piece of text.

{{ HTMLRefTable("HTML Text-Level Semantics") }}

## Image and multimedia

HTML supports various multimedia resources such as images, audio, and video.

{{ HTMLRefTable("multimedia") }}

## Embedded content

In addition to regular multimedia content, HTML can include a variety of other content, even if it's not always easy to interact with.

{{HTMLRefTable({"include":["HTML embedded content"], "exclude":["multimedia"]})}}

## Scripting

In order to create dynamic content and Web applications, HTML supports the use of scripting languages, most prominently JavaScript. Certain elements support this capability.

{{ HTMLRefTable("HTML Scripting") }}

## Demarcating edits

These elements let you provide indications that specific parts of the text have been altered.

{{ HTMLRefTable("HTML Edits") }}

## Table content

The elements here are used to create and handle tabular data.

{{ HTMLRefTable("HTML tabular data") }}

## Forms

HTML provides a number of elements which can be used together to create forms which the user can fill out and submit to the Web site or application. There's a great deal of further information about this available in the [HTML forms guide](/guide/html/forms).

{{HTMLRefTable({"include": ["HTML forms"], "exclude":["Deprecated"]})}}

## Interactive elements

HTML offers a selection of elements which help to create interactive user interface objects.

{{ HTMLRefTable("HTML interactive elements") }}

## Web Components

Web Components is an HTML-related technology which makes it possible to, essentially, create and use custom elements as if it were regular HTML. In addition, you can create custom versions of standard HTML elements.

{{HTMLRefTable({"include":["Web Components"],"exclude":["Deprecated", "Obsolete"]})}}

## Obsolete and deprecated elements

**Warning:** These are old HTML elements which are deprecated and should not be used. **You should never use them in new projects, and should replace them in old projects as soon as you can.** They are listed here for informational purposes only.

{{HTMLRefTable({"include":["Deprecated","Obsolete"]})}}