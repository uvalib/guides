# HTML Styleguide

*Standards for developing flexible, durable, and sustainable HTML via @mdo* 

## Table of Contents

  1. [Syntax](#syntax)
  1. [HTML5 doctype](#doctype)
  1. [Language Attribute](#lang)
  1. [IE Compatibility Mode](#sass)
  1. [Character encoding](#sass)
  1. [CSS and JavaScript includes](#sass)
  1. [Practicality over purity](#sass)
  1. [Attribute order](#sass)
  1. [Boolean attributes](#sass)
  1. [Reducing markup](#sass)
  1. [JavaScript generated markup](#sass)


### Syntax

* Use soft tabs with two spaces—they're the only way to guarantee code renders the same in any environment.
* Nested elements should be indented once (two spaces).
* Always use double quotes, never single quotes, on attributes.
* Don't include a trailing slash in self-closing elements—the HTML5 spec says they're optional.
* Don’t omit optional closing tags (e.g. </li> or </body>).

```html
<!doctype html>
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
### Doctype
Enforce standards mode and more consistent rendering in every browser possible with this simple doctype at the beginning of every HTML page.

```html
<!doctype html>
<html>
  <head>
  </head>
</html>
```
