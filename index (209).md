::::::::::: main-wrapper
# OWASP aegis4j {#owasp-aegis4j .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
Avoid the NEXT Log4Shell vulnerability!

The Java platform has accrued a number of features over the years. Some
of these features are no longer commonly used, but their existence
remains a security liability, providing attackers with a diverse toolkit
to leverage against Java-based systems.

It is possible to eliminate some of this attack surface area by creating
custom JVM images with
[jlink](https://docs.oracle.com/en/java/javase/17/docs/specs/man/jlink.html),
but this is not always feasible or desired. Another option is to use the
[--limit-modules](https://docs.oracle.com/en/java/javase/17/docs/specs/man/java.html)
command line parameter when running your application, but this is a
relatively coarse tool that cannot be used to disable individual
features like serialization or native process execution.

A third option is aegis4j, a Java agent which can patch key system
classes to completely disable a number of standard Java features:

- `jndi`{.language-plaintext .highlighter-rouge}: all JNDI functionality
  (`javax.naming.*`{.language-plaintext .highlighter-rouge})
- `rmi`{.language-plaintext .highlighter-rouge}: all RMI functionality
  (`java.rmi.*`{.language-plaintext .highlighter-rouge})
- `process`{.language-plaintext .highlighter-rouge}: all process
  execution functionality (`Runtime.exec()`{.language-plaintext
  .highlighter-rouge}, `ProcessBuilder`{.language-plaintext
  .highlighter-rouge})
- `httpserver`{.language-plaintext .highlighter-rouge}: all use of the
  JDK HTTP server (`com.sun.net.httpserver.*`{.language-plaintext
  .highlighter-rouge})
- `serialization`{.language-plaintext .highlighter-rouge}: all Java
  serialization (`ObjectInputStream`{.language-plaintext
  .highlighter-rouge}, `ObjectOutputStream`{.language-plaintext
  .highlighter-rouge})
- `unsafe`{.language-plaintext .highlighter-rouge}: all use of
  `sun.misc.Unsafe`{.language-plaintext .highlighter-rouge}
- `scripting`{.language-plaintext .highlighter-rouge}: all JSR 223
  scripting (`javax.script.*`{.language-plaintext .highlighter-rouge})
- `jshell`{.language-plaintext .highlighter-rouge}: all use of the Java
  Shell API (`jdk.jshell.*`{.language-plaintext .highlighter-rouge})

For more information, see the [GitHub
repository](https://github.com/gredler/aegis4j).
:::
::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-aegis4j/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-aegis4j){.github-button
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

### Project Information

Project Type: Code

Project Stage: Incubator

Project Classification: Builder, Defender

License: Apache 2.0

### Links

[Download](https://repo1.maven.org/maven2/net/gredler/aegis4j/1.1/aegis4j-1.1.jar)

[Code Repository](https://github.com/gredler/aegis4j)

[Bug Reports](https://github.com/gredler/aegis4j/issues)

[Pull Requests](https://github.com/gredler/aegis4j/pulls)

### Leaders

- [Daniel
  Gredler](../cdn-cgi/l/email-protection.html#d7b3b6b9beb2bbf9b0a5b2b3bbb2a597b0bab6bebbf9b4b8ba)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::
