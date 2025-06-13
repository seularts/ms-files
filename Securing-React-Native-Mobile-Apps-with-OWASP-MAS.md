::::::::::: main-wrapper
# Securing React Native Mobile Apps with OWASP MAS {#securing-react-native-mobile-apps-with-owasp-mas .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {.section .homepage-blog}
![image](../../../../assets/images/people/leader_julia_mezher.html)

Julia Mezher

Wednesday, October 2, 2024

React Native is a popular cross-platform mobile development framework
that allows developers to build native-looking apps for iOS and Android
using a single codebase. Like any other software, React Native apps are
also vulnerable to a variety of security threats.

## 1. Securing each part of the app {#1-securing-each-part-of-the-app}

To secure a React Native app you should analyse all its parts and how
they communicate. This requires an understanding of each block: React
Native, iOS, and Android platforms and Bridge between them.

The React Native app uses JavaScript that is run on the JS engine.
Understanding native JS engines and Hermes engine from Facebook is also
necessary as they have different threat vectors. Using native JS engines
makes extracting minified JS code from application bundles easy, while
[Hermes had several reported
vulnerabilities](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=hermes)
in the past.

## 2. Assessing React Native apps with OWASP guides {#2-assessing-react-native-apps-with-owasp-guides}

It is also important to follow general mobile application security best
practices, such as those described in OWASP guides. While there are no
React Native-specific guides, OWASP provides guidance on how to improve
the security of native apps, protecting them from common threats and
vulnerabilities:

- [OWASP Mobile Application Security Verification
  Standard](https://mas.owasp.org/MASVS/)
- [OWASP Mobile Application Security Testing
  Guide](https://mas.owasp.org/MASTG/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)

OWASP React Native guides can be used to assess platform-specific
security controls, while OWASP JavaScript guides can be used to cover
most of the remaining assessment areas:

- [OWASP Application Security Verification
  Standard](../../../../www-project-application-security-verification-standard/index.html)
- [OWASP Secure coding
  guide](../../../../www-project-secure-coding-practices-quick-reference-guide/stable-en/02-checklist/05-checklist.html)

The common area for assessment in each cross-platform app is the way
methods are bridged between native and non-native parts (like, how
JavaScript and native code are communicating). For example, bridged
methods may lack obfuscation making platform-specific security controls
more visible for reverse engineers. The resilience sections of [OWASP
MASTG](https://mas.owasp.org/MASTG/) can serve as a guide to protect
against reverse engineering and tampering because they describe concepts
that can be applied to cross-platform apps.

## 3. React Native libraries: Secure choice {#3-react-native-libraries-secure-choice}

JavaScript brings to React Native one of its most painful stepping
stones: Managing a large number of dependencies and dealing with
vulnerabilities in them. Integrating dependency checkers like [OWASP
Dependency-Check](../../../../www-project-dependency-check/index.html)
or GitHub Dependabot into the CI/CD process becomes a must-have for
React Native apps.

Many React Native libraries are ported from the JavaScript ecosystem,
but they may not be suitable for mobile apps, especially for
security-sensitive functionality.

A secure React Native library is:

- **Without vulnerabilities:** The library doesn't have known
  vulnerabilities and it has a reasonable history of patching known
  vulnerabilities.
- **Without open security issues:** Review GitHub issues and PRs to see
  how the maintainers respond to security issues.
- **Actively maintained and supported** by multiple people. The
  security-related library should be supported by people with security
  and cryptography expertise, and ideally audited by a third party.
- **Optimised for mobile platforms:** For example, a library with a
  cryptographically secure pseudorandom generator should not depend on
  mouse clicks ([example
  explained](https://www.cossacklabs.com/blog/crypto-wallets-security/#dependency-issues-with-crypto-wallets)).
- **Easy-to-use API:** The library has well-documented APIs that work
  the same on iOS and Android.
- **Licence:** Pay attention to the open-source licence, as not all
  open-source libraries are free to use.
- **Tests:** Make sure the library has unit and integration tests,
  especially if it deals with cryptography or operates highly sensitive
  data.

Research [React Native
libraries](https://www.cossacklabs.com/blog/react-native-libraries-security/)
and their dependencies before using them for security-sensitive
functionality.

## 4. Seven steps to secure React Native app {#4-seven-steps-to-secure-react-native-app}

Find your way to a secure React Native app, by following the steps that
we singled out to simplify this journey:

1.  Understand the implication of adding one more vendor (Facebook) and
    put **trust** in the security of its platform.
2.  Make sure your team has enough **security expertise** for iOS,
    Android, and React Native. Depending on data sensitivity, you may
    want to hire external security experts.
3.  **Educate your development team** about security best practices,
    secure coding, possibilities to automate security checks, OWASP
    [Mobile Top-10](../../../../www-project-mobile-top-10/index.html),
    and [OWASP MAS](https://mas.owasp.org/).
4.  **Creating security controls for mobile apps** as React Native apps
    are still mobile apps. Use OWASP MAS as a main guidance. Add
    security controls specific to React Native, if needed.
5.  **Managing dependencies** in your React Native apps, and keeping
    them up to date. Automated dependency analysers and code scanning is
    a good proactive approach.
6.  **Cover security controls with tests**, especially if they deal with
    cryptographic operations, Secure Enclave, and StrongBox Keystore
7.  **Send the app for security review** by third-party experts.
    Implement mitigations, cover them with tests, and add the issue to
    the regression testing checklist.

Securing React Native mobile apps requires a holistic approach, applied
to all aspects of the development process, from choosing secure
libraries to implementing security controls.
:::
::::

::: github-buttons
[Watch](https://github.com/owasp/owasp.github.io/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/owasp.github.io){.github-button
icon="octicon-star" data-size="large" show-count="true"
aria-label="Star on GitHub"}
:::

::::::: {.sidebar role="complementary"}
::: owasp-sidebar-top
**The OWASP^®^ Foundation** works to improve the security of software
through its community-led open source software projects, hundreds of
chapters worldwide, tens of thousands of members, and by hosting local
and global conferences.
:::

<div>

### Recent News & Opinions

- [OWASP Enables AI Regulation That Works with OWASP AI
  Exchange](../../../2025/05/06/AI-Exchage-Regulation.html)
- [OWASP Calls to Build a Unified Framework for Global Vulnerability
  Intelligence](../../../2025/04/17/owasp-global-vulnerability-intelligence.html)
- [ASVS 5.0 RC1 is ready for your
  review!](../../../2025/04/09/asvs-rc1-review.html)
- [OWASP Education and Training Committee
  update](../../../2025/03/06/owasp-education-and-training-committee-update.html)
- [Advisory on Software Bill of Materials and Real-time Vulnerability
  Monitoring for Open-Source Software and Third-Party
  Dependencies](../../../2025/02/24/advisory-on-implementation-of-software-bill-of-materials-for-vulnerability-management.html)
- [OWASP Juice Shop leadership changes & contributor
  recognition](../../../2025/01/29/juice-shop-leadership.html)
- [Lifecycle events are part of the secure supply
  chain](../../11/26/lifecycle-events-are-part-of-the-secure-supply-chain.html)
- [More than a Password Day
  2024](../../11/12/more-than-a-password-day-2024.html)
- [A workaround for OWASP Foundation emails being blocked by Microsoft
  Office 365](../30/owaspfoundation-org-emails.html)
- [Securing React Native Mobile Apps with OWASP
  MAS](Securing-React-Native-Mobile-Apps-with-OWASP-MAS.html)
- [OWASP Email Problems (and
  solutions)](../../08/01/owasp-email-problems.html)
- [New Articles of Incorporation and Bylaws for the OWASP
  Foundation!](../../07/09/new-coi-and-bylaws.html)
- [Update on the ASVS Community
  Meetup](../../07/03/asvs-community-meetup.html)
- [SecureFlag and OWASP partner to offer Threat Modeling Automation tool
  ThreatCanvas to
  Members](../../05/30/secureflag-threatcanvas-member-benefit.html)
- [The OWASP Foundation appoints Starr Brown as Director of
  Projects](../../04/22/starr-brown-hired-as-director-projects.html)
- [The OWASP Foundation Celebrates 20th
  Anniversary](../../04/21/owasp-foundation-20th-anniversary.html)
- [Checkmarx and OWASP Launch First-ever Global Codebashing Learning
  Initiative](../../04/18/codebashing-member-benefit.html)
- [CycloneDX v1.6 Released, Advances Software Supply Chain Security with
  Cryptographic Bill of Materials and
  Attestations](../../04/09/CycloneDX-v1.6-Released.html)
- [OWASP Data Leak
  Notification](../../03/29/OWASP-data-breach-notification.html)
- [Traefik Labs Joins OWASP and Integrates Coraza and Core Rule Set
  Projects](../../03/19/traefik_owasp.html)

</div>

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
:::::::
:::::::::::
