# HTML Styleguide

*Standards for developing flexible, durable, and sustainable HTML via @mdo* 

## Table of Contents

  1. [Syntax](#syntax)
  1. [HTML5 doctype](#html5-doctype)
  1. [Language Attribute](#language-attribute)
  1. [IE Compatibility Mode](#ie-compatibility-mode)
  1. [Character encoding](#character-encoding)
  1. [CSS and JavaScript includes](#css-and-javascript-includes)
  1. [Practicality over purity](#practicality-over-purity)
  1. [Attribute order](#attribute-order)
  1. [Boolean attributes](#boolean-attributes)
  1. [Reducing markup](#reducing-markup)
  1. [JavaScript generated markup](#javascript-generated-markup)


### Syntax

* Use soft tabs with two spaces—they're the only way to guarantee code renders the same in any environment.
* Nested elements should be indented once (two spaces).
* Always use double quotes, never single quotes, on attributes.
* Don't include a trailing slash in self-closing elements—the HTML5 spec says they're optional.
* Don’t omit optional closing tags (e.g. </li> or </body>).

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company">
    <h1 class="hello-world">Hello, world!</h1>
  </body>
</html>
```
### HTML5 Doctype
Enforce standards mode and more consistent rendering in every browser possible with this simple doctype at the beginning of every HTML page.

```html
<!DOCTYPE html>
<html>
  <head>
  </head>
</html>
```
### Language Attributes
From the HTML5 spec:

Authors are encouraged to specify a lang attribute on the root html element, giving the document's language. This aids speech synthesis tools to determine what pronunciations to use, translation tools to determine what rules to use, and so forth.
Read more about the lang attribute in the spec.

Head to Sitepoint for a list of language codes.

```html
<html lang="en-us">
  <!-- ... -->
</html>
```

### IE Compatibility Mode
 
```html
 <meta http-equiv="X-UA-Compatible" content="IE=Edge">
```

### Character encoding
```html
<head>
  <meta charset="UTF-8">
</head>
```

### CSS and JavaScript includes

Per HTML5 spec, typically there is no need to specify a type when including CSS and JavaScript files as text/css and text/javascript are their respective defaults.

HTML5 spec links
Using link
Using style
Using script

```html
<!-- External CSS -->
<link rel="stylesheet" href="code-guide.css">

<!-- In-document CSS -->
<style>
  /* ... */
</style>

<!-- JavaScript -->
<script src="code-guide.js"></script>
```
### Practicality over purity
Strive to maintain HTML standards and semantics, but not at the expense of practicality. Use the least amount of markup with the fewest intricacies whenever possible.

### Attribute order
HTML attributes should come in this particular order for easier reading of code.
* class
* id, name
* data-*
* src, for, type, href, value
* title, alt
* role, aria-*

Classes make for great reusable components, so they come first. Ids are more specific and should be used sparingly (e.g., for in-page bookmarks), so they come second.

```html
<a class="..." id="..." data-toggle="modal" href="#">
  Example link
</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```
### Boolean attributes
A boolean attribute is one that needs no declared value. XHTML required you to declare a value, but HTML5 has no such requirement.

For further reading, consult the WhatWG section on boolean attributes:

The presence of a boolean attribute on an element represents the true value, and the absence of the attribute represents the false value.
If you must include the attribute's value, and you don't need to, follow this WhatWG guideline:

If the attribute is present, its value must either be the empty string or [...] the attribute's canonical name, with no leading or trailing whitespace.
In short, don't add a value.

```html
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
  <option value="1" selected>1</option>
</select>
```
### Reducing markup
Whenever possible, avoid superfluous parent elements when writing HTML. Many times this requires iteration and refactoring, but produces less HTML. Take the following example:

```html
<!-- Not so great -->
<span class="avatar">
  <img src="...">
</span>

<!-- Better -->
<img class="avatar" src="...">
```

### JavaScript generated markup
Writing markup in a JavaScript file makes the content harder to find, harder to edit, and less performant. Avoid it whenever possible.
