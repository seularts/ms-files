:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP Top 10 Drone Security Risks {#owasp-top-10-drone-security-risks .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
Creating an "OWASP Drone Top 10 Security Risks" list involves adapting
the known security vulnerabilities from the mobile and web application
domain to the specific context of drones. Drones, or unmanned aerial
vehicles (UAVs), introduce unique challenges due to their physical
mobility, the diversity of their applications, and their often complex
interaction with hardware and software systems. Here's a tailored list
that mirrors the structure and intent behind the original OWASP Mobile
Top 10, focusing on the unique aspects of drone technology:

1.  Insecure Communication Risk: Transmission of data over unsecured
    channels, allowing interception or modification of sensitive
    information (e.g., video feeds, control commands). Mitigation:
    Implement end-to-end encryption for data transmission, use secure
    protocols like TLS.
2.  Weak Authentication/Authorization Risk: Inadequate authentication
    allows unauthorized access to drone controls or sensitive data.
    Mitigation: Strong, multi-factor authentication and role-based
    access control systems.
3.  Insecure Firmware/Software Risk: Vulnerabilities in the drone's
    firmware or software can be exploited to gain unauthorized access or
    control. Mitigation: Regular updates, secure development practices,
    and vulnerability scanning.
4.  Inadequate Personal Data Protection Risk: Drones collecting personal
    data without proper safeguards or consent. Mitigation: Implement
    data protection measures, respect privacy norms, and ensure
    compliance with relevant regulations (e.g., GDPR).
5.  Lack of Secure Update Mechanism Risk: An insecure update process
    could introduce malware or unauthorized modifications. Mitigation:
    Signed firmware/software updates, secure update protocols, and
    integrity verification.
6.  Insecure Third-party Components Risk: Use of vulnerable third-party
    components (e.g., libraries, modules) can compromise drone security.
    Mitigation: Careful vetting of third-party components, keeping them
    up-to-date, and monitoring for disclosed vulnerabilities.
7.  Insufficient Network Security Risk: Vulnerabilities in the drone's
    network services (Wi-Fi, Bluetooth) can lead to unauthorized access.
    Mitigation: Strong network encryption, secure network configuration,
    and disabling unnecessary services.
8.  Physical Security Weaknesses Risk: Physical tampering with the drone
    or its components to gain unauthorized access or control.
    Mitigation: Tamper detection and prevention mechanisms, secure
    hardware design, and access controls.
9.  Insecure Data Storage Risk: Sensitive data stored on the drone
    (e.g., location history, captured images) is not adequately
    protected. Mitigation: Encryption of stored data, secure data
    storage practices, and options for remote wipe if necessary.
10. Lack of Logging and Monitoring Risk: Insufficient logging and
    monitoring can hinder the detection of security breaches or
    unauthorized activities. Mitigation: Implement comprehensive logging
    and real-time monitoring systems, with alerts for suspicious
    activities.

### Road Map

Intro April 2024 Initial version December 2024.
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-10-drone-security-risks/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-10-drone-security-risks){.github-button
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

### Top 10 Drone Security Risks Information

- [Incubator Project](#)
- [Type of Project](#)
- [Version 0.0.0](#)
- [Builder](#)
- [Breaker](#)

### Downloads or Social Links

- [Download](#)
- [Meetup](#)

### Code Repository

- [repo](#)

### Change Log

- [changes](#)

### Leaders

- [Godfrey
  Nolan](../cdn-cgi/l/email-protection.html#fbbc949f9d899e82d5b594979a95bb948c9a888bd594899c)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
