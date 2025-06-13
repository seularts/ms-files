::::::::::::::: main-wrapper
# OWASP safetypes {#owasp-safetypes .page-title}

:::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::: {#sec-main .section .page-body}
## About

Safetypes is a Java library, which aims to decrease the cost and effort
for input validation for REST APIs.

## Summary

The safetypes-java library contains special classes which can substitute
their conventional alternatives in Java and which aid input validation
on deserialization level, when used in a REST API implementation.

## Example

safetypes-java contains classes which can be used instead of String when
declaring a request parameter:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
//Spring REST example
import Word;
...
@GetMapping("/word")
public ResponseEntity<String> word(@RequestParam Word word) {
return new ResponseEntity<>(word.get(), HttpStatus.OK);
}
...
```
:::
::::

The class Word is used instead of String and in the same time Word is
constructed in such a way, that it allows only for letters, e.g. "abcd",
"test", "Todor", etc. and it throws an exception for everything else,
e.g. "this is a test", "number1", "Ol3v". From the API point of view, a
correct and expected input will be successfully processed, while
something incorrect or unexpected will lead to a Bad Request response.

## Extensibility

The library contains useful classes ready to be used, but it is also
easily extensible for customisation. Every special class in the library
is in a hierarchy extending AbstractSafeType.java. This abstract class
has two methods:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
protected abstract void accept(T value) throws TypeValidationException;
protected void validate(T value) throws TypeValidationException { }
```
:::
::::

`accept()`{.language-plaintext .highlighter-rouge} must be implemented
by any new special class, which is not part of the library, while
`validate()`{.language-plaintext .highlighter-rouge} is intended to
facilitate the customization of existing classes.

## License

OWASP Java safetypes is free to use under the [Apache License, Version
2.0](https://www.apache.org/licenses/LICENSE-2.0).
:::::::
::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-safetypes/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-safetypes){.github-button
icon="octicon-star" data-size="large" show-count="true"
aria-label="Star on GitHub"}
:::

:::::: {.sidebar role="complementary"}
::: owasp-sidebar-top
**The OWASP^®^ Foundation** works to improve the security of software
through its community-led open source software projects, hundreds of
chapters worldwide, tens of thousands of members, and by hosting local
and global conferences.
:::

### Code Repository

- [GitHub](https://github.com/OWASP/safetypes)

### Leaders

- [Todor
  Olev](../cdn-cgi/l/email-protection.html#70041f141f025e1f1c1506301f071103005e1f0217)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::
