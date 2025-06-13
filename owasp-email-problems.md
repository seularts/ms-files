::::::::::: main-wrapper
# OWASP Email Problems (and solutions) {#owasp-email-problems-and-solutions .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {.section .homepage-blog}
![image](../../../../assets/images/people/staff_andrew.jpg)

Andrew van der Stock

Thursday, August 1, 2024

Recently, Google, Microsoft, and Yahoo and other major email providers
have been implementing stricter email authentication controls. This is a
good thing, as it helps to reduce the amount of spam and phishing emails
that we all receive. However, it can also cause problems for legitimate
email senders, such as OWASP. In the last month or so, we have
experienced great difficulty in sending emails to Microsoft email
addresses (Office 365, Exchange Online, Outlook, Hotmail, Live, etc).
This has been a major problem for us, as many of our members and
volunteers use Microsoft email addresses. We have been working hard to
resolve this issue. In this post, we document a solution that every
Microsoft user needs to do to reliably receive our email.

We have created staff accounts on owaspfoundation.org. Our staff will
only let you know how to un-quarantine our emails, with a link to this
blog post, and to ask that you reply to the original email once restored
to your Inbox.

OWASP has had the various controls (SPF, DKIM, DMARC) in place for
several years. They were not as tight as they were required to be under
the new February 2024 email guidelines promulgated by all major email
providers. We have now tightened those controls to be in line with the
requirements.

However, Microsoft users need to whitelist our email domains, and click
"This is not junk" on our emails. This will help to improve our
reputation with Microsoft, and ensure that our emails are delivered to
your inbox. This is unfortunately a manual process, and one you may not
realize that you need to do.

## Outlook users

1.  Review your junk mail folder
2.  If you find an email from an owasp.org or owasp.com email address in
    your junk mail folder, click on the email, and then click "This is
    not junk" in the toolbar. You can also just drag the message back to
    your Inbox. This will move the email to your inbox, and will help to
    improve our reputation with Microsoft
3.  You can also add the email address to your safe senders list, which
    will help to ensure that future emails are always delivered to your
    inbox.

## Microsoft 365 - Exchange Online Protection (EOP) or Microsoft Defender for Office 365

If your organization uses Microsoft Office 365 or Microsoft Exchange
Online, there is potentially a separate step you need to do to release
the message from quarantine, and then for your administrator to add our
email domains to the allow list.

- [How to release emails from quarantine as a
  user](https://learn.microsoft.com/en-us/defender-office-365/quarantine-end-user#take-action-on-quarantined-email)

Once requested, please ask your admins to release the email, and add
owasp.org and owasp.com to allow sender list so that they don't need to
do this for every email.

- [Manage quarantined messages and files as an
  admin](https://learn.microsoft.com/en-us/defender-office-365/quarantine-admin-manage-messages-files?source=recommendations)
- [How to handle Legitimate emails getting blocked (False Positive),
  using Microsoft Defender for Office
  365](https://learn.microsoft.com/en-us/defender-office-365/step-by-step-guides/how-to-handle-false-positives-in-microsoft-defender-for-office-365)
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
- [OWASP Email Problems (and solutions)](owasp-email-problems.html)
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
