:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Cycle](#div-cycle){#cycle-link .tab-link role="tab"
  aria-selected="false" aria-controls="cycle"}
- [Tasks](#div-tasks){#tasks-link .tab-link role="tab"
  aria-selected="false" aria-controls="tasks"}

# OWASP Vulnerability Management Guide {#owasp-vulnerability-management-guide .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![logo](assets/images/OVMG_253.png)

## About Project

Vulnerability management is one of the most effective means of
controlling cybersecurity risk. Yet, as indicated by the wave of massive
data breaches and ransomware attacks, all too often organizations are
compromised over missing patches and misconfigurations. Vulnerability
management seeks to help organizations identify such weaknesses in its
security posture so that they can be rectified before they are exploited
by attackers. The OWASP Vulnerability Management Guide ([OWASP
VMG](OWASP-Vuln-Mgm-Guide-Jul23-2020.pdf)) project seeks to establish
guidance on the best practices that organizations can use establish a
vulnerability management program within their organization. The guide
provides in depth coverage of the full vulnerability management
lifecycle including the preparation phase, the vulnerability
identification/scanning phase, the reporting phase, and remediation
phase.

The vulnerability management guide should help to breakdown
vulnerability management process into a manageable repeatable cycles
tailored to your organizational needs. Target audience: information
security practitioners of all levels, IT professionals, and business
leaders.

------------------------------------------------------------------------

### Who is this project for?

OWASP VMG is for technical and non-technical professionals who are on
the front line of information security engineering and their managers.

Here is a self-assessment to determine whether you need a robust
vulnerability management program or not. All answers are confidential
;-)

1.  What is the size of your organization?
    - a\. 0-999
    - b\. 1K-10K
    - c\. 10K-25K+
    - d\. I don't know...
2.  Do you have a dedicated security team?
    - a\. No
    - b\. In the process of forming it
    - c\. Yes
    - d\. I don't know.
3.  Are vulnerability scans required in compliance of:
    - a\. PCI-DSS
    - b\. ISO 27001
    - c\. NIST 800-53
    - d\. I don't know!
4.  Which of these sharing services is your organization most likely to
    utilize?
    - a\. FTP
    - b\. SFTP
    - c\. HTTPS
    - d\. SMBv1
5.  When was last time you had a security incident?
    - a\. During the last three months
    - b\. During the last three weeks
    - c\. During the last three days
    - d\. I don't KNOW!!!

------------------------------------------------------------------------

##### [Results](https://github.com/lizfrenz/owasp-vuln-mngmnt/blob/master/quizz_answers.md)
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Vulnerability Management Cycle

![Cycle Image](assets/images/OWASP-Vuln-Mng-Cycle.png)
:::

::: {#sec-cycle .section .page-body .tab-hidden}

------------------------------------------------------------------------

## OWASP VMG TriCycle

![Cycle Image](assets/images/cycle_frames_v2.gif)

------------------------------------------------------------------------

Failures of vulnerability management programs are likely to result from
failures of implementation caused by the common misconception that a
working security scanner equals managing vulnerabilities in IT
environments.

Vulnerability management cannot be outsourced to a single tool or even a
set of very good tools that would seamlessly orchestrate a process
around "some findings" and "some patches".

The processes described in the guide involve decision making based on
risk practices adopted by your organization. If you are tasked with
rolling out a vulnerability management program -- this guide will help
you ask the right questions. If you are a manager or CISO, the guide
should outline how a vulnerability management program can be integrated
into your organization.

Regardless of your role, the purpose of the OWASP Vulnerability
Management Guide is to explain how continuous and complex processes can
be broken down into three essential parts, which we call cycles.

------------------------------------------------------------------------

[\[To read\]](OWASP-Vuln-Mgm-Guide-Jul23-2020.pdf)
:::

::: {#sec-tasks .section .page-body .tab-hidden}

------------------------------------------------------------------------

### Where are we?

- [ ] OVMG Update coming soon
- [x] OWASP VMG Working Group [next scheduled
  session](https://www.linkedin.com/posts/zoebraiterman_owasp-vulnerability-management-guide-thu-activity-7014045486412095488-GPzD)
- [x] Written document
- [x] Checklist (aka "bare bones")
- [x] A mind map "Vulnerability Management Cycle"
- [x] Visual aid

Track the
[project](https://github.com/lizfrenz/owasp-vuln-mngmnt/projects/1)

------------------------------------------------------------------------

### Join the cause

The simplest way to contribute to the OWASP Vulnerability Management
Guide project is adopting it!

Please read the [Guide](OWASP-Vuln-Mgm-Guide-Jul23-2020.pdf) and use
["request
feature"](https://github.com/lizfrenz/owasp-vuln-mngmnt/issues) to ask
your questions or something that would benefit you to speed up the
implementation. Fork away the OVMG on
[GitHub](https://github.com/lizfrenz/owasp-vuln-mngmnt).

------------------------------------------------------------------------

### How to collaborate

Please use the GitHub
[issue](https://github.com/lizfrenz/owasp-vuln-mngmnt/issues) to post
your ideas. OWASP is a highly dispersed team of InfoSec/IT
professionals. Let's utilize asynchronous communications to move OVMG
along. Fill out the questionnaire in the **Feature Request** template by
replacing the text in grey with your answers:

- Can you implement OWASP Vulnerability Management Guide at your place
  of work or business?

\` Please state "yes" or "no' and explain why. E.g.: "not applicable",
"I don't work in InfoSec", "too complicating". \[...\]\`

- Is your feature request related to the OWASP VMG implementation?
  Please explain how.

\` A clear and concise explanation of what the problem your request
solves. \[...\]\`

- Please describe which of VMG cycles would host your addition?
  Detection, Reporting, Remediation.

\` A clear and concise description how what you suggest could be plugged
into the existing doc. \[...\]\`

- Describe alternatives you've considered

\` A clear and concise description why alternative would NOT
work.\[...\]\`

- Did you read the OWASP VMG? What are your thoughts

\` Your honest answer goes here.\[...\]\`

## ![feature_request](assets/images/feature_request.png)

### Report Bugs

If you spot a typo or a missing link, please report to the GitHub
[issue](https://github.com/lizfrenz/owasp-vuln-mngmnt/issues). Much
appreciated!

------------------------------------------------------------------------

### Code of Conduct

Important! You must adhere to the [OWASP Code of
Conduct](../www-policy/operational/code-of-conduct.html).

------------------------------------------------------------------------

### Responsible Disclosure

Please allow some time to respond. Please check out [OWASP
Anti-Ransomware Guide
Project](../www-project-anti-ransomware-guide/migrated_content.html) and
[OWASP Secure Medical Device Deployment
Standard](../www-project-secure-medical-device-deployment-standard/migrated_content.html).

Copyright lizfrenz 2023.
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-vulnerability-management-guide/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-vulnerability-management-guide){.github-button
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

### Project Information

- Project Level: Incubator
- Project Type: Documenation
- Version 1.0

### Downloads or Social Links

- [Presentation at OWASP
  (2017)](https://github.com/lizfrenz/owasp-vuln-mngmnt/blob/master/owasp_vuln_mgmnt_08162017.pdf)
- [OWASP Vulnerability Management Guide
  (2018)](https://github.com/OWASP/www-project-vulnerability-management-guide/blob/master/owasp-vuln-mngm-guide-v1.txt)
- [OWASP Vulnerability Management Guide
  (2020)](OWASP-Vuln-Mgm-Guide-Jul23-2020.pdf)
- [OWASP Chapters All Day Event, PowerPoint
  (2020)](https://github.com/OWASP/www-project-vulnerability-management-guide/blob/master/owasp_VMG_06062020.pdf)
- [OWASP NYC Chapter at All Day Event, Recording
  (2020)](https://www.youtube.com/watch?v=mGVXYaqmybo)
- [OWASP Vulnerability Management Guide Inaugural Working Group Meeting,
  PowerPoint
  (2023)](https://github.com/OWASP/www-project-vulnerability-management-guide/blob/master/owasp_VMG_01122023.pdf)

### Code Repository

- [GitHub](https://github.com/lizfrenz/owasp-vuln-mngmnt)

### Leaders

- [Elizabeth
  Frenz](../cdn-cgi/l/email-protection.html#91f4fdf8ebf0f3f4e5f9bff3f4fdfee4e2fee7d1fee6f0e2e1bffee3f6)
- [Zoe
  Braiterman](../cdn-cgi/l/email-protection.html#1b61747e3579697a726f7e69767a755b746c7a686b3574697c)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
