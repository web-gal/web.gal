---
title: lang
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/lang
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang'
browserCompact: html.global_attributes.lang
---
The **`lang`** [global attribute](/html/global_attributes) helps define the language of an element: the language that non-editable elements are written in, or the language that the editable elements should be written in by the user. The attribute contains a single “language tag” in the format defined in [_Tags for Identifying Languages (BCP47)_](https://www.ietf.org/rfc/bcp/bcp47.txt).

The default value of `lang` is `unknown`, therefore it is recommended to always specify this attribute with the appropriate value.

{{ EmbedInteractiveExample("pages/tabbed/attribute-lang.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

If the attribute value is the _empty string_ (`lang=""`), the language is set to _unknown_; if the language tag is not valid according to BCP47, it is set to _invalid_.

## Language tag syntax

The full BCP47 syntax is in-depth enough to mark extremely specific language dialects, but most usage is much simpler.

A language tag is made of hyphen-separated _language subtags_, where each subtag indicates a certain property of the language. The 3 most common subtags are:

Language subtag
: Required. A 2-or-3-character code that defines the basic language, typically written in all lowercase. For example, the language code for English is `en`, and the code for Badeshi is `bdz`.

Script subtag
: Optional. This subtag defines the writing system used for the language, and is always 4 characters long, with the first letter capitalized. For example, French-in-Braille is `fr-Brai` and `ja-Kana` is Japanese written with the Katakana alphabet. If the language is written in a highly typical way, like English in the Latin alphabet, there is no need to use this subtag.

Region subtag
: Optional. This subtag defines a dialect of the base language from a particular location, and is either 2 letters in ALLCAPS matching a country code, or 3 numbers matching a non-country area. For example, `es-ES` is for Spanish as spoken in Spain, and `es-013` is Spanish as spoken in Central America. “International Spanish” would just be `es`.

The script subtag precedes the region subtag if both are present — `ru-Cyrl-BY` is Russian, written in the Cyrillic alphabet, as spoken in Belarus.

To find the correct subtag codes for a language, try [the Language Subtag Lookup](https://r12a.github.io/app-subtags/).

Even if the **lang** attribute is set, it may not be taken into account, as the [**xml:lang**](/html/global_attributes/xml:lang) attribute has priority.

For the CSS pseudo-class {{ cssxref(":lang") }}, two invalid language names are different if their names are different. So while `:lang(es)` matches both `lang="es-ES"` and `lang="es-419"`, `:lang(xyzzy)` would _not_ match `lang="xyzzy-Zorp!"`.

## Accessibility

WCAG Success Criterion 3.1.1 **requires** that a page language is specified in a way which may be 'programmatically determined' (i.e. via the **`lang`** attribute).

WCAG Sucesss criterion 3.1.2 requires that pages with **parts** in different languages have the languages of those parts specified too. Again, the **`lang`** attribute is the correct mechanism for this.

The purpose of these requirements is primarily to allow assistive technologies such as screen readers to invoke the correct pronunciation.

For example, the language menu on this site (MDN) includes a **`lang`** attribute for each entry:

```
 `<div class="dropdown-container language-menu">
	<button id="header-language-menu" type="button" class="dropdown-menu-label" aria-haspopup="true" aria-owns="language-menu" aria-label="Current language is English. Choose your preferred language.">English
		<span class="dropdown-arrow-down" aria-hidden="true">▼</span>
	</button>
	<ul id="language-menu" class="dropdown-menu-items right show" aria-expanded="true" role="menu">
		<li lang="ca" role="menuitem">
			<a href="/ca/docs/Web/HTML/Global_attributes/lang" title="Catalan">
				<bdi>Català</bdi>
			</a>
		</li>
		<li lang="de" role="menuitem">
			<a href="/de/docs/Web/HTML/Globale_Attribute/lang" title="German">
				<bdi>Deutsch</bdi>
			</a>
		</li>
		<li lang="es" role="menuitem">
			<a href="/es/docs/Web/HTML/Atributos_Globales/lang" title="Spanish">
				<bdi>Español</bdi>
			</a>
		</li>
		<li lang="fr" role="menuitem">
			<a href="/fr/docs/Web/HTML/Attributs_universels/lang" title="French">
				<bdi>Français</bdi>
			</a>
		</li>
		<li lang="ja" role="menuitem">
			<a href="/ja/docs/Web/HTML/Global_attributes/lang" title="Japanese">
				<bdi>日本語</bdi>
			</a>
		</li>
		<li lang="ko" role="menuitem">
			<a href="/ko/docs/Web/HTML/Global_attributes/lang" title="Korean">
				<bdi>한국어</bdi>
			</a>
		</li>
		<li lang="pt-BR" role="menuitem">
			<a href="/pt-BR/docs/Web/HTML/Global_attributes/lang" title="Portuguese (Brazilian)">
				<bdi>Português (do&nbsp;Brasil)</bdi>
			</a>
		</li>
		<li lang="ru" role="menuitem">
			<a href="/ru/docs/Web/HTML/Global_attributes/lang" title="Russian">
				<bdi>Русский</bdi>
			</a>
		</li>
		<li lang="uk" role="menuitem">
			<a href="/uk/docs/Web/HTML/%D0%97%D0%B0%D0%B3%D0%B0%D0%BB%D1%8C%D0%BD%D1%96_%D0%B0%D1%82%D1%80%D0%B8%D0%B1%D1%83%D1%82%D0%B8/lang" title="Ukrainian">
				<bdi>Українська</bdi>
			</a>
		</li>
		<li lang="zh-CN" role="menuitem">
			<a href="/zh-CN/docs/Web/HTML/Global_attributes/lang" title="Chinese (Simplified)">
				<bdi>中文 (简体)</bdi>
			</a>
		</li>
		<li>
			<a href="https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang$locales" rel="nofollow" id="translations-add">Add a translation</a>
		</li>
	</ul>
</div>` 
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'lang' in that specification](https://html.spec.whatwg.org/multipage/dom.html#the-lang-and-xml:lang-attributes) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'lang' in that specification](https://www.w3.org/TR/html51/dom.html#the-lang-and-xml:lang-attributes) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'lang' in that specification](https://www.w3.org/TR/html52/dom.html#the-lang-and-xml:lang-attributes) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), behavior with `xml:lang` and language determination algorithm defined. It also is a true global attribute. |
| [**HTML 4.01 Specification** The definition of 'lang' in that specification](https://www.w3.org/TR/html401/struct/dirlang.html#h-8.1) | {{ Spec2('HTML4.01') }} | Supported on all elements but [`applet`](/html/element/applet/), [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`br`](/html/element/br/), [`frame`](/html/element/frame/), [`frameset`](/html/element/frameset/), [`iframe`](/html/element/iframe/), [`param`](/html/element/param/), and [`script`](/html/element/script/). |

## Browser compatibility

{{ Compat("html.global_attributes.lang") }}

## See also

-   All [global attributes](/html/global_attributes).
-   [`Content-Language` HTTP Header](/http/headers/content-language)
-   HTML {{ htmlattrxref("translate") }} attribute