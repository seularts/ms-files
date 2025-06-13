:::::::::::::: main-wrapper
# Lifecycle events are part of the secure supply chain {#lifecycle-events-are-part-of-the-secure-supply-chain .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
:::::: {.section .homepage-blog}
![image](../../../../assets/images/people/Olle-Johansson-and-Benji-Visser.jpg)

Olle Johansson and Benji Visser

Tuesday, November 26, 2024

*A new OWASP project - Common Lifecycle Enumeration - aims to
standardize encodings of product lifecycle events, such as end-of-life,
end-of-support and others. The specification will become an ECMA
International standard when ready. Read more about this exciting new
OWASP project!*

Digital products, both hardware and software have a lifecycle that
mirrors human life - they are born, grow and develop, and eventually
come to an end, just like ourselves. However, there are many more
changes in a product's lifecycle that need to be captured, both for
commercial products and open source software. The end-of-life state will
affect many users of a product in various ways and needs to be
communicated in a way that supports a high degree of automation.

When building a product today, we combine components from a range of
upstream vendors and open source projects - a motherboard, operating
system, sensors, software libraries and tools. The bill-of-materials
(BOM) is a necessary tool to manage both hardware and software during
the lifetime of the product. The BOM, when combined with lifecycle
events, provides a foundation for automating and proactively managing
each product's lifecycle.

## Regulators require product lifecycle management

New regulations, like the recently adopted EU Cyber Resilience Act,
enforces a lifecycle management process where manufacturers are obliged
to maintain security through the product's entire lifecycle, from
purchasing to decommissioning. This means manufacturers must ensure that
the product and all components are secure, kept up-to-date, and free of
exploitable vulnerabilities.

The [OWASP CycloneDX](https://cyclonedx.org/) bill-of-materials standard
can cover many aspects of a product, both software and hardware. But one
thing that's been missing is just the lifecycle events, like
end-of-support, end-of-life and end-of-sales. For Open Source projects
there are similar events covering "LTS release support", "security fixes
only", "stable" and other variants.

## Monitoring the life state of a product or component is essential

A manufacturer needs to be assured that components from upstream vendors
and projects are supported, otherwise the manufacturer assumes full
responsibility.

A customer, through their IT organization, also wants to be able to plan
their inventory and capture this information from all vendors. Products
without any support need to be phased out in a controlled and planned
way with as few surprises as possible.

## Lifecycle management requires a high degree of automation

This exchange of information across the supply chain needs to be both
enumerated in a standard format and automatically exchanged. Rest
assured that OWASP is working on all fronts here.

The [OWASP Common Lifecycle Enumeration (CLE)
project](../../../../cle/index.html) is actively working on a standard
for capturing these events. This will be part of the effort to
standardize OWASP standards in [ECMA TC54](https://tc54.org/). The
summer of 2024 CycloneDX became an ECMA standard and more is on the way.
A new working group, ECMA TC54 TG3, was formed in October 2024 to lead
the standardization alongside working groups for the Package URL (PURL)
and the Transparency Exchange API.

## How OWASP CLE fits into other work

The CLE syntax will be adopted by the [OWASP Transparency Exchange API
(TEA)](https://github.com/CycloneDX/transparency-exchange-api) working
group (also known as "Project Koala") that creates a standardized set of
APIs for publishing and consuming software and hardware transparency
artifacts like SBOM, HBOM, VEX/CSAF vulnerability information, IN-Toto
attestations, SCITT statements and much more. With TEA the interaction
between customers and vendors will be highly automated. A standard API
leads not only to efficient workflows, but also keeps costs for
integration under control. Many vendors of platforms have shown interest
in integration TEA into their systems, including [OWASP Dependency
Track](https://dependencytrack.org/), a leading open source platform for
software transparency, license compliance and vulnerability management.

If you're interested, all are welcome to join the work in the OWASP
common lifecycle enumeration project!

[https://owasp.org/www-project-common-lifecycle-enumeration/](../../../../www-project-common-lifecycle-enumeration/index.html)

::::: {style="display: flex; flex-wrap: wrap;"}
::: {style="flex: 1; min-width: 50%; padding-top: 3rem;"}
**Benji Visser**\
Leader of OWASP CLE
:::

::: {style="flex: 1; min-width: 50%; padding-top: 3rem;"}
**Olle E. Johansson**\
Leader of OWASP CycloneDX project Koala
:::
:::::
::::::
:::::::

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
  chain](lifecycle-events-are-part-of-the-secure-supply-chain.html)
- [More than a Password Day
  2024](../12/more-than-a-password-day-2024.html)
- [A workaround for OWASP Foundation emails being blocked by Microsoft
  Office 365](../../10/30/owaspfoundation-org-emails.html)
- [Securing React Native Mobile Apps with OWASP
  MAS](../../10/02/Securing-React-Native-Mobile-Apps-with-OWASP-MAS.html)
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
::::::::::::::
