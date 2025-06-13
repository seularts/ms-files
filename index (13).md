:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP WAF-A-MoLE {#owasp-waf-a-mole .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# Project Overview

WAF-A-MoLE is a guided mutation-based fuzzer for Web Application
Firewalls.

Given an input attack payload, it tries to produce a semantic invariant
query that bypasses detection rules for the target WAF. You can use this
tool for assessing the robustness of your product by letting WAF-A-MoLE
explore the solution space to find dangerous "blind spots" left
uncovered by the target classifier.

## WAF-A-MoLE Architecture

WAF-A-MoLE takes an initial payload and inserts it in the payload Pool,
which manages a priority queue ordered by the WAF confidence score over
each payload.

During each iteration, the head of the payload Pool is passed to the
Fuzzer, where it gets randomly mutated, by applying one of the available
mutation operators. Mutation operators Mutations operators are all
semantics-preserving and they leverage the expressive power of the
target grammar.

Below are the SQL mutation operators available in the current version of
WAF-A-MoLE.

  Mutation                  Example
  ------------------------- -----------------------------------------------
  Case Swapping             admin' OR 1=1# ⇒ admin' oR 1=1#
  Whitespace Substitution   admin' OR 1=1# ⇒ admin'\\t\\rOR\\n1=1#
  Comment Injection         admin' OR 1=1# ⇒ admin'/\*\*/OR 1=1#
  Comment Rewriting         admin'/*\*/OR 1=1# ⇒ admin'/*xyz\*/OR 1=1#abc
  Integer Encoding          admin' OR 1=1# ⇒ admin' OR 0x1=(SELECT 1)#
  Operator Swapping         admin' OR 1=1# ⇒ admin' OR 1 LIKE 1#
  Logical Invariant         admin' OR 1=1# ⇒ admin' OR 1=1 AND 0\<1#
  Number Shuffling          admin' OR 1=1# ⇒ admin' OR 2=2#

How to Contribute Questions, bug reports and pull requests are always
welcome. In particular, if you are interested in expanding this project,
we are currently interested in the following contributions:

- New WAF adapters
- New mutation operators (both for SQL and other vulnerability classes,
  XSS in particular)
- New search algorithms

## Project Road Map

🎯**August 2024 - WAF-A-MoLE becomes a OWASP project!**

This version supports SQL mutations and contains drivers for ModSecurity
and a selection of ML-based WAFs The ModSecurity driver leverages on a
custom fork for the pymodsecurity module.

🎯**March 2024 - September 2024**

Testing + Feedback + Improvements These tests will include assessing how
effective the current strategy is at bypassing ModSecurity (with a focus
on the CoreRuleSet), also by gathering real experiences from users.
Compare and add optimization algorithms to the WAF-A-MoLE strategy
selection.

🎯**September 2024: Integrate WAF-A-MoLE in the FTW framework**

FTW currently uses static payloads, we want to add dynamic payload
generation.

🎯**March 2025: XSS support**

WAF-A-MoLE includes mutation operators and strategies for Cross-Site
Scripting payloads
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-waf-a-mole/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-waf-a-mole){.github-button
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

### WAF-A-MoLE Information

- [Incubator Project](#)
- [Type of Project](#)
- [Version 0.0.0](#)
- [Builder](#)
- [Breaker](#)

### Downloads or Social Links

- [Download](#)
- [Meetup](#)

### Code Repository

- [repo](#)

### Change Log

- [changes](#)

### Leaders

- [Andrea
  Valenza](../cdn-cgi/l/email-protection.html#22634c465047430c74434e474c5843624d554351520c4d5045)
- [Luca
  Demetrio](../cdn-cgi/l/email-protection.html#96dae3f5f7b8d2f3fbf3e2e4fff9d6f9e1f7e5e6b8f9e4f1)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
