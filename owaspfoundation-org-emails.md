::::::::::: main-wrapper
# A workaround for OWASP Foundation emails being blocked by Microsoft Office 365 {#a-workaround-for-owasp-foundation-emails-being-blocked-by-microsoft-office-365 .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {.section .homepage-blog}
![image](../../../../assets/images/people/staff_andrew.jpg)

Andrew van der Stock

Wednesday, October 30, 2024

Over the last several months, OWASP, particularly the owasp.com domain,
has been blocked from sending messages to tenants of the Microsoft
Office 365 platform or those using Microsoft Defender for Office 365,
where messages end up blacklisted in quarantine or never received.
Organizations that have failed to receive our emails includes legal
firms, our HR firm, our accountants, our European affiliate's
accountants and VAT specialists, and many others, including potential
sponsors, donors, and members.

This is an untenable situation, and extremely disappointing that we have
been unable to resolve this issue with Microsoft. So we have to use a
workaround domain, owaspfoundation.org to send emails to Microsoft 365
tenants. This is not ideal, but we have no other choice. We will never
use owaspfoundation.org for any other purpose other than to get around
this spam filter insanity. We will never send any marketing or other
unsolicited emails from this domain, it will not be linked to our
MailChimp or our accounting system. Only select staff have access to
this domain, and we will only use it when all else fails.

## What have we done to resolve this issue?

We updated and thoroughly tested our SPF and DKIM records for both
owasp.com and owasp.org many months ago, and they pass with flying
colors. We have tested and improved our MX records thoroughly with the
Pro version of mxtoolbox.com and other DNS tools. We have tested email
delivery to our friends at various firms. We have reported and have been
working with Microsoft to resolve the problem, but to no avail. It is
understandable that Microsoft has a very strict anti-spam policy, but it
is partially underscored by an AI categorizer, which somehow learned
that OWASP Foundation emails are spam, and for whatever reason,
Microsoft has been unable or unwilling to untrain their spam filter.

## owaspfoundation.org is our last resort email platform {#owaspfoundationorg-is-our-last-resort-email-platform}

Once we are certain that your organization is not receiving our emails,
or they are always being quarantined, we will be using a new domain,
owaspfoundation.org, which is hosted on the Microsoft 365 platform to
communicate with you. This is not normal, and we need your help to fix
the problem.

## What can you do?

If you're receiving email from owaspfoundation.org, please work with
your IT department to whitelist owasp.com emails, as we are not able to
do so on your behalf.

### Outlook and Exchange Online users

Microsoft users need to whitelist our email domains (owasp.org and
owasp.com), and click "This is not junk" on our emails that end up in
quarantine or in your spam folder. This will help to improve our
reputation with Microsoft, and ensure that our emails are delivered to
your inbox. This is unfortunately a manual process.

1.  Review your junk mail and quarantine folders
2.  If you find an email from an owasp.org or owasp.com email address in
    your junk mail folder, click on the email, and then click "This is
    not junk" in the toolbar. You can also just drag the message back to
    your Inbox. This will move the email to your inbox, and will help to
    improve our reputation with Microsoft
3.  If you find an email in your quarantine folder, ask for it to be
    released, and contact your IT administrators to whitelist owasp.org
    and owasp.com domains (see below)
4.  You can also add the email address to your safe senders list, which
    will help to ensure that future emails are always delivered to your
    inbox.

- [How to release emails from quarantine as a
  user](https://learn.microsoft.com/en-us/defender-office-365/quarantine-end-user#take-action-on-quarantined-email)

### Microsoft 365 - Exchange Online Protection (EOP) or Microsoft Defender for Office 365

If your organization uses Microsoft Office 365 or Microsoft Exchange
Online, there is potentially a separate step you need to do to release
the message from quarantine, and then for your administrator to add our
email domains to the allow list.

Once requested, please ask your admins to release the email, and add
owasp.org and owasp.com to allow sender list so that they don't need to
do this for every email.

- [Manage quarantined messages and files as an
  admin](https://learn.microsoft.com/en-us/defender-office-365/quarantine-admin-manage-messages-files?source=recommendations)
- [How to handle Legitimate emails getting blocked (False Positive),
  using Microsoft Defender for Office
  365](https://learn.microsoft.com/en-us/defender-office-365/step-by-step-guides/how-to-handle-false-positives-in-microsoft-defender-for-office-365)

Once Microsoft has resolved their spam filter training issue, the OWASP
Foundation will revert solely to using owasp.com as our primary email
domain.

## Conclusion

We apologize for any inconvenience this may cause, but we have no other
choice. We have tried everything else, and we are still unable to send
emails to Microsoft 365 tenants. If anyone knows anyone senior enough at
Microsoft who can help us resolve this issue, please [contact me
directly](../../../../cdn-cgi/l/email-protection.html#34555a504651431a42555a50514647405b575f745b435547441a575b59).
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
  Office 365](owaspfoundation-org-emails.html)
- [Securing React Native Mobile Apps with OWASP
  MAS](../02/Securing-React-Native-Mobile-Apps-with-OWASP-MAS.html)
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
