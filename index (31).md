::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Methodology](#div-methodology){#methodology-link .tab-link role="tab"
  aria-selected="false" aria-controls="methodology"}
- [Top10](#div-top10){#top10-link .tab-link role="tab"
  aria-selected="false" aria-controls="top10"}

# OWASP Top 10 for Business Logic Abuse {#owasp-top-10-for-business-logic-abuse .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
Modern applications rely heavily on complex business logic to manage
workflows, data, and user interactions. Unlike traditional
vulnerabilities such as SQL injection or misconfigurations, business
logic abuse exploits design flaws in how applications operate. These
attacks manipulate application workflows, state transitions, and
decision-making processes to gain unauthorized access, bypass
restrictions, or disrupt operations.

The OWASP Business Logic Abuse Top 10 complements and enhances existing
OWASP Top 10 projects by providing a cross-domain focus on business
logic vulnerabilities that transcend technology stacks. Whether applied
to web applications, APIs, mobile apps, firmware, supply chain systems,
or even hardware platforms, these issues remain universal as they target
the fundamental logic governing workflows and state transitions. By
addressing flaws like workflow step skipping, broken object-level
authorization, and business constraint bypasses, this Top 10 bridges
gaps in domain-specific lists, ensuring that logic abuse risks are
identified and mitigated regardless of the implementation medium. This
unifying approach fosters better integration of security practices
across diverse OWASP projects, strengthening overall application
security frameworks.

The OWASP Business Logic Abuse Top 10 provides a structured methodology
for identifying and prioritizing the most critical business logic
vulnerabilities. This project introduces an innovative, open approach
based on Turing machine principles, modeling applications as finite
states, transitions, and memory operations. This approach allows the
broader security community to understand, simulate, and mitigate
business logic vulnerabilities systematically.

# Purpose of the Project

- Raise Awareness: Highlight the prevalence and impact of business logic
  flaws in modern applications.
- Create a Reproducible Methodology: Provide an open framework based on
  computational principles for identifying, modeling, and analyzing
  these vulnerabilities.
- Empower Developers and Architects: Equip technical stakeholders with
  tools and insights to design secure workflows and logic.
- Define Top 10 Issues: Establish a comprehensive, prioritized list of
  the most critical business logic abuses, supported by real-world case
  studies and a computational model.

# First Release, May 30th, 2025 OWASP AppSec Global EU, Barcelona

#1: Lifecycle & Orphaned Transitions Flaws --- 13.1%

#2: Logic Bomb, Loops and Halting Issues --- 5.8%

#3: Data Type Smuggling --- 4.7%

#4: Sequential State Bypass --- 4.5%

#5: Data Oracle Exposure --- 4%

#6: Missing Roles and Permission Checks --- 2.8%

#7: Transition Validation Flaws --- 2.2%

#8: Replays of Idempotency Operations --- 1.5%

#9: Race Condition and Concurrency Issues --- 1.1%

#10: Resource Quota Violations --- \~1%

# Unique Approach

This project departs from traditional vulnerability frameworks by
leveraging the Turing machine model to define and categorize business
logic abuse. Applications are viewed as abstract machines with:

- Tape: Representing memory or data storage (e.g., databases, in-memory
  objects).
- Head: Representing data access mechanisms (e.g., API calls, queries).
- States: Representing application workflows (e.g., authentication,
  transaction approval).
- Transitions: Representing the logic that moves the application between
  states (e.g., user actions, API responses).

# Key Innovations

- Computational Foundation: Modeling vulnerabilities through Turing
  machine components provides a systematic approach to understanding
  flaws.
- Open Methodology: Every step of the vulnerability identification
  process is documented, allowing the community to validate and expand
  the research.
- Focus on Root Causes: Identifies and classifies vulnerabilities by
  their underlying computational flaws (e.g., state mismanagement,
  transition errors, memory corruption).
- Practical Outcomes: Provides actionable guidance for preventing,
  detecting, and mitigating business logic abuse.

# Methodology

## 1. Vulnerability Modeling with Turing Machines {#1-vulnerability-modeling-with-turing-machines}

Applications are modeled as Turing machines to abstract their behavior:

- Tape: Stores the application's data (e.g., user inputs, transaction
  logs).
- Head: Accesses and modifies data on the tape.
- States: Represent stages in application workflows.
- Transitions: Define how the application moves between states based on
  conditions.

Business logic vulnerabilities are identified by simulating flaws in
these components:

- Tape Issues: Data inconsistencies, corruption, or unauthorized
  modifications.
- State Issues: Improper initialization, transitions, or management of
  states.
- Transition Issues: Workflow bypasses, race conditions, or weak
  validations.

## 2. Open and Reproducible Process {#2-open-and-reproducible-process}

The project adopts a transparent research methodology:

Data Sources: Analysis of real-world incidents, penetration testing
reports, and industry publications.

Root Cause Analysis: Vulnerabilities are traced back to fundamental
issues in Turing machine components.

Community Collaboration: Contributions and feedback from the OWASP
community are integral to the project.

## 3. Vulnerability Prioritization {#3-vulnerability-prioritization}

The Top 10 vulnerabilities are selected based on:

Frequency: How often they are encountered in real-world applications.

Impact: The potential damage to confidentiality, integrity, and
availability.

Exploitability: The ease with which attackers can exploit the flaw.

## Road Map

1.  July-November 2024: analytical work for modeling business logic in
    terms of Turing machines
2.  December 2024 : mapping CVE data with issues classes by the model,
    open submissions
3.  March 2025: first draft release
4.  April 2025: public feedback gathering to decide of GA
:::

::: {#sec-methodology .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Overview

We modelled business-logic vulnerabilities as automata by mapping the
Turing-machine primitives to real-world logic flows. We chose this
framing because any business rule can be expressed as a Turing machine,
guaranteeing that our taxonomy can represent every possible logic flaw.

## Data collection and analysis

We used a large language model to validate that the proposed model
provides sufficient coverage by classifying all CVEs from 2023 to 2025,
clustered the classification results, and verified the model against a
sample of 25k GitHub security issues. This confirms that the model is
both theoretically complete and practically aligned with real-world
vulnerabilities.

The analysis was performed in four steps:

### Stage 1: Model definition and initial classification

We started with the basic groups of issues in regards to the
Turing-machine primitives: Tape, State, Transition. For each group, we
introduced around 20 root causes which resulted in 63 distinct classes
of vulnerabilities.

To validate the coverage, we used an LLM to classify all CVEs from 2023
to 2025 (76k CVE in total).

### Stage 2: Clustering of existing CVE and publicly known exploits

We took the high-confidence classifications from Stage 1 and removed any
CVE with a low correlation score. We then applied several clustering
algorithms using the initial root-cause labels as feature vectors, and
selected configurations that maximized cohesion and silhouette score.

Next, we discarded clusters whose silhouette fell below our threshold
and excluded individual CVE with low classification confidence. Similar
clusters were then merged to eliminate redundancy.

Finally, we removed clusters that are not related to business logic
attacks and are covered with other Top 10s, such as:

- Issues with cryptography.
- Security misconfigurations.
- Injection attacks.
- Improper API and asset inventory management including unsafe API
  consumption.

Result: 12 tightly-bound, high-confidence clusters of real-world
exploits.

### Stage 3: Clustering of existing CVE and publicly known exploits

As the next step, we removed any clusters whose coverage fell below our
threshold. We then added three additional clusters (Race Condition and
Concurrency Issues, Logic Bomb, Loops and Halting Issues, Resource Quota
Violations) to cover gaps in the taxonomy.

After merging similar groups and polishing definitions, we arrived at
ten cohesive clusters of vulnerabilities.

### Stage 4: Clustering of existing CVE and publicly known exploits

We recognized that CVE records emphasize impact and exploit details
rather than root-cause insights. To fill that gap, we drew a random
sample of 25k security-related issues from GitHub.

We mapped issue descriptions and tags back to our ten clusters and
measured how well each cluster captured real-world problem reports.
Based on alignment rates, we refined cluster definitions, merged or
split groups to match patterns seen in developer discussions, and
validated that our taxonomy holds outside the CVE corpus.
:::

::: {#sec-top10 .section .page-body .tab-hidden}

------------------------------------------------------------------------

# OWASP Top 10 for Business Logic Abuse -- 2025 {#owasp-top-10-for-business-logic-abuse--2025}

  Class name                                                                                                        Coverage^1^   Summary
  ----------------------------------------------------------------------------------------------------------------- ------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  [BLA1:2025 - Lifecycle & Orphaned Transitions Flaws](docs/the-top-10/lifecycle-orphaned-transitions-flaws.html)   13.1%         Orphaned sessions, tokens, or subflows persist after parent completion, leaving stale state reachable and letting attackers replay actions or corrupt business logic.
  [BLA2:2025 - Logic Bomb, Loops and Halting Issues](docs/the-top-10/logic-bomb-loops-halting-issues.html)          5.8%          Hidden triggers, unbounded loops, or unchecked recursion lacking exit conditions enable endless processing, resource exhaustion, or unintended privileged execution.
  [BLA3:2025 - Data type smuggling](docs/the-top-10/data-type-smuggling.html)                                       4.7%          Loose type checks, unsafe casting, or deserialization admit mismatched data types, subverting logic, executing code, or corrupting data.
  [BLA4:2025 - Sequential State Bypass](docs/the-top-10/sequential-state-bypass.html)                               4.5%          Weak state-machine enforcement lets attackers skip mandatory steps or combine invalid states, executing unauthorized actions outside intended progression.
  [BLA5:2025 - Data Oracle Exposure](docs/the-top-10/data-oracle-exposure.html)                                     4%            Distinct messages, UI cues, or timing variations reveal internal state, enabling enumeration, workflow mapping, and targeted attacks.
  [BLA6:2025 - Missing Roles and Permission Checks](docs/the-top-10/missing-roles-and-permission-checks.html)       2.8%          Applications omit or misapply role and permission checks, allowing unauthorized actors to perform privileged operations and escalate access.
  [BLA7:2025 - Transition Validation Flaw](docs/the-top-10/transition-validation-flaw.html)                         2.2%          Attackers bypass mandatory transactional conditions, advancing workflows without required validations and triggering incomplete or invalid operations.
  [BLA8:2025 - Replays of Idempotency Operations](docs/the-top-10/replays-of-idempotency-operations.html)           1.5%          One-time operations lack uniqueness or consumption tracking, permitting request replays that repeat effects and violate business invariants.
  [BLA9:2025 - Race Condition and Concurrency Issues](docs/the-top-10/race-condition-and-concurrency-issues.html)   1.1%          Concurrent actions on shared resources without synchronization lead to timing races, enabling inconsistent updates or unauthorized outcomes.
  [BLA10:2025 - Resource Quota Violations](docs/the-top-10/resource-quota-violations.html)                          \~1%          Absent rate limits or usage caps let attackers overconsume resource-intensive endpoints, exhausting compute, inflating costs, and degrading service availability.

^1^ Of the analyzed security issues on Github. Referer to the
Methodology section for further information.
:::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-10-for-business-logic-abuse/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-10-for-business-logic-abuse){.github-button
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

### Top 10 for Business Logic Abuse Information

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

- [Ivan
  Novikov](../cdn-cgi/l/email-protection.html#83eaf5e2edadedecf5eae8ecf5c3ecf4e2f0f3adecf1e4)
- [Silvia
  Pravida](../cdn-cgi/l/email-protection.html#ddaeb4b1abb4bceae5efebee9dbab0bcb4b1f3beb2b0)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
