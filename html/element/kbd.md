---
title: '<kbd>: The Keyboard Input element'
tags:
  - Displaying Input
  - Displaying Keys
  - Displaying Keystrokes
  - Displaying User Input
  - Element
  - HTML
  - HTML text-level semantics
  - Keyboard Input
  - Keystroke
  - Reference
  - Web
  - keyboard
  - user input
permalink: html/element/kbd
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd'
browserCompact: html.elements.kbd
---
{{ HTMLRef }}

The **HTML Keyboard Input element** (**`<kbd>`**) represents a span of inline text denoting textual user input from a keyboard, voice input, or any other text entry device. By convention, the [user agent](/glossary/user_agent/) defaults to rendering the contents of a `<kbd>` element using its default monospace font, although this is not mandated by the HTML standard.

{{ EmbedInteractiveExample("pages/tabbed/kbd.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

`<kbd>` may be nested in various combinations with the [`samp`](/html/element/samp/) (Sample Output) element to represent various forms of input or output based on visual cues.

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

Other elements can be used in tandem with `<kbd>` to represent more specific scenarios:

-   Nesting a `<kbd>` element within another `<kbd>` element represents an actual key or other unit of input as a portion of a larger input. See {{ anch("Representing keystrokes within an input") }} below.
-   Nesting a `<kbd>` element inside a [`samp`](/html/element/samp/) element represents input that has been echoed back to the user by the system. See {{ anch("Echoed input") }}, below, for an example.
-   Nesting a `<samp>` element inside a `<kbd>` element, on the other hand, represents input which is based on text presented by the system, such as the names of menus and menu items, or the names of buttons displayed on the screen. See the example under {{ anch("Representing onscreen input options") }} below.

You can define a custom style to override the browser's default font selection for the `<kbd>` element, although the user's preferences may potentially override your CSS.

## Examples

### Basic example

```html
<p>Use the command <kbd>help mycommand</kbd> to view documentation
for the command "mycommand".</p>

```

{{ EmbedLiveSample('Basic_example', 350, 80)  }}

### Representing keystrokes within an input

To describe an input comprised of multiple keystrokes, you can nest multiple `<kbd>` elements, with an outer `<kbd>` element representing the overall input and each individual keystroke or component of the input enclosed within its own `<kbd>`.

#### Unstyled

First, let's look at what this looks like as just plain HTML.

##### HTML

```html
<p>You can also create a new document using the keyboard shortcut
<kbd><kbd>Ctrl</kbd>+<kbd>N</kbd></kbd>.</p>
```

This wraps the entire key sequence in an outer `<kbd>` element, then each individual key within its own, in order to denote the components of the sequence.

**Note:** You don't need to do all this wrapping; you can choose to simplify it by leaving out the external `<kbd>` element. In other words, simplifying this to just `<kbd>Ctrl</kbd>+<kbd>N</kbd>` would be perfectly valid.

Depending on your style sheet, though, you may find it useful to do this kind of nesting.

##### Result

The output looks like this without a style sheet applied:

{{ EmbedLiveSample("Unstyled", 650, 80) }}

#### With custom styles

We can make more sense of this by adding some CSS:

##### CSS

We add a new style for `<kbd>` elements, `key`, which we can apply when rendering keyboard keys:

```css
kbd.key {
  border-radius: 3px;
  padding: 1px 2px 0;
  border: 1px solid black;
}
```

##### HTML

Then we update the HTML to use this class on the keys in the output to be presented:

```html
<p>You can also create a new document by pressing <kbd><kbd class="key">Ctrl</kbd>+<kbd class="key">N</kbd></kbd>.</p>
```

##### Result

The result is just what we want!

{{ EmbedLiveSample("With_custom_styles", 650, 80) }}

### Echoed input

Nesting a `<kbd>` element inside a [`samp`](/html/element/samp/) element represents input that has been echoed back to the user by the system.

```html
<p>If a syntax error occurs, the tool will output the initial
command you typed for your review:</p>
<blockquote>
  <samp><kbd>custom-git ad my-new-file.cpp</kbd></samp>
</blockquote>
```

{{ EmbedLiveSample("Echoed_input", 650, 100) }}

### Representing onscreen input options

Nesting a `<samp>` element inside a `<kbd>` element represents input which is based on text presented by the system, such as the names of menus and menu items, or the names of buttons displayed on the screen.

For example, you can explain how to choose the "New Document" option in the "File" menu using HTML that looks like this:

```html
<p>To create a new file, choose the menu option
<kbd><kbd><samp>File</samp></kbd>⇒<kbd><samp>New
Document</samp></kbd></kbd>.</p>

<p>Don't forget to click the <kbd><samp>OK</samp></kbd> button
to confirm once you've entered the name of the new file.</p>
```

This does some interesting nesting. For the menu option description, the entire input is enclosed in a `<kbd>` element. Then, inside that, both the menu and menu item names are  contained within both `<kbd>` and `<samp>`, indicating an input which is selected from a screen widget.

#### Result

{{ EmbedLiveSample("Representing_onscreen_input_options", 650, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<kbd>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-kbd-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<kbd>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-kbd-element) | {{ Spec2('HTML5 W3C') }} | Expanded to include any user input, like voice input and individual keystrokes. |
| [**HTML 4.01 Specification** The definition of '<kbd>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.kbd") }}

## See also

-   [`code`](/html/element/code/)