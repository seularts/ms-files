::::::::::: main-wrapper
# OWASP Data Leak Notification {#owasp-data-leak-notification .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {.section .homepage-blog}
![image](../../../../assets/images/people/staff_andrew.jpg)

Andrew van der Stock

Friday, March 29, 2024

In late February 2024, after receiving a few support requests, the OWASP
Foundation became aware of a misconfiguration of OWASP's old Wiki web
server, leading to a data leak involving decade+-old member resumes.

- **Who is affected?** If you were an OWASP member from 2006 to around
  2014 and provided your resume as part of joining OWASP, we advise
  assuming your resume was part of this leak.
- **What data was exposed?** The resumes contained names, email
  addresses, phone numbers, physical addresses, and other personally
  identifiable information.
- **Why was the data collected?** OWASP collected resumes as part of the
  early membership process, whereby members were required in the 2006 to
  2014 era to show a connection to the OWASP community. OWASP no longer
  collects resumes as part of the membership process.
- **What steps has OWASP taken to rectify the leak?** We have disabled
  directory browsing, reviewed the web server and Media Wiki
  configuration for other security issues, removed the resumes from the
  wiki site altogether, and purged the CloudFlare cache to prevent
  further access. Lastly, we have requested that the information be
  removed from the Web Archive.
- **Who will OWASP notify?** We are bringing this issue to the broader
  public's attention with abundant caution. As many of the individuals
  affected by this leak are no longer with OWASP and the age of the data
  is between ten and 18 years old, a great deal of the personal details
  included in this leak are significantly out of date, making contact
  difficult. Regardless, we will contact the email addresses discovered
  during our investigations.
- **How does OWASP protect current membership data?** We apply modern
  cloud-based security best practices such as two-factor authentication,
  minimal access, and resiliency to protect our membership data. We also
  purposefully collect only minimal information for OWASP membership to
  minimize any potential data loss in the future.
- **I think I am affected. What do I need to do?** OWASP has already
  removed your information from the Internet, so no immediate action on
  your part is required. Nothing needs to be done if the information at
  risk is outdated. However, if the information is current, such as
  containing your mobile phone number, please take the usual precautions
  when answering unsolicited emails, mail, or phone calls.

We recognize the significance of this leak, especially considering the
OWASP Foundation's emphasis on cybersecurity. We apologize to those
affected by the leak and are committed to ensuring that this does not
happen again. We are reviewing our data retention policies and will be
implementing additional security measures to prevent future leakes.

> Revision (19 April 2024): The incident should have been labeled a
> "leak" rather than a "breach". The information was exposed to the
> public internet due to a misconfiguration, not because of an attack.
> We do not know if the exposed information was accessed, or by whom.
> The press release has been revised to clarify this.
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
- [OWASP Data Leak Notification](OWASP-data-breach-notification.html)
- [Traefik Labs Joins OWASP and Integrates Coraza and Core Rule Set
  Projects](../19/traefik_owasp.html)

</div>

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
:::::::
:::::::::::
