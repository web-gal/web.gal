---
title: <keygen>
tags:
  - Deprecated
  - Element
  - HTML
  - HTML5
  - Obsolete
  - Reference
  - Web
permalink: html/element/keygen
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/keygen'
obsolete: true
browserCompact: html.elements.keygen
---
{{ HTMLRef }}

The HTML `<keygen>` element exists to facilitate generation of key material, and submission of the public key as part of an [HTML form](/guide/html/forms). This mechanism is designed for use with Web-based certificate management systems. It is expected that the `<keygen>` element will be used in an HTML form along with other information needed to construct a certificate request, and that the result of the process will be a signed certificate.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), interactive content, [listed](/html/content_categories#form_listed), [labelable](/html/content_categories#form_labelable), [submittable](/html/content_categories#form_submittable), [resettable](/html/content_categories#form_resettable) [form-associated element](/html/content_categories#form-associated_content), palpable content. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | Must have a start tag and must not have an end tag. |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Permitted ARIA roles | None |
| DOM interface | {{ DOMxRef("HTMLKeygenElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ HTMLAttrDef("autofocus") }}
: This Boolean attribute lets you specify that the control should have input focus when the page loads, unless the user overrides it, for example by typing in a different control. Only one form element in a document can have the `autofocus` attribute, which is a Boolean.

{{ HTMLAttrDef("challenge") }}
: A challenge string that is submitted along with the public key. Defaults to an empty string if not specified.

{{ HTMLAttrDef("disabled") }}
: This Boolean attribute indicates that the form control is not available for interaction.

{{ HTMLAttrDef("form") }}
: The form element that this element is associated with (its _form owner_). The value of the attribute must be an `id` of a [`form`](/html/element/form/) element in the same document. If this attribute is not specified, this element must be a descendant of a [`form`](/html/element/form/) element. This attribute enables you to place `<keygen>` elements anywhere within a document, not just as descendants of their form elements.

{{ HTMLAttrDef("keytype") }}
: The type of key generated. The default value is `RSA`.

{{ HTMLAttrDef("name") }}
: The name of the control, which is submitted with the form data.

The element is written as follows:

```html
<keygen name="name" challenge="challenge string" keytype="type"
        keyparams="pqg-params">
```

The `keytype` parameter is used to specify what type of key is to be generated. Valid values are "`RSA`", which is the default, "`DSA`" and "`EC`". The `name` and `challenge` attributes are required in all cases. The `keytype` attribute is optional for RSA key generation and required for DSA and EC key generation. The `keyparams` attribute is required for DSA and EC key generation and ignored for RSA key generation. `PQG` is a synonym for `keyparams`. That is, you may specify `keyparams="pqg-params"` or `pqg="pqg-params"`.

For RSA keys, the `keyparams` parameter is not used (ignored if present). The user may be given a choice of RSA key strengths. Currently, the user is given a choice between "high" strength (2048 bits) and "medium" strength (1024 bits).

For DSA keys, the `keyparams` parameter specifies the DSA PQG parameters which are to be used in the keygen process. The value of the `pqg` parameter is the the BASE64 encoded, DER encoded Dss-Parms as specified in IETF [RFC 3279](ftp://ftp.rfc-editor.org/in-notes/rfc3279.txt). The user may be given a choice of DSA key sizes, allowing the user to choose one of the sizes defined in the DSA standard.

For EC keys, the `keyparams` parameter specifies the name of the elliptic curve on which the key will be generated. It is normally a string from the table in [nsKeygenHandler.cpp](http://mxr.mozilla.org/mozilla-central/source/security/manager/ssl/src/nsKeygenHandler.cpp?mark=179-185,187-206,208-227,229-256#177 "http://mxr.mozilla.org/mozilla-central/source/security/manager/ssl/src/nsKeygenHandler.cpp?mark=179-185,187-206,208-227,229-256#177"). (Note that only a subset of the curves named there may actually be supported in any particular browser.) If the `keyparams` parameter string is not a recognized curve name string, then a curve is chosen according to the user's chosen key strength (low, medium, high), using the curve named "`secp384r1`" for high, and the curve named "`secp256r1`" for medium keys. (Note: choice of the number of key strengths, default values for each strength, and the UI by which the user is offered a choice, are outside of the scope of this specification.)

The `<keygen>` element is only valid within an HTML form. It will cause some sort of selection to be presented to the user for selecting key size. The UI for the selection may be a menu, radio buttons, or possibly something else. The browser presents several possible key strengths. Currently, two strengths are offered, high and medium. If the user's browser is configured to support cryptographic hardware (e.g. "smart cards") the user may also be given a choice of where to generate the key, i.e., in a smart card or in software and stored on disk.

When the submit button is pressed, a key pair of the selected size is generated. The private key is encrypted and stored in the local key database.

```
PublicKeyAndChallenge ::= SEQUENCE {
    spki SubjectPublicKeyInfo,
    challenge IA5STRING
}
SignedPublicKeyAndChallenge ::= SEQUENCE {
    publicKeyAndChallenge PublicKeyAndChallenge,
    signatureAlgorithm AlgorithmIdentifier,
    signature BIT STRING
}
```

The public key and challenge string are DER encoded as `PublicKeyAndChallenge`, and then digitally signed with the private key to produce a `SignedPublicKeyAndChallenge`. The `SignedPublicKeyAndChallenge` is [Base64](/glossary/base64/) encoded, and the ASCII data is finally submitted to the server as the value of a form name/value pair, where the name is name as specified by the `name` attribute of the `keygen` element. If no challenge string is provided, then it will be encoded as an `IA5STRING` of length zero.

Here is an example form submission as it would be delivered to a CGI program by the HTTP server:

```
   commonname=John+Doe&email=doe@foo.com&org=Foobar+Computing+Corp.&
   orgunit=Bureau+of+Bureaucracy&locality=Anytown&state=California&country=US&
   key=MIHFMHEwXDANBgkqhkiG9w0BAQEFAANLADBIAkEAnX0TILJrOMUue%2BPtwBRE6XfV%0AWtKQbsshxk5ZhcUwcwyvcnIq9b82QhJdoACdD34rqfCAIND46fXKQUnb0mvKzQID%0AAQABFhFNb3ppbGxhSXNNeUZyaWVuZDANBgkqhkiG9w0BAQQFAANBAAKv2Eex2n%2FS%0Ar%2F7iJNroWlSzSMtTiQTEB%2BADWHGj9u1xrUrOilq%2Fo2cuQxIfZcNZkYAkWP4DubqW%0Ai0%2F%2FrgBvmco%3D
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5.1** The definition of 'the `<keygen>` element' in that specification](https://www.w3.org/TR/html51/sec-forms.html#the-keygen-element) | {{ Spec2("HTML5.1") }} | Initial definition. |

## Browser compatibility

{{ Compat("html.elements.keygen") }}