---
title: x-ms-acceleratorkey
tags:
  - Attribute
  - HTML
  - 'HTML:Microsoft Extensions'
  - Non-standard
  - Reference
  - x-ms-acceleratorkey
permalink: html/global_attributes/x-ms-acceleratorkey
mdn: >-
  https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/x-ms-acceleratorkey
nonStandard: true
---
The `**x-ms-acceleratorkey**` attribute accessibly declares that an [accelerator key](https://docs.microsoft.com/en-us/windows/uwp/design/input/keyboard-accelerators) has been assigned to an element: the element is activated via JavaScript when the key(s) are pressed on a keyboard.

{{ Non-standard_Inline }} This proprietary property is specific to Internet Explorer and Microsoft Edge.

`x-ms-acceleratorkey` exposes a notification in the accessibility tree, for screen readers and other assistive technologies, that an accelerator key exists for that element. This attribute does **not** provide the accelerator key behavior. You must provide JavaScript event handlers, like `onkeypress`, `onkeydown`, or `onkeyup`, to listen for your declared accelerator keys and activate the element accordingly.

To provide a keyboard shortcut for an element that _does not_ need JavaScript, use [the `accesskey` attribute](/html/global_attributes/accesskey).

## Syntax

```html
<button x-ms-acceleratorkey="[explanation of key combination]">…</button>
```

## Value

The accelerator key combination. For example:

-   `"Ctrl+B"` for a combination of the Ctrl and B keys.
-   `"J"` for just the J key.
-   `"Ctrl+; then K"` for a shortcut similar to [FogBugz’s old keyboard mode](https://help.manuscript.com/7558/fogbugz-keyboard-shortcuts#For_Your_Server_or_non-Ocelot_Keyboard_Shortcuts). This approach is more complicated, but does not override existing keyboard shortcuts provided by the user’s browser or operating system.

## See also

-   [The global `accesskey` attribute](/html/global_attributes/accesskey)
-   [The `-ms-accelerator` CSS property](/css/-ms-accelerator)
-   [Microsoft API extensions](/api/microsoft_api_extensions)