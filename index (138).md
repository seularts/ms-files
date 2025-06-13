:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}

# OWASP EKS Goat {#owasp-eks-goat .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![Logo](external-images/logo-1.png){width="500"}

OWASP EKS Goat is a hands-on AWS EKS security lab that teaches
real-world attack and defense techniques for AWS managed Kubernetes
clusters.

The lab simulates realistic attack paths and defense mechanisms
including misconfigured IAM roles, IRSA abuse, ECR image backdooring,
RBAC privilege escalation, and pod-to-node breakout. Participants walk
through both the offensive and defensive scenarios.

**Attack Scenarios (includes CVE-2024-23897):**

- Exploit Jenkins CVE to leak IAM credentials via IMDSv2.
- Backdoor ECR images using leaked credentials.
- Deploy compromised image into the EKS cluster.
- Escalate privileges and breakout from pod to EC2 node.
- Abuse IAM roles to exfiltrate data from S3.

**Defense Scenarios:**

- Audit cluster state using Kubescape, Kubebench, and Hadolint.
- Implement Pod Security Context and enforce policies with Kyverno
  (CEL).
- Detect runtime behavior with eBPF-based Tetragon.
- Scan and lock down ECR repositories.
- Integrate AWS GuardDuty for monitoring.

## Lab Documentation

- Full walkthrough:
  [https://eksgoat.kubernetesvillage.com](https://eksgoat.kubernetesvillage.com/)

- Alternate Link

  - In case of accessibility issues, use:\
    <https://ekssecurity.netlify.app/>

## Scenarios Covered in Documentation

#### Container & Image Security {#container--image-security}

- Docker Image and Layer Analysis
- Container Secrets Misuse
- Static Scanning with Hadolint, Dockle
- Docker Bench Security (CIS benchmark)

#### AWS ECR Exploitation

- ECR Image Scanning
- Immutable Tag Enforcement
- Credential Abuse for Private ECR Enumeration
- Backdooring Docker Images in ECR

#### AWS EKS Exploitation

- Deploying Vulnerable EKS Infrastructure
- Metadata Service Abuse (IMDSv2) to Steal Credentials
- Web App Exploitation to AWS IAM Compromise
- ECR to EKS Cluster Compromise
- Pod-to-Node Breakout in EKS
- Privilege Escalation to S3 Access and Data Exfiltration
- EC2 Instance Cleanup Post Exploit

#### Scanning & Auditing {#scanning--auditing}

- Kubescape for Compliance Assessment
- Kubebench for Node Security Benchmarking
- Hadolint for Dockerfile Linting

#### Runtime Defense & Hardening {#runtime-defense--hardening}

- Pod Security Context Enforcement
- Kyverno (CEL) Policy Enforcement in EKS
- Real-time Runtime Detection via eBPF Tetragon
- AWS GuardDuty Alerts for EKS Threats

#### Environment Lifecycle

- Infra Spin-up for Vulnerable EKS Cluster
- Complete Infra Teardown Lab

### RoadMap

- Current State:
  - Created and open-sourced hands-on labs for AWS EKS misconfigurations
    and vulnerabilities.
  - Developed detailed documentation to accompany lab walkthrough and
    theoretical concepts.
  - Implementation of initial attack & defense scenarios with IAM and
    Kubernetes RBAC.
  - Continue using mdbook for documentation.
- Short-Term Goals:
  - Transition existing infrastructure deployment scripts to Terraform.
  - Update documentation to include images and step-by-step instructions
    for each lab.
  - Expand the defensive scenarios, adding advance topics such as
    network policies.
  - Add quizes for interaction.
- Long-Term Objectives:
  - Establish a continuous integration/continuous deployment (CI/CD)
    pipeline to automate the deployment and teardown of lab
    environments.
  - Develop a community forum to facilitate participant interaction,
    knowledge sharing, and collaborative learning.
  - Integrate threat modeling lab for AWS EKS infrastructure using EKS
    Goat to detect and mitigate proactively.
:::

::: {#sec-supporters .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Project Supporters

- *You want to appear on this list?* [Donate to OWASP here!
  🤲](../donate/index8e37.html?reponame=www-project-eks-goat&title=OWASP+EKS+Goat)

> You can attribute your donation to the OWASP Juice Shop project by
> using [this
> link](../donate/index8e37.html?reponame=www-project-eks-goat&title=OWASP+EKS+Goat)
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-eks-goat/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-eks-goat){.github-button
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

### EKS Goat Information

- [Incubator Project](#)
- [Type of Project](#)
- [Version 1.0.0](#)
- [Builder](#)
- [Breaker](#)

### Documentation

- [EKS Goat](https://eksgoat.kubernetesvillage.com/)

### Code Repository

- [Github repo](https://github.com/OWASP/www-project-eks-goat)

### Change Log

- [changes](#)

### Leaders

- [Anjali
  Shukla](../cdn-cgi/l/email-protection.html#89e8e7e3e8e5e0a7fae1fce2e5e8c9e6fee8faf9a7e6fbee)
- [Divyanshu
  Shukla](../cdn-cgi/l/email-protection.html#e98d809f9088879a819cc79a819c828588a9869e889a99c7869b8e)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
