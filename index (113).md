:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Charter](#div-charter){#charter-link .tab-link role="tab"
  aria-selected="false" aria-controls="charter"}
- [Related](#div-related){#related-link .tab-link role="tab"
  aria-selected="false" aria-controls="related"}
- [Glossary](#div-glossary){#glossary-link .tab-link role="tab"
  aria-selected="false" aria-controls="glossary"}

# OWASP Machine Learning Security Top Ten {#owasp-machine-learning-security-top-ten .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![OWASP
Incubator](https://img.shields.io/badge/owasp-incubator-blue.svg)](../projects/index.html)
[![License: CC BY-SA
4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

### 📌 ***Important Information*** {#-important-information}

*The current version of this work is in draft and is being modified
frequently. Please refer to the [project
wiki](https://github.com/OWASP/www-project-machine-learning-security-top-10/wiki)
for information on how to contribute and project release timelines.*

## Overview

Welcome to the repository for the OWASP Machine Learning Security Top 10
project! The primary aim of the OWASP Machine Learning Security Top 10
project is to deliver an overview of the top 10 security issues of
machine learning systems. More information on the project scope and
target audience is available in our [project working group
charter](index.html#div-charter)

## Top 10 Machine Learning Security Risks

- [**ML01:2023 Input Manipulation
  Attack**](docs/ML01_2023-Input_Manipulation_Attack.html)
- [**ML02:2023 Data Poisoning
  Attack**](docs/ML02_2023-Data_Poisoning_Attack.html)
- [**ML03:2023 Model Inversion
  Attack**](docs/ML03_2023-Model_Inversion_Attack.html)
- [**ML04:2023 Membership Inference
  Attack**](docs/ML04_2023-Membership_Inference_Attack.html)
- [**ML05:2023 Model Theft**](docs/ML05_2023-Model_Theft.html)
- [**ML06:2023 AI Supply Chain
  Attacks**](docs/ML06_2023-AI_Supply_Chain_Attacks.html)
- [**ML07:2023 Transfer Learning
  Attack**](docs/ML07_2023-Transfer_Learning_Attack.html)
- [**ML08:2023 Model Skewing**](docs/ML08_2023-Model_Skewing.html)
- [**ML09:2023 Output Integrity
  Attack**](docs/ML09_2023-Output_Integrity_Attack.html)
- [**ML10:2023 Model Poisoning**](docs/ML10_2023-Model_Poisoning.html)

## Communication

- [Google
  Groups](https://groups.google.com/u/1/a/owasp.org/g/project-machine-learning-security-top-ten)
- [OWASP Slack](../slack/invite.html) #project-mlsec-top-10
- [Github
  Discussions](https://github.com/OWASP/www-project-machine-learning-security-top-10/discussions)
- [Meeting
  Notes](https://github.com/OWASP/www-project-machine-learning-security-top-10/issues?q=label%3Ameeting)

## Contribution

The initial version of the Machine Learning Security Top 10 list was
contributed by [Sagar
Bhure](../cdn-cgi/l/email-protection.html#3043515751421e5258454255705f475143401e5f4257)
and [Shain
Singh](../cdn-cgi/l/email-protection.html#b3c0dbd2dadd9dc0daddd4dbf3dcc4d2c0c39ddcc1d4).
The project encourages community contribution and aims to produce a high
quality deliverable reviewed by industry peers.

All contributors will need to adhere to the project's [code of
conduct](https://github.com/OWASP/www-project-machine-learning-security-top-10/blob/master/CODE_OF_CONDUCT.md).
Please [use the following
form](https://github.com/OWASP/www-project-machine-learning-security-top-10/issues/new?assignees=shsingh&labels=issues%2Fgeneral%2Cissues%2Ftriage&projects=&template=feedback-report.yaml&title=%5BFEEDBACK%5D%3A+)
for any feedback, suggestions, issues or questions.

## Getting Started

The project has a
[wiki](https://github.com/OWASP/www-project-machine-learning-security-top-10/wiki)
which provides information to get help you started on how to contribute.

## Licensing

The OWASP Machine Learning Security Project is licensed under the
[Creative Commons Attribution-ShareAlike 4.0
license](https://creativecommons.org/licenses/by-sa/4.0/) so you can
copy, distribute and transmit the work, and you can adapt it, and use it
commercially, but all provided that you attribute the work and if you
alter, transform, or build upon this work, you may distribute the
resulting work only under the same or similar license to this one.
:::

::: {#sec-charter .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Purpose

The primary aim of of the OWASP Machine Learning Security Top 10 project
is to deliver an overview of the top 10 security issues of machine
learning systems. As such, a major goal of this project is to develop a
high quality deliverable, reviewed by industry peers.

## Target Audience

The primary audience for the deliverables in this project are
developers, machine learning engineering and operational practitioners,
and application security experts. While each of these roles build,
operate and secure machine learning systems, the content is not aimed to
be exclusively at them. The content will aim to specify where
appropriate the level of understanding required for specific technology
domains.

## Scope

This project will provide an overview of the top 10 security issues of
machine learning systems. Due to the rapid adoption of machine learning
systems, there are related projects within OWASP and other
organisations, that may have narrower or broader scope than this
project. As an example, while adversarial attacks is a category of
threats, this project will also cover non-adversarial scenarios, such as
security hygiene of machine learning operational and engineering
workflows.

## Governance

The project will:

- Adhere to the OWASP [Project
  Policy](../www-policy/operational/projects.html)

Project Leaders will:

- Follow and adhere to all OWASP Foundation [policies and
  procedures](../www-policy/index.html)
- Lead the project as per the [Project Leader
  Handbook](https://ubiquitous-adventure-gnwnz4m.pages.github.io/PROJECT_LEADER-HANDBOOK_2014.pdf)

Project Contributors will:

- Follow and adhere to the [code of conduct](CODE_OF_CONDUCT.md)
:::

::: {#sec-related .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Related

**Top 10 lists related to ML and AI:**

Top10 lists similar to famous OWASP Top10 for Web Applications list, but
for AI:

- [MLSecOps Top10](https://ethical.institute/security.html)
- [OWASP Top10 for Large Language
  Models](../www-project-top-10-for-large-language-model-applications/index.html)

**Vulnerability databases:**

Catalogued vulnerabilities and risks that were present in real-world AI
and ML systems:

- [AI Vulnerability Database (AVID)](https://avidml.org/)
- [MITRE ATLAS](https://atlas.mitre.org/)
- [AI Risk Database](https://airisk.io/)

**AI/ML security guidelines:**

Various guidelines on ML and AI Security and Safety

- [OWASP AI Security and Privacy
  Guide](../www-project-ai-security-and-privacy-guide/index.html)
- [ETSI "Securing Artificial
  Intelligence](https://www.etsi.org/technologies/securing-artificial-intelligence)
- [Biden&Harris Administraton - Ensuring Safe, Secure and Trustworthy
  AI](https://www.whitehouse.gov/wp-content/uploads/2023/07/Ensuring-Safe-Secure-and-Trustworthy-AI.pdf)

**Playbooks**

Interactive playbooks useful in threat modelling and securing AI.

- [NIST AI Risk Management Framework
  Playbook](https://pages.nist.gov/AIRMF/)
- [Department of Energy AI Risk Management
  Playbook](https://www.energy.gov/ai/doe-ai-risk-management-playbook-airmp)

**Other**

All the other resources related to ML Security - threat modelling
resources, risk assessments framework, "Awesome Lists" etc.

- [Google on Red Teaming
  AI](https://services.google.com/fh/files/blogs/google_ai_red_team_digital_final.pdf)
- [Berryville ML Institute Resources for Threat Modelling
  ML](%5bhttps_/berryvilleiml.com/interactive/index.html)
- [Microsoft AI Risk assessment
  framework](https://raw.githubusercontent.com/Azure/AI-Security-Risk-Assessment/main/AI_Risk_Assessment_v4.1.4.pdf)
- [ETSI document on securing Artificial
  Intelligence](https://www.etsi.org/technologies/securing-artificial-intelligence)
- [Trusted AI Adversarial Robustness
  Toolbox](https://github.com/Trusted-AI/adversarial-robustness-toolbox)
- [ENISA - Securing Machine Learning
  Algorithms](https://www.enisa.europa.eu/publications/securing-machine-learning-algorithms)
- [Awesome AI
  Security](https://github.com/DeepSpaceHarbor/Awesome-AI-Security)
- [Awesome ML
  Security](https://github.com/trailofbits/awesome-ml-security)
- [Awesome Attacks on ML
  Privacy](https://github.com/stratosphereips/awesome-ml-privacy-attacks)
:::

::: {#sec-glossary .section .page-body .tab-hidden}

------------------------------------------------------------------------

[0](#zero) [1](#one) [2](#two) [3](#three) [4](#four) [5](#five)
[6](#six) [7](#seven) [8](#eight) [9](#nine) [A](#a) [B](#b) [C](#c)
[D](#d) [E](#e) [F](#f) [G](#g) [H](#h) [I](#i) [J](#j) [K](#k) [L](#l)
[M](#m) [N](#n) [O](#o) [P](#p) [Q](#q) [R](#r) [S](#s) [T](#t) [U](#u)
[V](#v) [W](#w) [X](#x) [Y](#y) [Z](#z)

------------------------------------------------------------------------

## 0 {#zero}

[](#)

## 1 {#one}

[](#)

## 2 {#two}

[](#)

## 3 {#three}

[](#)

## 4 {#four}

[](#)

## 5 {#five}

[](#)

## 6 {#six}

[](#)

## 7 {#seven}

[](#)

## 8 {#eight}

[](#)

## 9 {#nine}

[](#)

## A

[Adversarial attack](#adversarial_attack)\
Type of attack which seeks to trick machine learning models into
misclassifying inputs by maliciously tampering with input data

## B

[](#)

## C

[Classification](#classification)\
Process of arranging things in groups which are distinct from each
other, and are separated by clearly determined lines of demarcation

## D

[Data labeling](#data_labeling)\
Process of assigning tags or categories to each data point in a dataset

[Data poisoning](#data_poisoning)\
Type of attack that inject poisoning samples into the data

[Deep learning](#deep_learning)\
Family of machine learning methods based on artificial neural networks
with long chains of learnable causal links between actions and effects

## E

[Ensemble](#ensemble)\
See: [Model Ensemble](#model_ensemble)

## F

[](#)

## G

[](#)

## H

[](#)

## I

[Input Validation](#input_validation)\
Input validation is a technique for checking potentially dangerous
inputs in order to ensure that the inputs are safe for processing within
the code, or when communicating with other components

[Intrusion Detection Systems (IDS)](#ids)\
Security service that monitors and analyzes network or system events for
the purpose of finding, and providing real-time or near real-time
warning of, attempts to access system resources in an unauthorized
manner

[Intrusion Prevention System (IPS)](#ips)\
System that can detect an intrusive activity and can also attempt to
stop the activity, ideally before it reaches its targets

## J

[](#)

## K

[](#)

## L

[](#)

## M

[MLOps](#mlops)\
The selection, application, interpretation, deployment, and maintenance
of machine learning models within an AI-enabled system

[Model](#model)\
Detailed description or scaled representation of one component of a
larger system that can be created, operated, and analyzed to predict
actual operational characteristics of the final produced component

[Model ensemble](#model_ensemble)\
Art of combining a diverse set of learners (individual models) together
to improvise on the stability and predictive power of the model

## N

[](#)

## O

[Obfuscation](#obfuscation)\
Defense mechanism in which details of the model or training data are
kept secret by adding a large amount of valid but useless information to
a data store

[Overfitting](#overfitting)\
Overfitting is when a statistical model begins to describe the random
error in the data rather than the relationships between variables. This
occurs when the model is too complex

## P

[Perturbation](#perturbation)\
Noise added to an input sample

## Q

[](#)

## R

[Regularisation](#regularisation)\
Controlling model complexity by adding information in order to solve
ill-posed problems or to prevent overfitting

## S

[Spam](#spam)\
The abuse of electronic messaging systems to indiscriminately send
unsolicited bulk messages

## T

[](#)

## U

[Underfitting](#underfitting)\
Underfitting is when a data model is unable to capture the relationship
between the input and output variables accurately, generating a high
error rate on both the training set and unseen data

## V

[](#)

## W

[](#)

## X

[](#)

## Y

[](#)

## Z

[](#)
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-machine-learning-security-top-10/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-machine-learning-security-top-10){.github-button
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

### Machine Learning Security Top 10

This project's content is currently in draft release

Website: [https://mltop10.info](https://mltop10.info/)\
Edition: 2023\
Version: 0.3 Draft [Source
Code](https://github.com/OWASP/www-project-machine-learning-security-top-10/tree/master/docs/2023)
([Download
PDF](https://mltop10.info/OWASP-Machine-Learning-Security-Top-10.pdf))
Release Notes:
[Changelog](https://github.com/OWASP/www-project-machine-learning-security-top-10/releases)

### Project Information

- [Incubator Project]{style="font-size:1.0em;padding-left:12px;"}

#### Classification

- [Documentation]{style="font-size:1.0em;padding-left:12px;"}

#### Audience

- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}
- [Breaker]{style="font-size:1.0em;padding-left:12px;"}

### Leaders

- [Shain
  Singh](../cdn-cgi/l/email-protection.html#c8bba0a9a1a6e6bba1a6afa088a7bfa9bbb8e6a7baaf)
- [Sagar
  Bhure](../cdn-cgi/l/email-protection.html#a7d4c6c0c6d589c5cfd2d5c2e7c8d0c6d4d789c8d5c0)
- [Ben
  Kereopa-Yorke](../cdn-cgi/l/email-protection.html#a2c0c7cc8cc9dbe2cdd5c3d1d28ccdd0c5)

### Core Team

- \[Mikołaj Kowalczyk\]
- \[Aryan Kenchappagol\]
- \[Priyadharshini Parthasarathy\]

### Project Team

Thanks go to this wonderful list of [contributors](CONTRIBUTORS.html)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
