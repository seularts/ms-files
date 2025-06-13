::::::::::: main-wrapper
# OWASP Ontology Driven Threat Modeling Framework {#owasp-ontology-driven-threat-modeling-framework .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## What is OdTM?

OWASP Ontology-driven Threat Modelling (OdTM) framework is a set of
means for implementation of an ontological approach into automatic
threat modelling of computer systems.

### Description

The OdTM framework enables formalization of security related knowledge
(architectural components and associated threats and countermeasures) of
different computer system types (architectural domains) in form of
domain-specific threat models, or ontologies in the OWL (Web Ontology
language) format. That gives a useful way to collect the knowledge by
security professionals and share with software architects, developers
and users. Also, the framework allows to describe a computer system in
term of a domain-specific threat model with a DFD (data flow diagram),
and use automatic reasoning procedures to build a threat model (relevant
threats and countermeasures) of the system. Such a feature makes it
easily automation of the threat modelling process.

Our goals are:

- to maintain a base threat model (ontology) that enables creation of
  domain-specific threat models;
- to create different domain-specific threat models (for Web
  applications, Cloud computing, Internet of Things etc.);
- to develop an ontology-driven threat rule engine, and a GUI editor of
  domain-specific threat models.

### Roadmap

**Vision**: Involve the ontology-driven approach into automatic threat
modelling for collecting, sharing and usage of the strict
security-related knowledge through creation of domain-specific threat
models and development of software tools.

**Initial plan**:

- Milestone 1: To implement a threat rule engine (OdTM Server) as a
  remote JSON API service.
- Milestone 2: To develop various domain-specific threat models (the
  cloud computing domain as the first step).
- Milestone 3: To implement software modules, providing integration of
  OdTM Server with GUI threat modelling tools.
- Milestone 4: To implement a GUI editor of domain-specific threat
  models (OdTM Studio).

**Technology**: Knowledge engineering, OWL (Web Ontology Language),
Java, the OWL API library, the Jackson JSON library.

### Related Projects

from OWASP:

- [OWASP Threat Dragon](../www-project-threat-dragon/index.html)
- [OWASP Threat Model
  Cookbook](../www-project-threat-model-cookbook/index.html)
- [OWASP PyTM (Pythonic Threat
  Modeling)](../www-project-pytm/index.html)

third-party:

- [A set of semantic data flow
  diagrams](https://github.com/nets4geeks/DockerComposeDataset)
- [ACCTP catalog](https://nets4geeks.github.io/acctp/)
- [OWL API](https://github.com/owlcs/owlapi)
- [HermiT Reasoner](http://www.hermit-reasoner.com/)

### Getting Involved

Everyone is welcome and encouraged to participate in the OWASP OdTM
project with contributions (github pulls, issues, clons etc.),
collaboration, feedback, and promotion.
:::
::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-ontology-driven-threat-modeling-framework/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-ontology-driven-threat-modeling-framework){.github-button
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

![](assets/images/common/owasp_level_incubator.svg){width="66"}

![Defenders](assets/images/common/owasp_defenders.svg)
![Builders](assets/images/common/owasp_builders.svg) ![Tool
Project](assets/images/common/owasp_tool_project.svg)

### Code repository

- [github](https://github.com/OWASP/OdTM/)

### Documentation

- [guide](https://github.com/OWASP/OdTM/blob/master/guide/README.md)

### Cloud threat model (ACCTP)

- version 0.60 (November 2021)
- [description](https://github.com/OWASP/OdTM/blob/master/docs/ODTMACCTP.md)
- [OWL file](https://github.com/OWASP/OdTM/blob/master/OdTMACCTP.owl)

### Integrated model

- ATT&CK, CAPEC & CWE
- [description](https://github.com/OWASP/OdTM/blob/master/docs/IM.md)

### Base Threat Model

- version 0.60 (Nov. 2021)
- [description](https://github.com/OWASP/OdTM/blob/master/docs/BASEMODEL.md)
- [OWL
  file](https://github.com/OWASP/OdTM/blob/master/OdTMBaseThreatModel.owl)

### Community

- [slack channel (OWASP)](https://owasp.slack.com/archives/C01MUFTB0HG)

### License

- MIT

### Leaders

- [Andrei
  Brazhuk](../cdn-cgi/l/email-protection.html#bcddd2d8ced9cb92deceddc6d4c9d7fcdbd1ddd5d092dfd3d1)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::
