# U.Va Library Code Styleguides

*a place to build styleguides, linters, and other reasonable approaches to code.*

## Golden Rule
```
Every line of code should appear to be written by a single person, no matter the number of contributors.
```
Enforce these, or your own, agreed upon guidelines at all times. Small or large, call out what's incorrect. 

For additions or contributions to this please submit a [pull request](https://github.com/uvalib/guides/pulls) or open an [issue](https://github.com/uvalib/guides/issues/new)
 
## Guides

  1. [CSS/SASS Styleguide](css/README.md)
  1. [HTML Styleguide](html/README.md)
  1. [Javascript Styleguide](js/README.md)
  1. [Ruby Styleguide](ruby/README.md)
  1. [NPM Tooling](tooling/README.md)
  1. [Testing](testing/README.md)
  
## Browser Support
At the present, we officially aim to support the following browsers
- IE10+, Edge
- Firefox 45+
- Chrome 43+
- Safari 8+
- Opera Mini 7.5+
- Android(Chrome 4.4, 4.3.3)
- Blackberry 10

Note: Our site can be used in other browsers, but our focus will be making the above browsers work optimally. 

### The CSS browser prefixes that you can use (each of which is specific to a different browser) are:
Android: -webkit-
Chrome: -webkit-
Firefox: -moz-
Internet Explorer: -ms-
iOS: -webkit-
Opera: -o-

Note: If you are autoprefixing browsers, the below Javascript code will provide wide coverage.
```javascript
const AUTOPREFIXER_BROWSERS = [
    'ie >= 10',
    'ie_mob >= 10',
    'ff >= 30',
    'chrome >= 34',
    'safari >= 7',
    'opera >= 23',
    'ios >= 7',
    'android >= 4.4',
    'bb >= 10'
  ];
```
## Recommendations

A survey of our current state of technologies show:

* The preprocessor of choice is SCSS (Project Blacklight -> Libra, Sufia, Geoblacklight, Tracksys, etc)
* No CSS Framework is recommended, but Bootstrap is used in the blacklight based projects.
* Ruby is the language of choice for the majority of our web application (Project Hydra)
* There are twelve stylesheets weigh in at around 282.23kb total on library.virginia.edu.
* There’s no particular “CSS architecture” in place.
* Pixels are the unit of choice, although we do have some ems/rem lying around.
* There are no basic reset styles that we use. 

## Goal 

Based on our current state, these guides should provide the following:

* Have an agreed upon “CSS architecture” in place (ie SMACSS, OOCSS, BEM, etc) for consistent naming
* Ensure we are prefixing for all major browsers at minimum the last three versions.
* Add ways to prioritize visible content using npm tooling (critical)
* Do's and don't of each language or framework
* Some tooling options for minifying, concatenating, and adding browser prefixes
* Use Normalize.css and a mix of our own reset styles

## License

Apache 2.0  
Copyright 2016 University of Virginia Library
