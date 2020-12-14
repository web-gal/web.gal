---
title: '<command>: The HTML Command element'
tags:
  - Command
  - HTML
  - HTML commands
  - HTML5
  - 'HTML:Element'
  - 'HTML:Element Reference'
  - Obsolete
permalink: html/element/command
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/command'
obsolete: true
browserCompact: html.elements.command
---
The **HTML Command element** (**`<command>`**) represents a command which the user can invoke. Commands are often used as part of a context menu or toolbar. However, they can be used anywhere on the page.

The `<command>` element is included in the W3C specification, but not in the WHATWG specification, and browser support is nonexistent. You should use the [`menuitem`](/html/element/menuitem/) element instead, although that element is non-standard and only supported in Edge and Firefox.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), metadata content. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | The start tag is mandatory, but, as it is a void element, the use of an end tag is forbidden. |
| Permitted parent elements | [`colgroup`](/html/element/colgroup/) only, though it can be implicitly defined as its start tag is not mandatory. The [`colgroup`](/html/element/colgroup/) must not have a [`span`](/html/element/span/) as child. |
| DOM interface | {{ domxref("HTMLCommandElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("checked") }}
: Indicates whether the command is selected. Must be omitted unless the `type` attribute is `checkbox` or `radio`.

{{ htmlattrdef("disabled") }}
: Indicates that the command is not available.

{{ htmlattrdef("icon") }}
: Gives a picture which represents the command.

{{ htmlattrdef("label") }}
: The name of the command as shown to the user.

{{ htmlattrdef("radiogroup") }}
: This attribute gives the name of the group of commands, with a `type` of `radio`, that will be toggled when the command itself is toggled. This attribute must be omitted unless the `type` attribute is `radio`.

{{ htmlattrdef("type") }}
: This attribute indicates the kind of command. This can be one of three values.

-   `command` or empty which is the default state and indicates that this is a normal command.
    
-   `checkbox` indicates that the command can be toggled using a checkbox.
    
-   `radio` indicates that the command can be toggled using a radio button.

## Examples

```html
<command type="command" label="Save"
    icon="icons/save.png" onclick="save()">

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5** The definition of '<command>' in that specification](https://www.w3.org/TR/html52/semantics.html#the-command-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.command") }}

{{ HTMLRef  }}