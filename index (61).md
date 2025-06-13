:::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Status Update](#div-update){#update-link .tab-link role="tab"
  aria-selected="false" aria-controls="update"}
- [Philosophies](#div-philosophies){#philosophies-link .tab-link
  role="tab" aria-selected="false" aria-controls="philosophies"}
- [Survey](#div-survey){#survey-link .tab-link role="tab"
  aria-selected="false" aria-controls="survey"}

# OWASP Secure Logging Benchmark {#owasp-secure-logging-benchmark .page-title}

::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# OWASP Secure Logging Benchmark {#owasp-secure-logging-benchmark}

## Information

- [Incubator Project](#)
- [Builder](#)
- [Breaker](#)

## Downloads or Social Links

- [Blog](https://veronica-schmitt.com/category/blog-posts/)

## Introduction

The information that is often written in the log may be sensitive in
nature or give an attacker access to low-hanging fruit in terms of
exposure of endpoints or other sensitive information. The OWASP in the
Top 10 refers to "Sensitive Data Exposure" as one of the risk factors
for any application. Logging of information can be beneficial but this
is often a double-ended sword. Developers design logs with debugging in
mind. Application logs are designed by developers for developers. There
are important components to have a secure standard of logging. There is
great power within logging and taking into account designing your logs
with future breaches in mind. "When nothing goes right, just go left".
The process of detecting or dealing with an incident relies heavily on
having the information built into the application logs prior to an
incident occurring. The biggest pitfall of dealing with a potential
breach is that your logging is verbose and critical data is lost between
the noise or logs are overwritten. Another extreme is that the
information that is logged has little to no context or information
surrounding an event. When designing application logs there should be
consideration taken to not only log what is important to developers but
to consider and be kind to the future forensicator tasked with reading
your logs. Logs which are messy and noisy are often the result of not
clean code. When this occurs you have instances where log levels have
not been adequately set and data inappropriately tagged and leaked
within production logs. There should be thought placed into your logs,
and the information you put into them. There should be clear attention
given to prevent sensitive data disclosure by building in controls.

## Project Overview

A benchmarking for application logs that are based on the NIST Security
Controls taking into account debugging and system performance.

- Log levels and what they mean
- Event categories and why they are important
- Classification of data and preventions of sensitive data disclosure
- Logging Structure
- Content within log messages and identifying weaknesses within these
- Building in forensic readiness within application logs
- Log hygiene and analysis techniques
- Two weeks of training material that you can use to populate logging
  hygiene backlogs items to address within sprints.
- A guide on how to apply this within your application security team.

This project is a movement more than it is a standard. Logs are for more
than just debugging and system metrics. They give insights into code
quality and can be a symptom of problems within development teams. They
are crucial to understanding a breach, mitigation against breaches, and
information gathering for threat modeling.
:::

::: {#sec-update .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Update 04 March 2020

This project is in research phase, in which information is gathered
about logging best practises in terms of development, security and
forensic readiness. The benchmarking scoring metric has been developed
and needs to be translated into both a mobile application and web
application.

## Update 19 December 2023

Updates are being made to the content of the project. This includes the
benchmark, a survey and more guidelines around logging.
:::

::::: {#sec-philosophies .section .page-body .tab-hidden}

------------------------------------------------------------------------

# The Five Philosophies of Log Design

*TL;DR*: Effective logs should be simple, structured, and informative
without compromising sensitive information. Avoid accidental data
exposure to prevent security breaches.

## Simplicity, Structure, and Detail

A well-designed log should offer a clear understanding at a glance.
Avoid over-complication; logs aren't just data caches but sources of
necessary information. Focus on these aspects:

- **Log simplicity and structure**: Ensure uniformity across logs,
  regardless of the developer.
- **Purpose of logs**: Define whether they're for debugging, security
  events, or performance metrics. Decide this early to avoid logging
  irrelevant data.
- **Integration with systems like SIEM**: Consider how logs will be
  structured for external analysis.

## Tagging and Metadata

Be mindful of the data your application handles. Sensitive information
like personal health data (PHI) and personally identifiable information
(PII) should be treated cautiously. Consider tagging data to manage
privacy levels effectively. Example snippets:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
// Non-sensitive data
Logger().info("Smoothie name: \(smoothieName, privacy: .public)")

// Sensitive data
let userPassw : Str = getUserPassw()
Logger().info("User’s Password: \(userPassw, privacy: .secret)")
```
:::
::::

## Clean and Focused Logging

Logs grow with your application. Regular maintenance and cleaning of
logs are essential to avoid 'logging debt'. Aim for logs that are
informative and relevant. Regular benchmarking and testing of logs
should be a part of your development cycle.

## Log with Security in Mind

Assume that a security compromise can occur. Design your logs to assist
in forensic analysis and incident response. Logging should cater not
only to debugging but also to security and forensic readiness.

## Access, Storage, and Transportation of Logs

Be cautious about who can access logs and how they are stored and
transmitted. Logs should be informative yet secure, without exposing
sensitive application details or user information.

------------------------------------------------------------------------

**Acknowledgements and Inspiration**

A heartfelt thank you to Eric and all the dedicated developers and
visionaries who contributed their insights and expertise to this
project. Their collective wisdom has been invaluable in shaping these
philosophies.

This work is also inspired by the insightful narratives found in 'The
Unicorn Project' and 'The Phoenix Project', which offer profound lessons
in IT, DevOps, and software development.

Stay tuned for more in-depth discussions and explorations of these
topics. This article was first published on my website and is part of a
series dedicated to advancing understanding and best practices in the
field of log design.
:::::

::: {#sec-survey .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Participate in Our Survey: Shaping the Future of Logging Culture in Software Development

# Your Insight is Invaluable

As part of my doctoral research, I am conducting a comprehensive survey
aimed at understanding and enhancing the logging culture within the
realm of software development. This survey presents a unique opportunity
for professionals like you to share insights and experiences that are
crucial in shaping the future of how we approach logging in software
development.

# Why Your Participation Matters

**Note:** Your participation is not just a response to a survey; it is a
pivotal contribution that will influence the direction of this important
project. The insights gathered from this survey will directly impact my
PhD research, helping to develop strategies and best practices that
could redefine our approach to logging in software development.

### Survey Details

The survey covers various aspects of logging practices, challenges, and
the overall impact of logging on software development processes. It is
designed to be both insightful for participants and instrumental in
gathering meaningful data.

### How to Participate

To be a part of this transformative study, please follow the link below
to the survey. Your responses will be treated with the utmost
confidentiality and will only be used for the purposes of this research.

[Take the
Survey](https://veronicaschmitt.questionpro.com/a/TakeSurvey?tt=duf7q2d7OMoECHrPeIW9eQ%3D%3D)

Thank you for your time and valuable contribution to this research.
Together, we can pave the way for better logging practices in software
development.
:::
:::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-secure-logging-benchmark/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-secure-logging-benchmark){.github-button
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

### Information {#information}

- [Incubator Project](#)
- [Builder](#)
- [Breaker](#)

### Downloads or Social Links {#downloads-or-social-links}

- [Blog](https://veronica-schmitt.com/category/blog-posts/)

### Leaders

- [Veronica
  Schmitt](../cdn-cgi/l/email-protection.html#d2a4b7a0bdbcbbb1b3fca1b1babfbba6a692bda5b3a1a2fcbda0b5)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::
