:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Contributing](#div-contributing){#contributing-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributing"}

# OWASP DevSecOps Guideline {#owasp-devsecops-guideline .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
The OWASP DevSecOps Guideline explains how we can implement a secure
pipeline and use best practices and introduce tools that we can use in
this matter. Also, the project is trying to help us promote the
shift-left security culture in our development process. This project
helps any companies of each size that have a development pipeline or, in
other words, have a DevOps pipeline. We try to draw a perspective of a
secure DevOps pipeline during this project and then improve it based on
our customized requirements.

The Ideal goal is "detect security issues (by design or application
vulnerability) as fast as possible."

![DevSecOps pipeline](assets/images/DevSecOps-pipeline.png)

### Initial steps:

At first, we consider to implement the following steps in a basic
pipeline:

- Scan git repositories for finding potential credentials leakage.
- SAST (Static Application Security Test)
- SCA (Software Composition Analysis)
- IAST (Interactive Application Security Testing)
- DAST (Dynamic Application Security Test)
- IaC Scanning (Scanning Terraform, HelmChart code to find
  misconfiguration)
- Infrastructure scanning
- Compliance check

## Latest

You can [read the latest development documents in our official GitHub
repository](https://github.com/OWASP/DevSecOpsGuideline/tree/master/documents)
or view the latest content at [latest](latest/index.html).

### Contributions

Feel free to contribute to this project; any contributors are welcome to
make a pull request on [the project
repo](https://github.com/OWASP/DevSecOpsGuideline).

### Related Project\[s\]:

- [OWASP SAMM](../www-project-samm/index.html)
- [OWASP Devsecops Maturity
  Model](../www-project-devsecops-maturity-model/index.html)
:::

::: {#sec-contributing .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Contributing

Contributing to this project is so simple. Please go to the project's
[GitHub repo](https://github.com/OWASP/DevSecOpsGuideline) and send a
new pull request.

Please do not hesitate to create an issue if you have any ideas or
recommendations.[Share your opinion or
recommandation](https://github.com/OWASP/DevSecOpsGuideline/issues)
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-devsecops-guideline/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-devsecops-guideline){.github-button
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

### DevSecOps Guideline Information

- [Documentation]{style="font-size:1.0em;padding-left:12px;"}
- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}
- [Current Version \[latest\]](latest/index.html)

### Downloads

- [Download](https://github.com/OWASP/DevSecOpsGuideline/releases)

### Code Repository

- [Github repo](https://github.com/OWASP/DevSecOpsGuideline)

### Change Log

- [changes](https://github.com/OWASP/DevSecOpsGuideline/releases)

### Leaders

- [Ali
  Yazdani](../cdn-cgi/l/email-protection.html#86e7eaefa8ffe7fce2e7e8efc6e9f1e7f5f6a8e9f4e1)
- [Milan Singh
  Thakur](../cdn-cgi/l/email-protection.html#2e4347424f406e41594f5d5e00415c49)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
