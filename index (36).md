:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Specification](#div-specification){#specification-link .tab-link
  role="tab" aria-selected="false" aria-controls="specification"}

# OWASP Threat Model Library {#owasp-threat-model-library .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## Our Mission

> 🎯\
> To enable secure software architectures by democratising threat
> modeling through open-source, community engagement and AI advancements
> with clean, vetted and reliable data.

Welcome to the first, open-sourced, structured, peer-reviewed threat
modeling dataset. By generating this open-source curated dataset of
real-world threat models, we aim to:

1.  Promote and contribute to the standardization of threat modelling
2.  Contribute to the knowledge exchange between peers by reviewing
    every model.
3.  Improve the security of open-source applications by having them
    openly threat modeled. Death to security via obscurity!
4.  Create a dataset to fine-tune existing pre-trained LLMs to achieve
    more reliable threat modeling results

## News

Project will be presented at the OWASP Global AppSec in Barcelona on
29th of May 2025, along with the release of the schema! ![Join us at
OWASP Barcelona Global AppSec](assets/images/barcelona.png)

[v1.0.0](https://github.com/OWASP/www-project-threat-model-library/blob/v1.0.0/threat-model.schema.json)
of the schema is out!

## Road Map

1.  **Start Receiving Contributions!**
    - See the schema, uploaded examples and start threat modelling!
2.  **Community Engagement:**
    - Workshops and
      [hackathons](https://airtable.com/appwu5c5wt1zJXhIQ/pagnNjTTHWSMQJIer/form)
      will be organized to promote collaboration and encourage community
      involvement.
3.  **Threat Modeling for Popular Open Source Software:**
    - Initiatives will be launched to model the security threats of
      widely used open-source software.

------------------------------------------------------------------------

## FAQs

1.  **How do I contribute?**

    - Start by threat modeling! The JSON schema is available, and there
      are example threat models too. Use these examples to create your
      threat model and submit a pull request (PR) on the repository.
      Detailed contribution guidelines will be provided once the schema
      is finalized.
    - Contribute by donating - head over to the OWASP Projects Page,
      click [donate](../donate/index8492.html?reponame=owasp.github.io)
      and contributions can go directly to us if you donate more than
      \$1000!
    - Register interest for a hackathon
      [here](https://airtable.com/appwu5c5wt1zJXhIQ/pagnNjTTHWSMQJIer/form).

2.  **What is the CycloneDx TM-BOM?**

    CycloneDx TM-BOM (Threat Model Bill of Materials) is an
    industry-standard specification that provides a way to describe
    threat models. The official release is pending! Once TM-BOM is
    released, there will be another version released of the Threat Model
    Library Schema to ensure compatibility.

3.  **What tools can I use for threat modeling?**

    There are several tools available for threat modeling, both
    open-source and commercial. Some popular options include:

    - **OWASP Threat Dragon** (open-source)
    - **OWASP pytm** (open-source)
    - **Microsoft Threat Modeling Tool** (free, proprietary)

    You can use any tool you're comfortable with as long as the output
    can be converted into the JSON format once the schema is published.

4.  **How will threat models be reviewed and validated?**

    Threat models submitted to the repository will be reviewed by the
    maintainers and the community. The review process will ensure that
    the model adheres to the schema, follows best practices, and
    provides meaningful insights. Reviewers may request adjustments or
    additional details before merging.

5.  **What happens after I submit a threat model?**

    After submission, the maintainers and community will review the
    model. If it meets the standards, it will be merged into the
    library. We encourage contributors to continuously update and refine
    threat models as new information or threats emerge.

6.  **Will there be support or training for beginners in threat
    modeling?**

    Yes, we plan to offer training resources, workshops, and tutorials
    for those who are new to threat modeling. These resources will help
    you understand the key concepts, tools, and best practices in threat
    modeling.

7.  **How do I report issues or suggest improvements to the project?**

    If you encounter any issues or have suggestions for improvement, you
    can open an issue in the project's GitHub repository. Be sure to
    provide as much detail as possible, and if applicable, a proposed
    solution or workaround.

## Thank You Notes

Thank you to our sponsors from DevArmor!
![devarmor.com](assets/images/devarmor.png)

Contributions will be used for organising hackathons and community
engagement. Register interest for a hackathon
[here](https://airtable.com/appwu5c5wt1zJXhIQ/pagnNjTTHWSMQJIer/form).

Thank you to the [CycloneDX](../www-project-cyclonedx/index.html) TM-BOM
workgroup - including:

- [Steve
  Springett](../cdn-cgi/l/email-protection.html#f88b8c9d8e9dd68b888a91969f9d8c8cb8978f998b88d6978a9f)
- [Izar
  Tarandach](../cdn-cgi/l/email-protection.html#f1988b9083df859083909f95909299b1969c90989ddf929e9c)

## Contact Us

- [Petra
  Vukmirovic](../cdn-cgi/l/email-protection.html#68180d1c1a09461e1d0305011a071e010b28071f091b1846071a0f)
- [Julian
  Mehnle](../cdn-cgi/l/email-protection.html#0369766f6a626d436e666b6d6f662d6d6677)
- [OWASP #project-threat-model-library Slack
  channel](https://owasp.slack.com/archives/C08UNEQTPUY)
:::

::::: {#sec-specification .section .page-body .tab-hidden}

------------------------------------------------------------------------

# **OWASP Threat Model Library Schema Specification**

This specification explains each major element defined in the OWASP
Threat Model Library JSON Schema. It is designed to help understand the
purpose and relationships of various schema components.

## **Document Metadata**

### **`version`{.language-plaintext .highlighter-rouge}**

A structured version number (e.g., "1.0") representing the current
version of the threat model. Helps track evolution of the model over
time.

### **`$schema`{.language-plaintext .highlighter-rouge}**

Specifies the Threat Model Library schema, and its specific version, the
threat model document conforms to. For example:

`“$schema”: “https://github.com/OWASP/www-project-threat-model-library/blob/v1.0.0/threat-model.schema.json”`{.language-plaintext
.highlighter-rouge}

## **System Description**

The following top-level properties describe the system being
threat-modeled.

### **`scope`{.language-plaintext .highlighter-rouge}**

Defines the boundary and criticality of what is being modeled. This is
foundational to any threat modeling exercise, as it determines what is
included/excluded - "scoping the work" is a common terminology used in
threat modelling or other security domains like pentesting.

- `title`{.language-plaintext .highlighter-rouge}: Name of the system
  being modeled.
- `description`{.language-plaintext .highlighter-rouge}: Describes
  what's in scope and what's out of scope. This is distinct from the
  description of the system's purpose and behavior, which goes in the
  *top-level* `description`{.language-plaintext .highlighter-rouge}
  property, separate from `scope`{.language-plaintext
  .highlighter-rouge}.
- `business_criticality`{.language-plaintext .highlighter-rouge}:
  Indicates how important the system is to business operations. This
  helps prioritize risk mitigation.
- `data_sensitivity`{.language-plaintext .highlighter-rouge}: Flags if
  the system handles sensitive data types (e.g., credentials, PII).
  Critical for compliance and privacy.
- `exposure`{.language-plaintext .highlighter-rouge}:
  `internal`{.language-plaintext .highlighter-rouge} or
  `external`{.language-plaintext .highlighter-rouge} access. Externally
  facing systems are at higher risk.
- `tier`{.language-plaintext .highlighter-rouge}: Prioritization tier
  used to guide depth of modeling, risk exposure and review frequency.
  - `mission_critical:`{.language-plaintext .highlighter-rouge}
    - business criticality maximal + external
    - business critical maximal + stores sensitive data
    - business criticality high + stores sensitive data + external
  - `business_critical`{.language-plaintext .highlighter-rouge}
    - business criticality maximal and no sensitive data, internal
    - business criticality high + external but no sensitive data
    - business criticality high + sensitive data + internal
    - business criticality moderate but sensitive data + external
  - `important`{.language-plaintext .highlighter-rouge}
    - business criticality moderate and below + sensitive data
    - business criticality moderate + external, no sensitive data
  - `non_critical`{.language-plaintext .highlighter-rouge}
    - business criticality moderate and below + internal and no
      sensitive data
    - business criticality low and minimal, no sensitive data, can be
      external

### `description`{.language-plaintext .highlighter-rouge}

Describes the system's purpose and behavior and any other business
context not otherwise captured.

## **Architecture Modeling**

### **`trust_zones`{.language-plaintext .highlighter-rouge}**

Logical areas with uniform trust assumptions (e.g., public internet,
internal VPC, secure enclave). Used to define boundaries of exposure and
control. Each `component`{.language-plaintext .highlighter-rouge} is
assigned to a `trust zone`{.language-plaintext .highlighter-rouge}.

### **`trust_boundaries`{.language-plaintext .highlighter-rouge}**

Interfaces where data crosses from one trust zone to another. These are
high-risk areas in any architecture:

- Controls (e.g., authentication, access control) must be explicitly
  modeled here.
- To exist they must be defined with controls such as encryption,
  authentication, token management, session security ...
- If a trust boundary is not defined then that is a threat modelling
  finding - the root cause of potential threats!

### **`actors`{.language-plaintext .highlighter-rouge}**

These are commonly known as entities. Human or machine entities that
interact with the system. Key to identifying external threats and misuse
scenarios.

### **`components`{.language-plaintext .highlighter-rouge}**

Building blocks of the system (e.g., APIs, backend services). Central to
threat modeling since most threats target specific components.

### **`data_stores`{.language-plaintext .highlighter-rouge}**

Where data is stored or persisted. Important for identifying risks like
unauthorized access, data corruption, and backups.

### **`data_sets`{.language-plaintext .highlighter-rouge}**

Logical groupings of data. Mapping datasets to their stores helps
clarify data flow, exposure, and sensitivity.

### **`data_flows`{.language-plaintext .highlighter-rouge}**

Represents communication between components, actors, and data stores.
Data flows are key to STRIDE-based threat modeling and attack path
analysis.

### **`diagrams`{.language-plaintext .highlighter-rouge}**

Enables visual system modeling using PlantUML, Mermaid, or similar.
Essential for collaboration and reviewing architecture.

## **Security Modeling**

### **`assumptions`{.language-plaintext .highlighter-rouge}**

Things you take as true about your system (e.g., "TLS terminates at the
load balancer"). Helps clarify model boundaries and gaps.

- `description`{.language-plaintext .highlighter-rouge}: An arbitrary
  statement about the system.
- `topics`{.language-plaintext .highlighter-rouge}: A list of topics on
  which the assumption makes a statement. These topics will be of a
  standardized taxonomy and must not be arbitrarily chosen. As of right
  now, no topics have been standardized, so this property must not be
  specified.
- `validity`{.language-plaintext .highlighter-rouge}: Whether the
  assumption is `unconfirmed`{.language-plaintext .highlighter-rouge}
  (proposed/assumed by a stakeholder), `confirmed`{.language-plaintext
  .highlighter-rouge} (definitely true), or
  `rejected`{.language-plaintext .highlighter-rouge} (proposed but known
  to be false).

### **`threat_personas`{.language-plaintext .highlighter-rouge}**

Adversary profiles that inform how and why threats might be realized.
Useful for risk assessment and simulating realistic attacker behavior.

Aids in justifying and validating threats. Supports structured
persona-based modeling and possible support for integration with threat
detection tools in the future.

### **`threats`{.language-plaintext .highlighter-rouge}**

Individual threat events. Each threat references its persona, attack
vector (CAPEC), and weakness (CWE). They are the core unit of security
concern in the model.

### **`controls`{.language-plaintext .highlighter-rouge}**

Implementations of mitigations tied to specific threats. Helps ensure
your model leads to actionable recommendations.

**Effectiveness of controls:** Added as a property (e.g., minimal to
maximal scale) to assess relative control strength.

Distinguished from mitigations which is the process of implementing
countermeasures. A mitigation is the **effect** or **strategy** of
reducing risk, rather than the specific tool or mechanism.

We chose the term "controls" over alternatives like "mitigations" or
"countermeasures" because:

- controls is more aligned with risk and governance frameworks such as
  ISO 27001, NIST, CIS, and SOC2
- it reflects the language used in security audits, risk treatment
  plans, and governance reporting
- it's broader and implementation-agnostic, a control can be preventive,
  detective, or corrective - not just a technical fix
- "mitigation" often implies reduction in risk, but not full prevention
- "countermeasure" is more military/technical and less used in
  enterprise security governance
- it enables clearer mapping between threat models and control
  libraries, using controls makes it easier to link threat model outputs
  to control catalogs like NIST 800-53, OWASP ASVS, or CIS Controls

In short, "control" unifies threat modeling with risk governance and
enterprise security frameworks --- making threat models more actionable
and aligned with business processes.

### **`risks`{.language-plaintext .highlighter-rouge}**

A combination of threat, likelihood, and impact. Ties the threat model
to risk management practices and governance. Enables prioritization.

Even though risks are influenced by org-specific factors (impact
context, likelihood drivers), the schema retains this optional element
to support linkage with enterprise risk registers.

## **Extensions**

### **`extensions`{.language-plaintext .highlighter-rouge}**

Allows custom fields while enforcing namespace uniqueness. Enables
organizations to capture additional data relevant to their threat
modeling workflows. For example:

:::: {.language-json .highlighter-rouge}
::: highlight
``` highlight
{
  ...
  "extensions": {
    "example.com/owasp-threat-model-foobar-extension": {
      // Whatever schema is needed, whereas the schema should be clearly
      // documented at https://example.com/owasp-threat-model-foobar-extension.
      ...
    },
    "example.net/other-extension": {
      // Analogously.
      ...
    }
  }
}
```
:::
::::

This schema enables traceable, evidence-backed, and enterprise-ready
threat modeling for modern systems. It is optimized for structured
outputs, tool integration, and supports formal risk analysis through
linkage of threats, risks, and mitigations.

For implementation guidance or examples, refer to
<https://github.com/OWASP/www-project-threat-model-library>.
:::::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-threat-model-library/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-threat-model-library){.github-button
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

### Threat Model Library Information

- [Incubator Project](#)
- [Type of Project](#)
- [Version
  1.0.0](https://github.com/OWASP/www-project-threat-model-library/blob/v1.0.0/threat-model.schema.json)
- [Builder](#)

### Downloads or Social Links

- [Download](#)
- [Meetup](#)

### Code Repository

- [repo](https://github.com/OWASP/www-project-threat-model-library)

### Change Log

- [changes](https://github.com/OWASP/www-project-threat-model-library/releases)

### Leaders

- [Petra
  Vukmirovic](../cdn-cgi/l/email-protection.html#d2a2b7a6a0b3fca4a7b9bfbba0bda4bbb192bda5b3a1a2fcbda0b5)
- [Julian
  Mehnle](../cdn-cgi/l/email-protection.html#0268776e6b636c426f676a6c6e672c6c6776)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
