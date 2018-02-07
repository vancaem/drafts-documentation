---
title: Scripting
---

Drafts actions may contain [Script steps]({{ site.baseurl }}/actions/steps/script) which execute Javascript. Drafts uses [JavaScriptCore](https://developer.apple.com/documentation/javascriptcore), which Apple ships with the host platform, and all standard libraries are available to work with native Javascript data types.  Note that this is not a browser hosted Javascript environment and will not have access to the same extensions to the language provided by browsers, like the Document Object Model and XHTTP objects.

Drafts extends the Javascript environment with many objects to allow manipulation of drafts, the editor - and to interact with system and online services. Details on the objects currently available in Drafts scripting environment is maintained at our Wiki:

- **[Drafts Scripting Reference](https://github.com/agiletortoise/drafts-documentation/wiki)**

Check back and watch release notes because we are always expanding the scripting capabilities of Drafts.

### Learning Javascript

If you are new to Javascript, learning the basic can be easy, recommend taking a look at the following resources to get started:

- [Code Academy](https://www.codecademy.com/catalog/language/javascript)
- [Code School](https://www.codeschool.com/learn/javascript)
- [w3schools.com Javascript reference](https://www.w3schools.com/jsref/default.asp)
