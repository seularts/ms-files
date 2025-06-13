:::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP untrust {#owasp-untrust .page-title}

::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::::::: {#sec-main .section .page-body}
### Secure, Base-Level, Programming Constructs with OWASP-Untrust

#### **The Problem with Classic Libraries**

Traditional programming libraries, while powerful, were not designed
with modern security considerations. They rely on outdated assumptions:

- The executing code and compiled binaries can be trusted.
- System-level permissions (e.g., root or su) ensure safety.
- Operating systems enforce user-level safety.

These assumptions fail in server environments:

- **Untrusted Users**: Servers expose code to malicious actors.
- **Powerful Contexts**: Servers often run with elevated privileges
  (e.g., root), increasing potential damage.
- **Missing Authorization**: The operating system does not inherently
  manage user-level permissions or authorization for server users.

------------------------------------------------------------------------

#### **The OWASP-Untrust Vision**

To bridge the gap between traditional base-level constructs and secure
task-oriented constructs, OWASP-Untrust proposes a paradigm shift. This
involves creating **bounded, validated types** that enforce security
policies at the language level, ensuring safe usage patterns.

------------------------------------------------------------------------

#### **From Base Constructs to Secure Constructs**

OWASP-Untrust will provide secure alternatives to commonly misused or
risky programming constructs. The core idea is to replace unbounded,
permissive types with restricted, secure types that validate their
content at creation.

  **Classic Type**                                                                                         **Secure Alternative**                                     **Example Use Case**
  -------------------------------------------------------------------------------------------------------- ---------------------------------------------------------- ------------------------------------------------------
  `Path`{.language-plaintext .highlighter-rouge}                                                           `BoxedPath`{.language-plaintext .highlighter-rouge}        Secure file system operations confined to a sandbox.
  `String`{.language-plaintext .highlighter-rouge}                                                         `BoundedString`{.language-plaintext .highlighter-rouge}    Strings with length and content restrictions.
  `int`{.language-plaintext .highlighter-rouge} or `Integer`{.language-plaintext .highlighter-rouge}       `BoundedInteger`{.language-plaintext .highlighter-rouge}   Integer values bounded by a safe range.
  `File Name`{.language-plaintext .highlighter-rouge} (`String`{.language-plaintext .highlighter-rouge})   `Filename`{.language-plaintext .highlighter-rouge}         Validates acceptable characters for file names.
  `String`{.language-plaintext .highlighter-rouge} (free text)                                             `FreeText`{.language-plaintext .highlighter-rouge}         Ensures safe characters for freeform text.
  `String`{.language-plaintext .highlighter-rouge} (user input)                                            `UserName`{.language-plaintext .highlighter-rouge}         Enforces length and character restrictions.

------------------------------------------------------------------------

### Secure Constructs in Action

#### **1. BoxedPath** {#1-boxedpath}

Classic `Path`{.language-plaintext .highlighter-rouge} assumes full
system access, whereas `BoxedPath`{.language-plaintext
.highlighter-rouge} confines operations to a sandbox.

:::: {.language-java .highlighter-rouge}
::: highlight
``` highlight
// Classic Path
Path unrestrictedPath = Path.of("/sensitive/system/file.txt");

// Secure BoxedPath
SandboxPath sandbox = SandboxPath.boxroot("/sandbox/root");
BoxedPath securePath = sandbox.of("file.txt");
```
:::
::::

Any attempt to escape the sandbox with `BoxedPath`{.language-plaintext
.highlighter-rouge} results in a `SecurityException`{.language-plaintext
.highlighter-rouge}.

------------------------------------------------------------------------

#### **2. FreeText** {#2-freetext}

Classic strings allow any content, which can introduce injection
vulnerabilities. `FreeText`{.language-plaintext .highlighter-rouge}
restricts input to safe characters and enforces length constraints.

**Example: Task Descriptions**

:::: {.language-java .highlighter-rouge}
::: highlight
``` highlight
// Classic String
String taskDescription = "Execute this task!\n<script>alert(1);</script>";

// Secure FreeText
TaskDescription description = new TaskDescription("Execute this task!");
```
:::
::::

Attempts to include unsafe characters like
`<script>`{.language-plaintext .highlighter-rouge} or excessive lengths
are rejected at creation.

------------------------------------------------------------------------

#### **3. Filename** {#3-filename}

Classic filenames lack validation, leading to vulnerabilities with
unsafe characters or malformed names. `Filename`{.language-plaintext
.highlighter-rouge} enforces allowed characters and length constraints.

:::: {.language-java .highlighter-rouge}
::: highlight
``` highlight
// Classic Filename
String filename = "../../../../etc/passwd";

// Secure Filename
Filename secureFilename = new Filename("user-data.txt");
```
:::
::::

If the filename contains invalid characters (e.g.,
`/`{.language-plaintext .highlighter-rouge}), a
`TypeValidationException`{.language-plaintext .highlighter-rouge} is
thrown.

------------------------------------------------------------------------

#### **4. Bounded Integer** {#4-bounded-integer}

Unbounded integers can lead to overflows or logical errors.
`Times`{.language-plaintext .highlighter-rouge} ensures integer values
remain within a valid range.

:::: {.language-java .highlighter-rouge}
::: highlight
``` highlight
// Classic Integer
int times = -5; // Invalid value

// Secure Bounded Integer
Times validTimes = Times.from(10); // Enforces range [1, 100]
```
:::
::::

Values outside the defined range trigger a
`TypeValidationException`{.language-plaintext .highlighter-rouge}.

------------------------------------------------------------------------

### Advantages of OWASP-Untrust Constructs

1.  **Validation at Creation**: Unsafe data never enters the application
    logic.
2.  **Encapsulation of Constraints**: Security policies are enforced in
    reusable classes.
3.  **Minimal Code Changes**: Replacing classic constructs with secure
    equivalents requires minimal changes while drastically improving
    safety.
4.  **Self-Documenting Code**: Developers can understand constraints
    directly from type names (e.g., `FreeText`{.language-plaintext
    .highlighter-rouge}, `Filename`{.language-plaintext
    .highlighter-rouge}).

------------------------------------------------------------------------

### A Holistic Approach to Secure Programming

OWASP-Untrust's goal is to systematically replace risky constructs
across all domains:

- **File System Operations**: Use `BoxedPath`{.language-plaintext
  .highlighter-rouge} for safe and confined file access.
- **User Input Handling**: Replace unvalidated strings with bounded
  types (`UserName`{.language-plaintext .highlighter-rouge},
  `TaskName`{.language-plaintext .highlighter-rouge},
  `CommentText`{.language-plaintext .highlighter-rouge}).
- **Freeform Text**: Use `FreeText`{.language-plaintext
  .highlighter-rouge} to ensure safe and expected content.
- **Numerical Values**: Enforce limits with bounded integers
  (`Times`{.language-plaintext .highlighter-rouge},
  `BoundedInteger`{.language-plaintext .highlighter-rouge}).

By adopting OWASP-Untrust, developers gain tools to create inherently
secure applications, protecting against common classes of
vulnerabilities at the core of the programming model.
:::::::::::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::
:::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-untrust/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-untrust){.github-button
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

### Project Classification

-  Incubator Project
-  Builder
-  Code

### Downloads or Social Links

- [Download](#)
- [Meetup](#)

### Code Repository

- [GitHub](https://github.com/owasp-untrust)

### Change Log

- [changes](#)

### Leaders

- [Yariv
  Tal](../cdn-cgi/l/email-protection.html#3f465e4d5649114b5e537f50485e4c4f11504d58)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::::
