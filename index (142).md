::::::::::: main-wrapper
# OWASP Domain Protect {#owasp-domain-protect .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![OWASP
Maturity](https://img.shields.io/badge/owasp-incubator%20project-53AAE5.svg)
[![Domain Protect Github
Stars](https://img.shields.io/github/stars/domain-protect/domain-protect?label=domain-protect&style=social)](https://github.com/domain-protect/domain-protect)
[![Release
Version](https://img.shields.io/github/v/release/domain-protect/terraform-aws-domain-protect)](https://github.com/domain-protect/terraform-aws-domain-protect/releases)
[![Python
3.x](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

Attackers can take over an organisation's subdomains, using them for
reputational damage, malware hosting and credential harvesting.
Subdomain takeover by bug bounty researchers is particularly common for
organisations hosting their applications and infrastructure in the
cloud.

**Domain Protect** helps to prevent subdomain takeover, using serverless
functions in AWS or GCP to continually scan an organisation's DNS
records. When vulnerable subdomains are found, it sends alerts via Slack
or email, and optionally creates cloud resources to take over subdomains
before attackers or bug bounty researchers.

![](assets/images/slack-alerts.png){width="600"}

### Contributing

We very much welcome contributors to the project, and we're also looking
for more Project Leaders.

Working on Domain Protect is a great way to improve your skills in
Python and Terraform development, increase your knowledge and experience
of serverless across different cloud providers, and enhance your
reputation within the security community.

The first step is to get in touch with the Project Leader [Paul
Schwarzenberger](../cdn-cgi/l/email-protection.html#710110041d5f0212190610030b141f131403161403311e061002015f1e0316)
at OWASP Slack channel #project-domain-protect or by email.

### Deployment

Deploy Domain Protect to your AWS environment using Terraform

![](assets/images/domain-protect.png)

or to GCP

![](assets/images/gcp-architecture.png)

Installation options detailed in [installation
documentation](https://github.com/domain-protect/domain-protect/blob/main/docs/installation.md)

We recommended deployment using GitHub Actions with [Domain Protect
Deploy](https://github.com/domain-protect/domain-protect-deploy)

### Manual Scans

Penetration testers and those evaluating Domain Protect can use [manual
scans](https://github.com/domain-protect/domain-protect/blob/main/manual_scans/aws/README.md)
in AWS, GCP or Cloudflare to identify vulnerabilities from their laptop
with no installation of cloud infrastructure.

![](assets/images/vulnerable-eb-cnames.png)
:::
::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-domain-protect/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-domain-protect){.github-button
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

## OWASP Domain Protect {#owasp-domain-protect}

![](assets/images/domain-protect-icon.png)

#### Classification

-  Tool

#### Audience

-  Builder
-  Breaker
-  Defender

### Code Repositories

- [Domain Protect Terraform
  Module](https://github.com/domain-protect/terraform-aws-domain-protect)
- [Domain Protect
  GCP](https://github.com/domain-protect/domain-protect-gcp)
- [Domain Protect GCP
  Deploy](https://github.com/domain-protect/domain-protect-gcp-deploy)
- [Domain Protect
  Demo](https://github.com/domain-protect/domain-protect-demo)
- [Domain Protect
  (archived)](https://github.com/domain-protect/domain-protect)
- [Domain Protect Deploy
  (archived)](https://github.com/domain-protect/domain-protect-deploy)

### Terraform Module Registry

Published as a public [Terraform registry
module](https://registry.terraform.io/modules/domain-protect/domain-protect/aws/latest)

### Documentation

- [Domain Protect documentation](https://domainprotect.cloud/)
- [Domain Protect GCP
  documentation](https://github.com/domain-protect/domain-protect-gcp)

### Conferences and Meetups

[OWASP Global AppSec Dublin 2023](https://youtu.be/fLrRLmKZTvE) [OWASP
London Chapter Meetup 2022](https://youtu.be/nw6uR0glJKk) [SANS CloudSec
Next 2022](https://youtu.be/Boy8DYrC-Xw)\
[Cloud Security Meetup London 2022](https://youtu.be/4Hg9bEvxTRo)

### OWASP Project Spotlight

- [OWASP Domain Protect](https://youtu.be/KoP1X1Dyz9o)

### Social Media

- [Twitter](https://twitter.com/paulschwarzen)

### Community

- [Slack
  Channel](https://owasp.slack.com/messages/project-domain-protect)

### Leaders

- [Paul
  Schwarzenberger](../cdn-cgi/l/email-protection.html#e29283978ecc91818a95839098878c808790858790a28d95839192cc8d9085)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::
