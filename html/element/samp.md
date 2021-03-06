---
title: '<samp>: The Sample Output element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Inline Sample
  - Reference
  - Sample Output
  - Sample Text
  - Web
permalink: html/element/samp
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp'
browserCompact: html.elements.samp
---
{{ HTMLRef }}

The **HTML Sample Element** (**`<samp>`**) is used to enclose inline text which represents sample (or quoted) output from a computer program. Its contents are typically rendered using the browser's default monospaced font (such as [`Courier (typeface`](https://en.wikipedia.org/wiki/Courier_(typeface) or Lucida Console).

{{ EmbedInteractiveExample("pages/tabbed/samp.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

You can use a CSS rule to override the browser's default font face for the `<samp>` element; however, it's possible that the browser's preferences may take precedence over any CSS you specify.

The CSS to override the default font face would look like this:

```css
samp {
  font-family: "Courier";
}
```

If you need an element which will serve as a container for output generated by your website or app's JavaScript code, you should instead use the [`output`](/html/element/output/) element.

## Examples

### Basic example

In this simple example, a paragraph includes an example of the output of a program.

```html
<p>When the process is complete, the utility will output the text
<samp>Scan complete. Found <em>N</em> results.</samp> You can then
proceed to the next step.</p>
```

The resulting output looks like this:

{{ EmbedLiveSample("Basic_example", 650, 100) }}

### Sample output including user input

You can nest the [`kbd`](/html/element/kbd/) element within a `<samp>` block to present an example that includes text entered by the user. For example, consider this text presenting a transcript of a Linux (or macOS) console session:

#### HTML

```html
<pre>
<samp><span class="prompt">mike@interwebz:~$</span> <kbd>md5 -s "Hello world"</kbd>
MD5 ("Hello world") = 3e25960a79dbc69b674cd4ec67a72c62

<span class="prompt">mike@interwebz:~$</span> <span class="cursor">█</span></samp></pre>
```

Note the use of [`span`](/html/element/span/) to allow customization of the appearance of specific portions of the sample text such as the shell prompts and the cursor. Note also the use of `<kbd>` to represent the command the user entered at the prompt in the sample text.

#### CSS

The CSS that achieves the appearance we want is:

```css
.prompt {
  color: #b00;
}

samp > kbd {
  font-weight: bold;
}

.cursor {
  color: #00b;
}
```

This simply gives the prompt and cursor fairly subtle colorization and emboldens the keyboard input within the sample text.

#### Result

The resulting output is this:

{{ EmbedLiveSample("Sample_output_including_user_input", 650, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<samp>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-samp-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<samp>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-samp-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<samp>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.samp") }}

## See also

-   Related elements: [`kbd`](/html/element/kbd/), [`code`](/html/element/code/), [`pre`](/html/element/pre/)
-   The [`output`](/html/element/output/) element: a container for script-generated output