:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Getting Started](#div-gettingstarted){#gettingstarted-link .tab-link
  role="tab" aria-selected="false" aria-controls="gettingstarted"}

# OWASP DeepSecrets {#owasp-deepsecrets .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# Introduction

## OWASP DeepSecrets - a better tool for secret scanning

Yet another tool - why?

Existing tools don't really "understand" code. Instead, they mostly
parse texts.

DeepSecrets expands classic regex-search approaches with semantic
analysis, dangerous variable detection, and more efficient usage of
entropy analysis. Code understanding supports 500+ languages and formats
and is achieved by lexing and parsing - techniques commonly used in SAST
tools.

DeepSecrets also introduces a new way to find secrets: just use hashed
values of your known secrets and get them found plain in your code.

# How it Works

Under the hood story is in articles here:
<https://hackernoon.com/modernizing-secrets-scanning-part-1-the-problem>

# FAQ

## Mini-FAQ

> Pff, is it still regex-based?

Yes and no. Of course, it uses regexes and finds typed secrets like any
other tool. But language understanding (the lexing stage) and variable
detection also use regexes under the hood. So regexes is an instrument,
not a problem.

> Why don't you build true abstract syntax trees? It's academically more
> correct!

DeepSecrets tries to keep a balance between complexity and
effectiveness. Building a true AST is a pretty complex thing and simply
an overkill for our specific task. So the tool still follows the generic
SAST-way of code analysis but optimizes the AST part using a different
approach.

> I'd like to build my own semantic rules. How do I do that?

Only through the code by the moment. Formalizing the rules and moving
them into a flexible and user-controlled ruleset is in the plans.

> But what about Semgrep Secrets? Looks like you're cloning their thing.

DeepSecrets was released in April 2023 --- half a year before the
Semgrep Secrets release and I'm very glad to be followed. We share the
same ideas and principles under the hood but:

- DeepSecrets is free, Semgrep is a commercial product
- Code analysis in DeepSecrets is wider and not limited to a specific
  set of languages like in Semgrep

> I still have a question

Feel free to communicate with the
[maintainer](https://github.com/ntoskernel/deepsecrets/blob/main/pyproject.toml#L6-L8)
:::

::: {#sec-gettingstarted .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Getting Started

## Installation

From Github via pip

`$ pip install git+https://github.com/ntoskernel/deepsecrets.git`{.language-plaintext
.highlighter-rouge}

From PyPi

`$ pip install deepsecrets`{.language-plaintext .highlighter-rouge}

## Scanning

The easiest way:

`$ deepsecrets --target-dir /path/to/your/code --outformat dojo-sarif --outfile report.json`{.language-plaintext
.highlighter-rouge}

This will run a scan against `/path/to/your/code`{.language-plaintext
.highlighter-rouge} using the default configuration:

- Regex checks by a small built-in ruleset
- Semantic checks (variable detection, entropy checks)

Report in SARIF format (DefectDojo-compatible) will be saved to
`report.json`{.language-plaintext .highlighter-rouge}. If you face any
problem with SARIF format, you can fall back to internal format via
`--outfile json`{.language-plaintext .highlighter-rouge}

#### Masking secrets inside a report

As of version 1.3.0 all potential secrets inside reports are masked by
default, but you can turn this feature off via the
`--disable-masking`{.language-plaintext .highlighter-rouge} flag.

> \[!Caution\]\
> If you decide to integreate DeepSecrets to your CI pipeline with
> masking disabled, you will likely re-leak your secrets inside your CI
> artefacts.

### Fine-tuning

Run `deepsecrets --help`{.language-plaintext .highlighter-rouge} for
details.

Basically, you can (and should) use your own regex-ruleset by specifying
`--regex-rules`{.language-plaintext .highlighter-rouge}. Building
rulesets is described in the next section.

Paths to be excluded from scanning can be set via
`--excluded-paths`{.language-plaintext .highlighter-rouge}. The default
set of excluded paths is here:
`/deepsecrets/rules/excluded_paths.json`{.language-plaintext
.highlighter-rouge}, you can write your own following the format.

## Building rulesets

### Regex

The built-in ruleset for regex checks is located in
`/deepsecrets/rules/regexes.json`{.language-plaintext
.highlighter-rouge}. You're free to follow the format and create a
custom ruleset.

### HashedSecret

Example ruleset for hashed checks is located in
`/tests/fixtures/hashed_secrets.json`{.language-plaintext
.highlighter-rouge}. You're free to follow the format and create a
custom ruleset.
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-deepsecrets/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-deepsecrets){.github-button
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

### DeepSecrets Information

-  [Production Project]{style="font-size: 1.3em;"}

#### Project Classification

-  Tool

#### Audience

-  Builder
-  Defender

### Downloads or Social Links

- [PyPi](https://pypi.org/project/deepsecrets)

### Code Repository

- [DeepSecrets at Github](https://github.com/ntoskernel/deepsecrets)

### Leaders

- [Nikolai
  Khechumov](../cdn-cgi/l/email-protection.html#7c12151713101d15521714191f140911130a3c130b1d0f0c52130e1b)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
