:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP Agent Observability Standard {#owasp-agent-observability-standard .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
  --------------------------------------------------------------------------- --------------------------------------------
  The project is available here: \[https://trustworthyagents.github.io/AOS/   https://trustworthyagents.github.io/AOS/\]
  --------------------------------------------------------------------------- --------------------------------------------

AI agents make critical decisions autonomously. They collaborate,
execute code, and access sensitive data. But they operate as black
boxes. Enterprises can't trust what they can't see.

AOS introduces a standard way to introduce middleware into agent systems
to steer its behavior. It transforms opaque agents into transparent,
controllable systems.

AOS requires agents to be instrumentable, traceable and inspectable.

- Instrumentable: we can hook into agent execution and steer it in the
  right direction. We can put hard controls around agents and define
  their scope of action. Apply centralized enterprise logic, be it
  security, compliance or legal, uniformly across agent platforms.
  Prevent or modify behavior to comply.
- Traceable: we know what the agent did and why. We can trace back any
  action taken to the reasoning behind it and the originating task. Even
  if the thread goes through multiple agents and software systems. In
  case of compromise, we can identify and remediate the root cause.
- Inspectable: we don't have to guess what's inside. Which tools, models
  and capabilities are being used. What software version is running and
  who built it. What are the services behind them, and which data they
  can access. Must dynamically adapt to account for rapid changes in
  agent components.

AOS works by extending other existing standards. MCP and A2A for
instrumentation. OCSF and OpenTelemetry for Tracing. CycloneDX, SWID and
SPDX for inspectability.

AOs is already being adopted by major AI agent platform vendors, as they
react to enterprise needs.

### Road Map

Private release (Q2 2025, already happened)

- Create a draft protocol specification
- Begin collaborative implementation work with agent platform vendors
- Collect security community input
- Create draft spec for AgBOM
- Onboard founding members

Public release, collaboration with agent platform (Q3 2025)

- Ship a first public draft
- Public call for contribution
- Develop integration modules for popular MCP and A2A implementation
- Partner with more AI agent platform vendors for implementation

Target individual devs (Q4 2025)

- Develop testing framework for AOS-compliant agents
- Detailed implementation guides
- Develop integration modules for popular agent frameworks
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
[Watch](https://github.com/owasp/www-project-agent-observability-standard-2/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-agent-observability-standard-2){.github-button
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

### Agent Observability Standard Information

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

- [Michael
  Bargury](../cdn-cgi/l/email-protection.html#2d40444e454c4841034f4c5f4a585f546d425a4c5e5d03425f4a)
- [Ory
  Segal](../cdn-cgi/l/email-protection.html#eb868288838a8e87c5898a998c9e9992ab849c8a989bc584998c)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
