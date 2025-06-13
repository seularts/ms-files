::::::::::: main-wrapper
# OWASP Attack Surface Detector {#owasp-attack-surface-detector .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
### Introduction

During web application penetration testing, it is important to enumerate
your application's attack surface. While Dynamic Application Security
Testing (DAST) tools (such as [OWASP
ZAP](https://www2.owasp.org/www-project-zap/) and [PortSwigger Burp
Suite](https://portswigger.net/)) are good at spidering to identify
application attack surfaces, they will often fail to identify unlinked
endpoints, optional parameters, and parameter datatypes and name. These
endpoints and parameters not found often go untested, which can leave
your application open to an attacker.

### What is the Attack Surface Detector?

The Attack Surface Detector tool uncovers the endpoints of a web
application, the parameters these endpoints accept, and the data type of
those parameters. This includes the unlinked endpoints a spider won't
find in client-side code, or optional parameters totally unused in
client-side code. It also has the capability to calculate the changes in
attack surface between two versions of an application.

The Attack Surface Detector is available as a plugin to both ZAP and
Burp Suite, and a Command Line Interface (CLI) tool is also available.
The CLI tool exports the attack surface as a JSON output, which can then
be used by the ZAP and Burp Suite plugin. This is helpful for cases
where the source code is not provided to the penetration tester
directly. The CLI tool can also be used for other custom integration
where you want to discover an application attack surface or changes in
the attack surface.

For a quick overview of the Attack Surface Detection tool, see this
YouTube video:

[![](assets/images/ASD_yt_img.png){width="800" height="430"
border="10"}](https://www.youtube.com/watch?feature=player_embedded&v=MkJ_NVNsrFw){target="_blank"}

Below is a screenshot of the Burp Suite Attack Surface Detector plugin
where you can see a list of endpoints, endpoint details, and their
corresponding requests:

![ASD Screenshot](assets/images/ASD-Endpoint-Screens.png)

### How it Works

The Attack Surface Detector performs static code analyses to identify
web application endpoints by parsing routes and identifying parameters
(with supported languages and frameworks). This data is made available
in ZAP and Burp Suite to help improve testing coverage.

### Supported Languages and Frameworks

- **Java:** JSPs, Servlets, Struts, Spring MVC
- **C#:** ASP.NET MVC, Web Forms
- **Ruby:** Rails
- **Python:** Django

### Roadmap

We continue to improve the attack surface detection accuracy for
existing supported languages and frameworks, and we are looking to add
additional language support, particularly for PHP and Python. If there
are any PHP or Python developers that are looking to contribute, [please
let us
know](../cdn-cgi/l/email-protection.html#e58c8b838aa5868a8180819dcb868a88).
We are also looking to extend ASD for use in automated headless usage of
ZAP and Burp and move the ASD ZAP plugin out of alpha classification,
which requires
[internationalization](https://github.com/zaproxy/zap-extensions/wiki/AddOnsBeta).
If anyone can help, we would love your contributions. Finally, we are
really interested in what the community thinks will help improve ASD and
we will adjust our roadmap based on that feedback.

### Getting Involved

Contributions to the Attack Surface Detector project are encouraged and
welcome. Additions of new features and enhancements can be provided
through GitHub. We are eager to get user feedback, so please [reach out
to
us](../cdn-cgi/l/email-protection.html#6801060e07280b070c0d0c10460b0705)
or fill out this [ASD survey](https://www.surveymonkey.com/r/D2N87GB).

### Licensing

The Attack Surface Detector plugin is free to use. It is licensed under
the [link Mozilla Public License
2.0](https://www.mozilla.org/en-US/MPL/2.0/).

### Acknowledgements

The Attack Surface Detection project is led by [Code
Dx](https://codedx.com/) and was developed by [Secure
Decisions](https://securedecisions.com/) in collaboration with [Denim
Group](https://www.denimgroup.com/) under a research grant sponsored by
the Department of Homeland Security (DHS) Science and Technology
Directorate, Cyber Security Division (DHS S&T/CSD), BAA via contract
number HHSP233201600058C.
:::
::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-attack-surface-detector/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-attack-surface-detector){.github-button
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

## Project Resources

The Attack Surface Detector is available in the ZAP Marketplace and
PortSwigger BApp Store, and can be installed directly from within those
tools.

### ASD Plugin for OWASP ZAP:

- [Download ZAP
  Plugin](https://github.com/secdec/attack-surface-detector-zap/releases)
- [Documentation](https://github.com/secdec/attack-surface-detector-zap/wiki)
- [Submit
  Feedback](https://github.com/secdec/attack-surface-detector-zap/issues)
- [GitHub Source
  Code](https://github.com/secdec/attack-surface-detector-zap)

### ASD Plugin for PortSwigger Burp:

- [Download Burp Suite
  Plugin](https://github.com/secdec/attack-surface-detector-burp/releases)
- [Documentation](https://github.com/secdec/attack-surface-detector-burp/wiki)
- [Submit
  Feedback](https://github.com/secdec/attack-surface-detector-burp/issues)
- [GitHub Source
  Code](https://github.com/secdec/attack-surface-detector-burp)

### ASD Command-Line Tool:

- [Download ASD
  CLI](https://github.com/secdec/attack-surface-detector-cli/releases)
- [Documentation](https://github.com/secdec/attack-surface-detector-cli/wiki)
- [Submit
  Feedback](https://github.com/secdec/attack-surface-detector-cli/issues)
- [GitHub Source
  Code](https://github.com/secdec/attack-surface-detector-cli)

### News and Events

- 7 Mar 2019 [Version 1.1.4 of the ASD ZAP plugin is
  out!](https://github.com/secdec/attack-surface-detector-zap/releases)
- 8 Feb 2019 [Version 1.1.3 of the ASD Burp Suite plugin is
  out!](https://github.com/secdec/attack-surface-detector-burp/releases)
- 1 Nov 2018 [Version 1.3.5 of the ASD CLI is
  out!](https://github.com/secdec/attack-surface-detector-cli/releases)

### Contact Us

- Project Leader: Ken Prole
- Email: [[\[email protected\]]{.__cf_email__
  cfemail="573c3239792725383b3217242e393827242e247934383a"}](../cdn-cgi/l/email-protection.html#fa919f94d48a8895969fba898394958a898389d4999597)
- [Code Dx twitter](https://twitter.com/codedx)
- [Get Access](https://owasp-slack.herokuapp.com/) to join the
  discussion in the OWASP Slack Channel, #attack-surface-detector.

### Related Projects

- [OWASP Zed Attack Proxy
  Project](https://www.owasp.org/www-project-zap/)
- [OWASP Code Pulse Project](../www-project-code-pulse/index.html)

### Classifications

![New projects](assets/images/New_projects.png) ![OWASP
Breakers](assets/images/Owasp-breakers-small.png) ![OWASP
Defenders](assets/images/Owasp-defenders-small.png) ![Project Type Files
Tool](assets/images/Project_Type_Files_TOOL.png)

### Leaders

- [Ken
  Prole](../cdn-cgi/l/email-protection.html#aac1cfc484dad8c5c6cfeac5ddcbd9da84c5d8cd)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::
