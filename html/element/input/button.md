---
title: <input type="button">
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - Input
  - Input Element
  - Input Type
  - Reference
  - button
permalink: html/element/input/button
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button'
browserCompact: html.elements.input.input-button
---
{{ HTMLRef("Input_types") }}

[`input`](/html/element/input/) elements of type **`button`** are rendered as simple push buttons, which can be programmed to control custom functionality anywhere on a webpage as required when assigned an event handler function (typically for the {{ event("click") }} event).

{{ EmbedInteractiveExample("pages/tabbed/input-button.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

**Note**: While `<input>` elements of type `button` are still perfectly valid HTML, the newer [`button`](/html/element/button/) element is now the favored way to create buttons. Given that a [`button`](/html/element/button/)’s label text is inserted between the opening and closing tags, you can include HTML in the label, even images.

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} used as the button's label |
| **Events** | {{ domxref("Element/click_event", "click") }} |
| **Supported common attributes** | {{ htmlattrxref("type", "input") }} and {{ htmlattrxref("value", "input") }} |
| **IDL attributes** | `value` |
| **Methods** | None |

## Value

An `<input type="button">` elements' {{ htmlattrxref("value", "input") }} attribute contains a {{ domxref("DOMString") }} that is used as the button's label.

```html
<input type="button" value="Click Me">
```

{{ EmbedLiveSample("summary-example3", 650, 30) }}

If you don't specify a `value`, you get an empty button:

```html
<input type="button">
```

{{ EmbedLiveSample("summary-example1", 650, 30) }}

## Using buttons

`<input type="button">` elements have no default behavior (their cousins, `[<input type="submit">](/html/element/input/submit)` and `[<input type="reset">](/html/element/input/reset)` are used to submit and reset forms, respectively). To make buttons do anything, you have to write JavaScript code to do the work.

### A simple button

We'll begin by creating a simple button with a {{ event("click") }} event handler that starts our machine (well, it toggles the `value` of the button and the text content of the following paragraph):

```html
<form>
  <input type="button" value="Start machine">
</form>
<p>The machine is stopped.</p>
```
```js
const button = document.querySelector('input');
const paragraph = document.querySelector('p');

button.addEventListener('click', updateButton);

function updateButton() {
  if (button.value === 'Start machine') {
    button.value = 'Stop machine';
    paragraph.textContent = 'The machine has started!';
  } else {
    button.value = 'Start machine';
    paragraph.textContent = 'The machine is stopped.';
  }
}
```

The script gets a reference to the {{ domxref("HTMLInputElement") }} object representing the `<input>` in the DOM, saving this refence in the variable `button`. {{ domxref("EventTarget.addEventListener", "addEventListener()") }} is then used to establish a function that will be run when {{ event("click") }} events occur on the button.

{{ EmbedLiveSample("A_simple_button", 650, 100) }}

### Adding keyboard shortcuts to buttons

Keyboard shortcuts, also known as access keys and keyboard equivalents, let the user trigger a button using a key or combination of keys on the keyboard. To add a keyboard shortcut to a button — just as you would with any [`input`](/html/element/input/) for which it makes sense — you use the {{ htmlattrxref("accesskey") }} global attribute.

In this example, s is specified as the access key (you'll need to press s plus the particular modifier keys for your browser/OS combination; see [accesskey](/html/global_attributes/accesskey) for a useful list of those).

```html
<form>
  <input type="button" value="Start machine" accesskey="s">
</form>
<p>The machine is stopped.</p>

```

```js
const button = document.querySelector('input');
const paragraph = document.querySelector('p');

button.addEventListener('click', updateButton);

function updateButton() {
  if (button.value === 'Start machine') {
    button.value = 'Stop machine';
    paragraph.textContent = 'The machine has started!';
  } else {
    button.value = 'Start machine';
    paragraph.textContent = 'The machine is stopped.';
  }
}
```

{{ EmbedLiveSample("Adding_keyboard_shortcuts_to_buttons", 650, 100) }}

**Note**: The problem with the above example of course is that the user will not know what the access key is! In a real site, you'd have to provide this information in a way that doesn't intefere with the site design (for example by providing an easily accessible link that points to information on what the site accesskeys are).

### Disabling and enabling a button

To disable a button, simply specify the {{ htmlattrxref("disabled") }} global attribute on it, like so:

```html
<input type="button" value="Disable me" disabled>
```

You can enable and disable buttons at run time by simply setting `disabled` to `true` or `false`. In this example our button starts off enabled, but if you press it, it is disabled using `button.disabled = true`. A {{ domxref("WindowTimers.setTimeout","setTimeout()") }} function is then used to reset the button back to its enabled state after two seconds.

###### Hidden code 1

```html
<input type="button" value="Enabled">
```
```js
const button = document.querySelector('input');

button.addEventListener('click', disableButton);

function disableButton() {
  button.disabled = true;
  button.value = 'Disabled';
  window.setTimeout(function() {
    button.disabled = false;
    button.value = 'Enabled';
  }, 2000);
}
```

{{ EmbedLiveSample("Hidden_code_1", 650, 60) }}

If the `disabled` attribute isn't specified, the button inherits its `disabled` state from its parent element. This makes it possible to enable and disable groups of elements all at once by enclosing them in a container such as a [`fieldset`](/html/element/fieldset/) element, and then setting `disabled` on the container.

The example below shows this in action. This is very similar to the previous example, except that the `disabled` attribute is set on the `<fieldset>` when the first button is pressed — this causes all three buttons to be disabled until the two second timeout has passed.

###### Hidden code 2

```html
<fieldset>
  <legend>Button group</legend>
  <input type="button" value="Button 1">
  <input type="button" value="Button 2">
  <input type="button" value="Button 3">
</fieldset>
```
```js
const button = document.querySelector('input');
const fieldset = document.querySelector('fieldset');

button.addEventListener('click', disableButton);

function disableButton() {
  fieldset.disabled = true;
  window.setTimeout(function() {
    fieldset.disabled = false;
  }, 2000);
}
```

{{ EmbedLiveSample("Hidden_code_2", 650, 60) }}

**Note**: Firefox will, unlike other browsers, by default, [persist the dynamic disabled state](http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of a [`button`](/html/element/button/) across page loads. Use the {{ htmlattrxref("autocomplete","button") }} attribute to control this feature.

## Validation

Buttons don't participate in constraint validation; they have no real value to be constrained.

## Examples

The below example shows a very simple drawing app created using a [`canvas`](/html/element/canvas/) element and some simple CSS and JavaScript (we'll hide the CSS for brevity). The top two controls allow you to choose the color and size of the drawing pen. The button, when clicked, invokes a function that clears the canvas.

```html
<div class="toolbar">
  <input type="color" aria-label="select pen color">
  <input type="range" min="2" max="50" value="30" aria-label="select pen size"><span class="output">30</span>
  <input type="button" value="Clear canvas">
</div>

<canvas class="myCanvas">
  <p>Add suitable fallback here.</p>
</canvas>
```

```css
body {
  background: #ccc;
  margin: 0;
  overflow: hidden;
}

.toolbar {
  background: #ccc;
  width: 150px;
  height: 75px;
  padding: 5px;
}

input[type="color"], input[type="button"] {
  width: 90%;
  margin: 0 auto;
  display: block;
}

input[type="range"] {
  width: 70%;
}

span {
  position: relative;
  bottom: 5px;
}
```

```js
var canvas = document.querySelector('.myCanvas');
var width = canvas.width = window.innerWidth;
var height = canvas.height = window.innerHeight-85;
var ctx = canvas.getContext('2d');

ctx.fillStyle = 'rgb(0,0,0)';
ctx.fillRect(0,0,width,height);

var colorPicker = document.querySelector('input[type="color"]');
var sizePicker = document.querySelector('input[type="range"]');
var output = document.querySelector('.output');
var clearBtn = document.querySelector('input[type="button"]');

// covert degrees to radians
function degToRad(degrees) {
  return degrees * Math.PI / 180;
};

// update sizepicker output value

sizePicker.oninput = function() {
  output.textContent = sizePicker.value;
}

// store mouse pointer coordinates, and whether the button is pressed
var curX;
var curY;
var pressed = false;

// update mouse pointer coordinates
document.onmousemove = function(e) {
  curX = (window.Event) ? e.pageX : e.clientX + (document.documentElement.scrollLeft ? document.documentElement.scrollLeft : document.body.scrollLeft);
  curY = (window.Event) ? e.pageY : e.clientY + (document.documentElement.scrollTop ? document.documentElement.scrollTop : document.body.scrollTop);
}

canvas.onmousedown = function() {
  pressed = true;
};

canvas.onmouseup = function() {
  pressed = false;
}

clearBtn.onclick = function() {
  ctx.fillStyle = 'rgb(0,0,0)';
  ctx.fillRect(0,0,width,height);
}

function draw() {
  if(pressed) {
    ctx.fillStyle = colorPicker.value;
    ctx.beginPath();
    ctx.arc(curX, curY-85, sizePicker.value, degToRad(0), degToRad(360), false);
    ctx.fill();
  }

  requestAnimationFrame(draw);
}

draw();
```

{{ EmbedLiveSample("Examples", '100%', 600) }}

## Specifications

| Specification | Status | Comments |
| --- | --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/forms.html#button-state-(type=button) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5**](https://www.w3.org/TR/html52/forms.html#button-state-(type=button) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.input.input-button") }}

## See also

-   [`input`](/html/element/input/) and the {{ domxref("HTMLInputElement") }} interface which implements it.
-   The more modern [`button`](/html/element/button/) element.
-   [Compatibility of CSS properties](/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)