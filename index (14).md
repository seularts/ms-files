::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}
- [Meetings](#div-meetings){#meetings-link .tab-link role="tab"
  aria-selected="false" aria-controls="meetings"}

# OWASP VXDF (Validated Exploitable Data Flow) Format {#owasp-vxdf-validated-exploitable-data-flow-format .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# OWASP VXDF: The Standard for Verifiable Exploit Evidence

## The Problem

Security teams are overwhelmed by vulnerability alerts from scanning
tools (SAST, DAST, SCA). Most alerts are false positives or theoretical
vulnerabilities with no practical exploit path, leading to:

- **Alert Fatigue:** Wasted time on non-critical issues
- **Delayed Remediation:** Real threats get lost in the noise
- **Developer Frustration:** Constant interruptions for non-exploitable
  issues
- **Inconsistent Reporting:** Incompatible formats across tools and
  researchers

## The Solution: VXDF

**OWASP VXDF (Validated Exploitable Data Flow)** is a standardized,
machine-readable JSON format for describing **confirmed exploitable**
code vulnerabilities with mandatory validation evidence.

### Key Features

- **Evidence-Based:** Focus on validated exploitable findings, not
  theoretical possibilities
- **Standardized Format:** Common language for describing vulnerability
  exploitation paths
- **Machine-Readable:** Enables automation in security tools and CI/CD
  pipelines
- **Actionable Intelligence:** Clear exploitation steps with concrete
  proof

### What VXDF Contains

- **Vulnerability Identification:** CWE mapping and weakness details
- **Affected Component:** Precise software/library/code segment
  information
- **Exploitation Path:** Step-by-step attack flow from source to sink
- **Validation Evidence:** Working PoC scripts, HTTP requests/responses,
  or other verifiable proof
- **Impact Assessment:** Contextualized severity and business impact

## Who Benefits

- **Security Teams:** Prioritize real threats, reduce noise
- **Developers:** Get actionable reports with clear evidence
- **Tool Vendors:** Provide high-fidelity results
- **Researchers:** Submit findings with verifiable proof
- **Organizations:** Improve security posture efficiently

## Project Resources

### Official Links

- **Project Website:** [vxdf.org](https://vxdf.org/)
- **GitHub Repository:**
  [github.com/mihir-shah99/vxdf](https://github.com/mihir-shah99/vxdf)

### Documentation & Tools {#documentation--tools}

- **Schema Specification:** [https://vxdf.org/schema-explorer](#)
- **API Documentation:** [Normative
  Schema](https://github.com/mihir-shah99/vxdf/blob/main/docs/normative-schema.json)
- **Example Files:**
  [github.com/mihir-shah99/vxdf/blob/main/example1_flow_based.vxdf](https://github.com/mihir-shah99/vxdf/blob/main/test-data/example1_flow_based.vxdf.json)

### Community & Support {#community--support}

- **Discussions:** [GitHub
  Discussions](https://github.com/mihir-shah99/vxdf/discussions)
- **Issue Tracker:** [GitHub
  Issues](https://github.com/mihir-shah99/vxdf/issues)

### Integration & Implementation {#integration--implementation}

- **Tool Integration Guide:**
  [vxdf.org/integration](https://vxdf.org/integration)
- **Developer SDKs:** Work In Progress for Python, JavaScript, Go
- **CI/CD Plugins:** Work In Progress for Jenkins, GitHub Actions,
  GitLab CI

## Get Involved

**For Contributors:**

- Review the [Contributing
  Guide](https://github.com/mihir-shah99/vxdf/blob/main/CONTRIBUTING.md)
- Check [Good First
  Issues](https://github.com/mihir-shah99/vxdf/labels/good%20first%20issue)
- Join our [Slack channel](https://owasp.slack.com/archives/C08T85605RS)

**For Tool Vendors:**

- Implement VXDF in your security products
- Contact us for integration support
- Access our [Vendor Partnership Program](https://vxdf.org/partners)

**For Organizations:**

- Pilot VXDF in your security workflow
- Share feedback and use cases
- Join our [Advisory Board](https://vxdf.org/advisory-board)
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

# VXDF Project Roadmap

## Current Status (Q2 2025)

### ✅ Completed (2024-Q1 2025) {#-completed-2024-q1-2025}

- **Foundational Schema Definition** - Base VXDF JSON schema with
  validation rules
- **Normative Schema Documentation** - Complete schema specification
  v0.1-v0.2
- **GitHub Repository & Community** - Project infrastructure and OWASP
  integration
- **Schema Validation Tools** - Production-ready validation tools and
  CLI
- **Documentation Website** - Comprehensive project documentation at
  vxdf.org

### 🔄 In Progress (Q2 2025) {#-in-progress-q2-2025}

- **OWASP Top 10 2024 Mapping** - Mapping VXDF to OWASP Top 10 2024
- **Enhancing Correlation Engine** - Enhancing the correlation engine to
  support more complex and nuanced correlations.
- **Enhanced SDK Development** - JavaScript and Go library
  implementations
- **Adding more parser support** - Adding more parser support for more
  tools - Snyk, Semgrep, OWASP ZAP etc.

## Q3 2025 Milestones

### Core Platform Enhancement

- [ ] **Multi-Language SDK Suite** - Complete JavaScript, Go, and .NET
  SDKs
- [ ] **Intelligence Engine v1.0** - Mature validation and scoring
  engine.
- [ ] **Advanced Analytics Dashboard** - Real-time vulnerability
  management metrics
- [ ] **API Gateway** - Centralized VXDF processing and validation
  service

## Contribution Opportunities

### For Developers

- **SDK Development** - Contributing to multi-language library
  implementations
- **Intelligence Engine** - Mature coreelation and validation
  improvements
- **Tool Integrations** - Building connectors for security tools and
  platforms
- **Open Source Tools** - Community-driven utilities and extensions

### For Organizations

- **Enterprise Pilots** - Production deployment and feedback programs
- **Industry Standards Work** - Contributing to standardization efforts
- **Academic Research** - University collaboration and research projects
- **Conference Speaking** - Sharing implementation experiences and use
  cases

### For Vendors

- **Certified Integrations** - Building official VXDF support into
  security tools
- **Partnership Program** - Commercial collaboration and co-marketing
  opportunities
- **Technical Advisory** - Contributing to technical direction and
  standards
- **Marketplace Presence** - Featuring integrations in VXDF ecosystem

## Get Involved {#get-involved}

**Current Priorities:**

- Join our [roadmap
  discussions](https://github.com/mihir-shah99/vxdf/discussions/categories/roadmap)
- Participate in weekly Tuesday meetings
- Contribute to [GitHub
  Issues](https://github.com/mihir-shah99/vxdf/issues) and development

**Partnership Inquiries:**

- **Enterprise Pilots:** Contact
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="9bebe9f4f1fef8efb6ede3fffddbf4ecfae8ebb5f4e9fc"}
- **Vendor Integrations:** Join
  [#project-vxdf](https://owasp.slack.com/archives/C08T85605RS)
- **Academic Research:** Submit proposals via GitHub Discussions

------------------------------------------------------------------------

*Roadmap Updated: June 2025 \| Next Review: September 2025*
:::

::: {#sec-meetings .section .page-body .tab-hidden}

------------------------------------------------------------------------

# VXDF Project Meetings

## Weekly Project Call

**Every Tuesday, 8:00 AM - 9:00 AM Pacific Time**

- **Next Meeting:** June 10, 2025 at 8:00 AM PT
- **Join:** [Google Meet](https://meet.google.com/sxb-tjao-ucp)
- **Add to Calendar:** [Google Calendar
  Event](https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=NTBxdDlwbWpmdXMxM29rYzFxanJmdGJkYjZfMjAyNTA2MTBUMTUwMDAwWiBtaWhpci5zaGFoQG93YXNwLm9yZw&tmsrc=mihir.shah%40owasp.org&scp=ALL)
- **Agenda:** [Google
  Docs](https://docs.google.com/document/d/1Hc5nmbVnyr5gExA9Z0rJSzXYhTYdQv0NBgve7UXdnHM/edit?usp=sharing)

### Time Zone Conversions

- **UTC:** 4:00 PM (Winter) / 3:00 PM (Summer)
- **Eastern:** 11:00 AM EST / 12:00 PM EDT
- **Central European:** 5:00 PM CET / 4:00 PM CEST
- **India:** 9:30 PM IST
- **Australia:** 3:00 AM AEDT / 2:00 AM AEST

## Working Groups

### Schema & Standards Working Group {#schema--standards-working-group}

- **Focus:** Schema evolution, validation rules, standards alignment

### Tool Integration Working Group

- **Focus:** SDK development, Maturing Intelligence engine, and other
  tooling

## How to Participate

1.  **Join Slack:**
    [#project-vxdf](https://owasp.slack.com/archives/C08T85605RS) for
    announcements
2.  **Add Meeting:** Use the [calendar
    link](https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=NTBxdDlwbWpmdXMxM29rYzFxanJmdGJkYjZfMjAyNTA2MTBUMTUwMDAwWiBtaWhpci5zaGFoQG93YXNwLm9yZw&tmsrc=mihir.shah%40owasp.org&scp=ALL)
    above
3.  **Review Agenda:** Check the [Google
    Doc](https://docs.google.com/document/d/1Hc5nmbVnyr5gExA9Z0rJSzXYhTYdQv0NBgve7UXdnHM/edit?usp=sharing)
    before meetings

## Meeting Resources

- **Meeting Recordings:** [GitHub
  Repository](https://github.com/mihir-shah99/vxdf/tree/main/meeting-notes)
- **Action Items:** [GitHub
  Projects](https://github.com/mihir-shah99/vxdf/projects/1)
- **Technical Support:** [GitHub
  Issues](https://github.com/mihir-shah99/vxdf/issues)
- **General Questions:** [GitHub
  Discussions](https://github.com/mihir-shah99/vxdf/discussions)

------------------------------------------------------------------------

*Weekly meetings every Tuesday 8:00 AM Pacific Time*
:::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-vxdf/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-vxdf){.github-button
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

### VXDF Information

- [Incubator Project](#)
- [Type of Project](#)
- [Version 0.1](#)
- [Builder](#)
- [Breaker](#)

### Downloads or Social Links

- [Download](#)
- [Meetup](https://owasp.slack.com/archives/C08T85605RS)

### Code Repository

- [repo](https://github.com/mihir-shah99/vxdf)

### Change Log

- [changes](https://github.com/mihir-shah99/vxdf/blob/main/CHANGELOG.md)

### Leaders

- [Mihir
  Shah](../cdn-cgi/l/email-protection.html#7a17131213085409121b123a150d1b090a5415081d)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
