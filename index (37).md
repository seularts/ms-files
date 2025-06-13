:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Threat Modeling](#div-threatmodeling){#threatmodeling-link .tab-link
  role="tab" aria-selected="false" aria-controls="threatmodeling"}
- [Application Threat
  Modeling](#div-application-tm){#application-tm-link .tab-link
  role="tab" aria-selected="false" aria-controls="application-tm"}
- [Resources](#div-resources){#resources-link .tab-link role="tab"
  aria-selected="false" aria-controls="resources"}

# OWASP Threat Modeling Project {#owasp-threat-modeling-project .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
This is a documentation project. We provide information on threat
modeling techniques for applications of all types, with a focus on
current and emerging techniques.

Most threat model techniques answer one or more of the following
questions:

- What are we working on?
- What can go wrong?
- What are we going to do about that?
- Did we do a good enough job?

This project will gather techniques, methodologies, tools and examples.
We will group these using the four questions. This will allow people to
easily find advice they can use.

Example: if you are looking for different diagramming techniques you
will want to look for all the techniques answering the question "What
are we working on."

### Guiding principles:

This project follows a number of principles that all contributions must
adhere to:

- We are vendor, methodology and tool independent: we strive to have
  examples in as many methodologies and/or tools as possible.
- Open discussion is promoted: all topics are open for discussion with
  just one rule: don't be a jerk. If you feel information is lacking or
  missing, let us know via the OWASP #threat-modeling slack channel.
- We come to an agreement: we discuss things mainly in google docs and
  on slack, if the project leaders feel a consensus is made, we will
  publish the content to our main website. All published content can be
  changed by submitting change requests on the Github repository that
  serves the website.
:::

::: {#sec-threatmodeling .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Overview

The term "Threat Modeling" has become quite popular. Microsoft has
published their process and includes threat modeling as a key activity
in their [Security Development Lifecycle
(SDL)](https://www.microsoft.com/en-us/securityengineering/sdl).

A threat model is essentially a structured representation of all the
information that affects the security of an application. In essence, it
is a view of the application and its environment through security
glasses.

Threat modeling is a process for capturing, organizing and analyzing all
of this information. Threat modeling enables informed decision-making
about application security risk. In addition to producing a model,
typical threat modeling efforts also produce a prioritized list of
security improvements to the concept, requirements, design, or
implementation.

In 2020, a group of threat modeling practitioners, researchers and
authors got together to write the [Threat Modeling
Manifesto](https://www.threatmodelingmanifesto.org/) in order to
"...share a distilled version of our collective threat modeling
knowledge in a way that should inform, educate, and inspire other
practitioners to adopt threat modeling as well as improve security and
privacy during development". The Manifesto contains values and
principles connected to the practice and adoption of Threat Modeling, as
well as identified patterns and anti-patterns to facilitate it.

## Objectives of Threat Modeling

Threat modeling is a family of activities for improving security by
identifying threats, and then defining countermeasures to prevent, or
mitigate the effects of, threats to the system. A threat is a potential
or actual undesirable event that may be malicious (such as DoS attack)
or incidental (failure of a Storage Device). Threat modeling is a
planned activity for identifying and assessing application threats and
vulnerabilities.

## Threat Modeling Across the Lifecycle

Threat modeling is best applied continuously throughout a software
development project. The process is essentially the same at different
levels of abstraction, although the information gets more and more
granular throughout the lifecycle. Ideally, a high-level threat model
should be defined in the concept or planning phase, and then refined
throughout the lifecycle. As more details are added to the system, new
attack vectors are created and exposed. The ongoing threat modeling
process should examine, diagnose, and address these threats.

Note that it is a natural part of refining a system for new threats to
be exposed. For example, when you select a particular technology -- such
as Java for example -- you take on the responsibility to identify the
new threats that are created by that choice. Even implementation choices
such as using regular expressions for validation introduce potential new
threats to deal with.

## Threat Modeling - Four Question Framework

For a threat to an application to exist, there must be a combination of
the following where the combined likelihood and impact are important
enough to do something about. Following is the four question framework
that helps organize threat modeling:

- What are we working on?
- What can go wrong?
- What are we going to do about it?
- Did we do a good job?

There are many methods or techniques which can be used to answer each of
these questions.

There is no "right" way to evaluate the search space of possible
threats. But there are better or worse ways. Attempting to evaluate all
the possible combinations of threat agent, attack, vulnerability, and
impact is often a waste of time and effort.

The basic threat modeling process consists of the following steps. The
process of exploring the search space can be iterative and refined. It
is common to mistakenly think you should filter for "the most important
threats" early, but how can you do that before you've found them?

- **Assessment Scope** - The first step is to ask what are we working
  on? This might be as small as a sprint, or as large as a whole system.
- **Identify what can go wrong** - This can be as simple as a
  brainstorm, or as structured as using STRIDE, Kill Chains, or Attack
  Trees.
- **Identify countermeasures or manage risk** - Decide what you're going
  to do about each threat. That might be to implement a mitigation, or
  to apply the accept/transfer/eliminate approaches of risk management.
- **Assess your work** - Did you do a good enough job for the system at
  hand?

## Benefits

Done right, threat modeling provides a clear "line of sight" across a
project that justifies security efforts. The threat model allows
security decisions to be made rationally, with all the information on
the table. The alternative is to make knee-jerk security decisions with
no support. The threat modeling process naturally produces an assurance
argument that can be used to explain and defend the security of an
application. An assurance argument starts with a few high level claims,
and justifies them with either sub-claims or evidence.

## Threat Modeling Tooling

There is a wide variety of tools that can support threat modeling,
including [OWASP Threat
Dragon](../www-project-threat-dragon/index.html), [OWASP
pytm](../www-project-pytm/index.html), and [OWASP
Threatspec](../www-project-threatspec/index.html).

There are also a number of other tools available, both Open Source and
commercial.
:::

::: {#sec-application-tm .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Application Threat Modeling

Threat modeling works to identify, communicate, and understand threats
and mitigations within the context of protecting something of value.

Threat modeling can be applied to a wide range of things, including
software, applications, systems, networks, distributed systems, things
in the Internet of things, business processes, etc. There are very few
technical products which cannot be threat modeled; more or less
rewarding, depending on how much it communicates, or interacts, with the
world. Threat modeling can be done at any stage of development,
preferably early - so that the findings can inform the design.

### What

Most of the time, a threat model includes:

- A description / design / model of what you're worried about
- A list of assumptions that can be checked or challenged in the future
  as the threat landscape changes
- A list of potential threats to the system
- A list of actions to be taken for each threat
- A way of validating the model and threats, and verification of success
  of actions taken

Our motto is: Threat modeling: the sooner the better, but never too
late.

### Why

The inclusion of threat modeling in the SDLC can help

- Build a secure design
- Efficient investment of resources; appropriately prioritize security,
  development, and other tasks
- Bring Security and Development together to collaborate on a shared
  understanding, informing development of the system
- Identify threats and compliance requirements, and evaluate their risk
- Define and build required controls.
- Balance risks, controls, and usability
- Identify where building a control is unnecessary, based on acceptable
  risk
- Document threats and mitigation
- Ensure business requirements (or goals) are adequately protected in
  the face of a malicious actor, accidents, or other causes of impact
- Identification of security test cases / security test scenarios to
  test the security requirements

### 4 Questions {#4-questions}

Most threat model methodologies answer one or more of the following
questions in the technical steps which they follow:

#### What are we building?

As a starting point you need to define the scope of the Threat Model. To
do that you need to understand the application you are building,
examples of helpful techniques are:

- Architecture diagrams
- Dataflow transitions
- Data classifications
- You will also need to gather people from different roles with
  sufficient technical and risk awareness to agree on the framework to
  be used during the Threat modeling exercise.

#### What can go wrong?

This is a "research" activity in which you want to find the main threats
that apply to your application. There are many ways to approach the
question, including brainstorming or using a structure to help think it
through. Structures that can help include STRIDE, Kill Chains, CAPEC and
others.

#### What are we going to do about that?

In this phase you turn your findings into specific actions. See
[Threat_Modeling_Outputs](Threat_Modeling_Outputs.html)

#### Did we do a good enough job?

Finally, carry out a retrospective activity over the work you have done
to check quality, feasibility, progress, and/or planning.

### Process

The technical steps in threat modeling involve answering questions:

- What are we working on - What can go wrong - What will we do with the
  findings
- Did we do a good job? The work to answer these questions is embedded
  in some sort of process, ranging from incredibly informal Kanban with
  Post-its on the wall to strictly structured waterfalls.

The effort, work, and timeframes spent on threat modeling relate to the
process in which engineering is happening and products/services are
delivered. The idea that threat modeling is waterfall or 'heavyweight'
is based on threat modeling approaches from the early 2000s. Modern
threat modeling building blocks fit well into agile and are in wide use.

#### When to Threat Model

When the system changes, you need to consider the security impact of
those changes. Sometimes those impacts are not obvious.

Threat modeling integrates into Agile by asking "what are we working on,
now, in this sprint/spike/feature?"; trying to answer this can be an
important aspect of managing security debt, but trying to address it
per-sprint is overwhelming. When the answer is that the system's
architecture isn't changing, no new processes or dataflows are being
introduced, and there are no changes to the data structures being
transmitted, then it is unlikely that the answers to 'what can go wrong'
will change. When one or more of those changes, then it's useful to
examine what can go wrong as part of the current work package, and to
understand designs trade-offs you can make, and to understand what
you're going to address in this sprint and in the next one. The question
of did we do a good job is split: the "did we address these threats" is
part of sprint delivery or merging, while the broader question is an
occasional saw-sharpening task.

After a security incident, going back and checking the threat models can
be an important process.

#### Threat Modeling: Engagement Versus Review

Threat modeling at a whiteboard can be a fluid exchange of ideas between
diverse participants. Using the whiteboard to construct a model that
participants can rapidly change based on identified threats is a
high-return activity. The models created there (or elsewhere) can be
meticulously transferred to a high-quality archival representation
designed for review and presentation. Those models are useful for
documenting what's been decided and sharing those decisions widely
within an organization. These two activities are both threat modeling,
yet quite different.

#### Validating Assumptions
:::

::: {#sec-resources .section .page-body .tab-hidden}

------------------------------------------------------------------------

The best resource to start learning about threat modeling or improving
your existing process, is the [Threat Modeling
Manifesto](https://www.threatmodelingmanifesto.org/). This Manifesto was
created by a group of leading threat modeling professionals.

## Related OWASP Projects

- [OWASP Threat Model
  Cookbook](../www-project-threat-model-cookbook/index.html)
- [OWASP Threat Dragon](../www-project-threat-dragon/index.html)
- [OWASP PyTM](../www-project-pytm/index.html)
- [Threatspec](https://threatspec.org/)
- [OWASP Ontology Driven Threat
  Modeling](../www-project-ontology-driven-threat-modeling-framework/index.html)

## Additional References

- [Adam Shostack - "Threat Modeling: Designing for
  Security"](https://shostack.org/books/threat-modeling-book)
- [Tony Uceda-Velez - "Risk Centric Threat Modeling: Process for Attack
  Simulation and Threat
  Analysis"](https://versprite.com/author/tony-ucedavelez/)
- [Brook Schoenfield - "Securing Systems: Applied Security Architecture
  and Threat Modeling"](http://brookschoenfield.com/?page_id=245)
- [Microsoft's Security Development
  Process](https://www.microsoft.com/en-us/securityengineering/sdl)
- [Microsoft Threat Modeling &
  Tool](https://www.microsoft.com/en-us/securityengineering/sdl/threatmodeling)
- [SAFECode - "Tactical Threat
  Modeling"](https://safecode.org/tactical-threat-modeling/)
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-threat-model/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-threat-model){.github-button
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

### OWASP Threat Model Information

- [Documentation Project](#)
- [Builder](#)

### Downloads or Social Links

- [Download](#)
- [Meetup](#)

### Code Repository

- [repo](https://github.com/OWASP/www-project-threat-model/)

### Change Log

- [changes](#)

### Leaders

- [Avi
  Douglen](../cdn-cgi/l/email-protection.html#a2c3d4cb8cc6cdd7c5cec7cce2cdd5c3d1d28ccdd0c5)
- [Steven
  Wierckx](../cdn-cgi/l/email-protection.html#e7949382918289c9908e8295848c9fa78890869497c9889580)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
