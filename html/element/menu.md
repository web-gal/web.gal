---
title: <menu>
tags:
  - Element
  - Experimental
  - HTML
  - HTML interactive elements
  - Navigation
  - Reference
  - Site Navigation
  - UI
  - UX
  - User Interface
  - User experience
  - Web
  - menu
  - menus
permalink: html/element/menu
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menu'
deprecated: true
browserCompact: html.elements.menu
---
{{ HTMLRef }}{{ SeeCompatTable }}

The **HTML `<menu>` element** represents a group of commands that a user can perform or activate. This includes both list menus, which might appear across the top of a screen, as well as [context menus](/html/element/menu#context_menu), such as those that might appear underneath a button after it has been clicked.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | 
[Flow content](/html/content_categories#flow_content). If the element's children include at least one [`li`](/html/element/li/) element: [Palpable content](/guide/html/content_categories#palpable_content).

 |
| Permitted content | 

If the element is in the _list menu_ state: [flow content](/html/content_categories#flow_content), or alternatively, zero or more occurrences of [`li`](/html/element/li/), [`script`](/html/element/script/), and [`template`](/html/element/template/). (_list menu_ is the default state, unless the parent element is a [`menu`](/html/element/menu/) in the _context menu_ state.)

If the element is in the _context menu_ state: zero or more occurrences, in any order, of [`menu`](/html/element/menu/) (_context menu_ state only), [`menuitem`](/html/element/menuitem/), [`hr`](/html/element/hr/), [`script`](/html/element/script/), and [`template`](/html/element/template/).

 |
| Tag omission | {{ No_Tag_Omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | `[list](/accessibility/aria/roles/list_role)` |
| Permitted ARIA roles | [`directory`](https://w3c.github.io/aria/#directory), [`group`](https://w3c.github.io/aria/#group), `[listbox](/accessibility/aria/roles/listbox_role)`, [`menu`](https://w3c.github.io/aria/#menu), [`menubar`](https://w3c.github.io/aria/#menubar), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation), [`radiogroup`](https://w3c.github.io/aria/#radiogroup), [`tablist`](https://w3c.github.io/aria/#tablist), [`toolbar`](https://w3c.github.io/aria/#toolbar) or [`tree`](https://w3c.github.io/aria/#tree) |
| DOM interface | {{ DOMxRef("HTMLMenuElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ HTMLAttrDef("label") }} {{ Deprecated_inline }}
: The name of the menu as shown to the user. Used within nested menus, to provide a label through which the submenu can be accessed. Must only be specified when the parent element is a [`menu`](/html/element/menu/) in the _context menu_ state.

{{ HTMLAttrDef("type") }}
: This attribute indicates the kind of menu being declared, and can be one of two values.

-   `context` {{ Deprecated_inline }} : Indicates the _popup menu_ state, which represents a group of commands activated through another element. This might be as a button menu referenced by a {{ HTMLAttrxRef("menu", "button") }} attribute of a [`button`](/html/element/button/) element, or as context menu for an element with a [`contextmenu`](/en-US/docs/HTML/Global_attributes#attr-contextmenu) attribute. This value is the default if the attribute is missing and the parent element is also a `<menu>` element.
-   `toolbar`: Indicates the _toolbar_ state, which represents a toolbar consisting of a series of commands for user interaction. This might be in the form of an unordered list of [`li`](/html/element/li/) elements, or, if the element has no `<li>` element children, [flow content](/html/content_categories#flow_content) describing available commands. This value is the default if the attribute is missing.

## Usage notes

The [`menu`](/html/element/menu/) and [`ul`](/html/element/ul/) elements both represent an unordered list of items. The key difference is that [`ul`](/html/element/ul/) primarily contains items for display, whilst [`menu`](/html/element/menu/) is intended for interactive items, to act on.

An HTML menu can be used to create context menus (typically activated by right-clicking another element) or toolbars.

**{{ anch("Context menu", "Context menus**") }} consist of a `<menu>` element which contains [`menuitem`](/html/element/menuitem/) elements for each selectable option in the menu, `<menu>` elements for submenus within the menu, and [`hr`](/html/element/hr/) elements for separator lines to break up the menu's content into sections. Context menus are then attached to the element they're activated from using either the associated element's {{ HTMLAttrxRef("contextmenu") }} attribute or, for {{ anch("Button menu", "button-activated menus") }} attached to [`button`](/html/element/button/) elements, the {{ HTMLAttrxRef("menu", "button") }} attribute.

**{{ anch("Toolbar", "Toolbar menus**") }} consist of a `<menu>` element whose content is described in one of two ways: either as an unordered list of items represented by [`li`](/html/element/li/) elements (each representing a command or option the user can utilize), or (if there are no `<li>` elements), [flow content](/html/content_categories#flow_content) describing the available commands and options.

This element was deprecated in HTML4, but reintroduced in HTML5.1 and the HTML living standard. This document describes the current Firefox implementation. Type 'list' is likely to change to 'toolbar' according to HTML5.1.

## Examples

### Context menu



#### HTML

```html
<!-- A <div> element with a context menu -->
<div contextmenu="popup-menu">
  Right-click to see the adjusted context menu
</div>

<menu type="context" id="popup-menu">
  <menuitem>Action</menuitem>
  <menuitem>Another action</menuitem>
  <hr/>
  <menuitem>Separated action</menuitem>
</menu>

```

#### CSS

```css
div {
  width: 300px;
  height: 80px;
  background-color: lightgreen;
}

```

#### Result

{{ EmbedLiveSample("Context_menu", "100%", 80) }}

### Menu button

Menu buttons haven't been implemented in any known browsers yet. The {{ HTMLAttrxRef("type", "menu") }} attribute on the `<menu>` element is now obsolete.

[`menuitem`](/html/element/menuitem/) element is obsolete.

#### HTML

```html
<!-- A button, which displays a menu when clicked. -->
<button type="menu" menu="popup-menu">
  Dropdown
</button>

<menu type="context" id="popup-menu">
  <menuitem>Action</menuitem>
  <menuitem>Another action</menuitem>
  <hr/>
  <menuitem>Separated action</menuitem>
</menu>

```

#### Result

{{ EmbedLiveSample("Menu_button", "100%", 50) }}

### Toolbar

Toolbar menus haven't been implemented in any known browsers yet.

#### HTML

```html
<!-- A context menu for a simple editor,
   - containing two menu buttons. -->
<menu type="toolbar">
  <li>
    <button type="menu" menu="file-menu">File</button>
    <menu type="context" id="file-menu">
      <menuitem label="New..." onclick="newFile()">
      <menuitem label="Save..." onclick="saveFile()">
    </menu>
  </li>
  <li>
    <button type="menu" menu="edit-menu">Edit</button>
    <menu type="context" id="edit-menu">
      <menuitem label="Cut..." onclick="cutEdit()">
      <menuitem label="Copy..." onclick="copyEdit()">
      <menuitem label="Paste..." onclick="pasteEdit()">
    </menu>
  </li>
</menu>

```

#### Result

{{ EmbedLiveSample("Toolbar", "100%", 100) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<menu>' in that specification](https://html.spec.whatwg.org/multipage/grouping-content.html#the-menu-element) | {{ Spec2("HTML WHATWG") }} | No change from latest snapshot, {{ SpecName("HTML5.3") }} |
| [**HTML 5.1** The definition of '<menu>' in that specification](https://www.w3.org/TR/html51/interactive-elements.html#the-menu-element) | {{ Spec2("HTML5.1") }} |  |

## Browser compatibility

{{ Compat("html.elements.menu") }}

## See also

-   Other list-related HTML Elements: [`ol`](/html/element/ol/), [`ul`](/html/element/ul/), [`li`](/html/element/li/), [`hr`](/html/element/hr/), and the obsolete [`dir`](/html/element/dir/).
-   The [`contextmenu`](/html/global_attributes#attr-contextmenu) [global attribute](/html/global_attributes) can be used on an element to refer to the `id` of a `menu` with {{ HTMLAttrxRef("type", "menu", 'type="context"') }}.