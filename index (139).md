::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Acknowledgments](#div-acknowledgments){#acknowledgments-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="acknowledgments"}
- [Deployment](#div-deployment){#deployment-link .tab-link role="tab"
  aria-selected="false" aria-controls="deployment"}
- [Join](#div-join){#join-link .tab-link role="tab"
  aria-selected="false" aria-controls="join"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}

# OWASP DVSA {#owasp-dvsa .page-title}

:::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![alt=DVSA](assets/images/dvsa_logo.png)

# DVSA

### a Damn Vulnerable Serverless Application

Damn Vulnerable Serverless Application (DVSA) is a deliberately
vulnerable application aiming to be an aid for security professionals to
test their skills and tools in a legal environment, help developers
better understand the processes of securing serverless applications and
to aid both students & teachers to learn about serverless application
security in a controlled class room environment.

The aim of DVSA is to practice some of the most common serverless
vulnerabilities, with a simple straightforward interface.

Please note, there are both documented and undocumented vulnerabilities
with this software. This is intentional. You are encouraged to try and
discover as many issues as possible.

# Disclaimer

***Do not install DVSA on a production account***

We do not take responsibility for the way in which any one uses this
application (DVSA). We have made the purposes of the application clear
and it should not be used maliciously. We have given warnings and taken
measures to prevent users from installing DVSA on to production
accounts.

# How to use?

See [Deployment](index.html#div-deployment) tab

# Cheat-Sheet

See instructions and demonstrations in the
[LESSONS](https://github.com/OWASP/DVSA/tree/master/AWS) section.

# License

Damn Vulnerable Serverless Application (DVSA) is free software: you can
redistribute it and/or modify it under the terms of the GNU General
Public License as published by the Free Software Foundation, either
version 3 of the License, or (at your option) any later version.

Damn Vulnerable Serverless Application (DVSA) is distributed in the hope
that it will be useful, but WITHOUT ANY WARRANTY; without even the
implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along
with Damn Vulnerable Serverless Application (DVSA). If not, see
http://www.gnu.org/licenses/.
:::

::: {#sec-acknowledgments .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Founder

  ------------------------------------------------------------------------------------------------ ------------------------------------------------------- -----------------------------------------------------
  [Tal Melamed](../cdn-cgi/l/email-protection.html#b4c0d5d89ad9d1d8d5d9d1d0f4dbc3d5c7c49adbc6d3)   [OWASP](https://www.owasp.org/index.php/User:Tal_Mel)   [LinkedIn](https://www.linkedin.com/in/talmelamed/)
  ------------------------------------------------------------------------------------------------ ------------------------------------------------------- -----------------------------------------------------

## Sponsors

![contrast](../../raw.githubusercontent.com/OWASP/www-project-dvsa/master/assets/images/contrast_logo.png)
:::

::: {#sec-deployment .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Deployment

#### [Application Repository](AWS/VIDEOS/reo_deploy.html)

- Deploy DVSA from the [AWS Serverless Application
  Repository](https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:674087993380:applications~OWASP-DVSA)

- After deployment is complete. Click on 'View CloudFormation Stack'

- Under 'Outputs' you will find the URL for the application (DVSA
  Website URL)

![](https://imgur.com/ZfjEyiM)

#### [Serverless Framework](AWS/VIDEOS/serverless_deploy.html)

You must run serverless deploy commands with an environment variable
profile (e.g. `AWS_PROFILE=<aws-profile-name>`{.language-plaintext
.highlighter-rouge}) instead of the serverless argument.

##### Clone Project

- `git clone `{.language-plaintext
  .highlighter-rouge}[`[email protected]`{.language-plaintext
  .highlighter-rouge}](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="33545a4773545a475b46511d505c5e"}`:OWASP/DVSA.git`{.language-plaintext
  .highlighter-rouge}

##### Install Serverless

- `npm install -g serverless`{.language-plaintext .highlighter-rouge}

##### Install AWS-CLI

- `pip install awscli --upgrade --user`{.language-plaintext
  .highlighter-rouge}

##### Verify AWS-CLI Installation

- `aws --version`{.language-plaintext .highlighter-rouge}

If you get a "command not found" error, see the "Steps to Take after
Installation" section
[here](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html#install-tool-pip).

##### Configure AWS-CLI for your Account

- `aws configure`{.language-plaintext .highlighter-rouge}

##### Install dependencies

- `npm i`{.language-plaintext .highlighter-rouge}

##### Deploy Backend

- `sls deploy`{.language-plaintext .highlighter-rouge}

##### Build Client

- `npm run-script client:build`{.language-plaintext .highlighter-rouge}

##### Deploy Client

- `sls client deploy`{.language-plaintext .highlighter-rouge}

------------------------------------------------------------------------

## Running locally

#### Run Client

- `npm run-script client:start`{.language-plaintext .highlighter-rouge}

***Note***: This will only work if you previously deployed the backend.
If this fails, confirm you still have a
`be-stack.json`{.language-plaintext .highlighter-rouge} file at the root
of this project.

#### Run Backend

- `npm start`{.language-plaintext .highlighter-rouge}

If you want to point your local client to your local backend, edit your
`be-stack.json`{.language-plaintext .highlighter-rouge} and set
`ServiceEndpoint`{.language-plaintext .highlighter-rouge} to
`http://localhost:3000`{.language-plaintext .highlighter-rouge}. Note
that you will still be using the Cognito pools in AWS.

------------------------------------------------------------------------

## Email subscription

DVSA sends receipts in the email (which will help you in hacking it).
You can use the built-in **Inbox** page within the application to get
the emails and obtain the receipts.

***Note***: each user will be assigned an email from
`mailsac.com`{.language-plaintext .highlighter-rouge} which will be
automatically verified. Real emails will be sent to their account and
will appear in the application Inbox page. All this is **transparent**
to the user and the deployer).

***Note***: to make the email verification script work your default AWS
region has to be "US East (N. Virginia)", for example by setting
`region = us-east-1`{.language-plaintext .highlighter-rouge} in your
\~/.aws/config file

**Alternatively**, if you want users to receive emails to their
registered email account (e.g. gmail), use one of the followings:

- Send an email verification link to email address, by running the
  following command (after clicking on the received link, emails will
  **also** be sent to their actual email address):

`aws ses verify-email-identity --email-address <your_email>`{.language-plaintext
.highlighter-rouge}

- [Request a sending limit
  increase](https://console.aws.amazon.com/support/v1#/case/create?issueType=service-limit-increase&limitType=service-code-ses).
  This will allow your entire cloud account to send emails to any
  address.
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::

::: {#sec-join .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Get Involved

Get involved in **DVSA**!

You do not have to be a security expert or a programmer to contribute.

Contact the Project Leader(s) to get involved, we welcome any type of
suggestions and comments.

## Slack

Join out [Slack
channel](https://join.slack.com/t/owasp/shared_invite/enQtNDI5MzgxMDQ2MTAwLTEyNzIzYWQ2NDZiMGIwNmJhYzYxZDJiNTM0ZmZiZmJlY2EwZmMwYjAyNmJjNzQxNzMyMWY4OTk3ZTQ0MzFhMDY)

## GitHub

The project is maintained in the [DVSA](https://github.com/OWASP/DVSA/).

Feel free to open or solve an
[issue](https://github.com/OWASP/DVSA//issues).
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Roadmap

- 25 DEC 2018: http://serverless.fail (official website) was launched.
- 08 JAN 2019: v1.0 beta release
  [GitHub](https://github.com/OWASP/DVSA/)
- 01 FEB 2019: v1.0 official version.
- 01 APR 2019: Serverless is available trough the [AWS Serverlesss
  Repository](https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:889485553959:applications~DVSA)
- 15 JAN 2020: v1.2 available on
  [Github](https://github.com/OWASP/DVSA/) and [AWS Serverless
  Repository](https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:889485553959:applications~DVSA)
:::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

- 15 Oct 2018: Hello world! - DVSA was created by [Tal
  Melamed](https://www.linkedin.com/in/talmelamed/)
- 25 Dec 2018: http://serverless.fail - Launched
- 01 Jan 2019: Project was donated by [Protego
  Labs](https://protego.io/)
- 03 Jan 2019: [The
  Register](https://www.theregister.co.uk/2019/01/03/damn_vulnerable_serverless_application/)
- 04 Jan 2019:
  [SDTimes](https://sdtimes.com/cloud/sd-times-news-digest-protegos-dvsa-quicklogic-acquires-ai-company-and-iot-interoperability/)
- 07 Jan 2019:
  [eWEEK](http://www.eweek.com/security/protego-labs-boosts-serverless-security-with-open-source-project)
- 08 Jan 2019: [Computer
  Weekly](https://www.computerweekly.com/news/252455429/Protego-Labs-launches-serverless-app-security-tool)
- 08 Jan 2019:
  [Technical.ly](https://technical.ly/baltimore/2019/01/08/protego-has-a-new-open-source-tool-to-provide-serverless-security-training/)
:::
::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-dvsa/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-dvsa){.github-button
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

### Leaders

- [Tal
  Melamed](../cdn-cgi/l/email-protection.html#3b4f5a5715565e575a565e5f7b544c5a484b1554495c)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::
