:::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Quickstart](#div-quickstart){#quickstart-link .tab-link role="tab"
  aria-selected="false" aria-controls="quickstart"}

# OWASP Mobile Audit {#owasp-mobile-audit .page-title}

::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![Mobile Audit](assets/images/mobile_audit.png)

## Mobile Audit - Static Analysis and detecting malware in Android APKs

![App](assets/images/app.png)

### Who is Mobile Audit for?

Mobile Audit focuses not only in the security testing and defensive use
cases, the goal of the project is to become a complete homologation for
Android APKs, which includes:

- Static Analysis (SAST): It will perform a full decompilation of the
  APK and extract all the possible information of it. It reports the
  different vulnerabilities and findings in the source code grouped by
  different categories. Also, it has full support on finding triage
  (change status and criticality).
- Malware Analysis: finds dangerous permissions and suspicious code.
- Best Practices of Secure Android Coding: tells developers in which
  parts of the code they are coding securely and where they are not.

It is aimed to different user profiles:

- Developers
- System Administrators
- Security Engineers

In each of the scans, it would have the following information:

- Application Info
- Security Info
- Components
- SAST Findings
- Best Practices Implemented
- Virus Total Info
- Certificate Info
- Strings
- Databases
- Files

![App](assets/images/scan.png)

For easy access there is a sidebar on the left page of the scan:

![Menu](assets/images/menu.png)

### Components

![Schema](assets/images/architecture.png)

- **db**: PostgreSQL 3.11.5
- **nginx**: Nginx 1.23.3
- **rabbitmq**: RabbitMQ 3.11.5
- **worker**: Celery 5.2.2
- **web**: Mobile Audit App
  [3.0.0](https://github.com/mpast/mobileAudit)

### Main features

- [x] Uses Docker for easy deployment in multiplatform environment
- [x] Extract all information of the APK
- [x] Analyze all the source code searching for weaknesses
- [x] All findings are categorized and follows CWE standards
- [x] Also highlight the Best Practices in Secure Android Implementation
  in the APK
- [x] The findings can be edited and the false positives can be triaged
  and deleted
- [x] All scan results can be exported to PDF
- [x] User authentication and user management
- [x] API v1 with Swagger and ReDoc
- [x] TLS
- [x] Dynamic page reload (WIP)
- [ ] Export to Markdown
- [ ] Export to CSV
- [ ] LDAP integration

### Integrations

#### Virus Total (API v3)

It checks if there has been an scan of the APK and extract all its
information. Also, there is the possibility of uploading the APK is
selected a property in the environment (Disabled by default).

#### Defect Dojo (API v2)

It is possible to upload the findings to the defect manager.

#### MalwareDB & Maltrail {#malwaredb--maltrail}

It checks in the database if there are URLs in the APK that are related
with Malware.

## Contribution

If you are interested in contributing with Mobile Audit:

1.  **Fork** this repo
2.  **Clone** the project to your own machine
3.  **Commit** changes to your own branch
4.  **Push** your work back up to your fork
5.  Submit a **Pull request** so that we can review your changes

## Licensing

This project is distributed under [GPL-3.0
License](https://github.com/mpast/mobileAudit/raw/main/LICENSE).
:::

::::::::::: {#sec-quickstart .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Quickstart

### Installation

Using Docker-compose:

The provided `docker-compose.yml`{.language-plaintext
.highlighter-rouge} file allows you to run the app locally in
development. To start the container, run:

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
docker-compose up
```
:::
::::

If there are changes to the local Application Dockerfile, you can build
the image with

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
docker-compose build
```
:::
::::

Once the application has launched, you can test the application by
navigating to: http://localhost:8888/ to access the dashboard.

![Dashboard](assets/images/dashboard.png)

Also, there is a TLS version running in port 443, so you can test the
application by navigating to: https://localhost/ to access the
dashboard.

In each of the scans, it would have the following information:

- Application Info
- Security Info
- Components
- SAST Findings
- Best Practices Implemented
- Virus Total Info
- Certificate Info
- Strings
- Databases
- Files

For easy access there is a sidebar on the left page of the scan:

![Menu](assets/images/menu.png)

### API v1

REST API integration with Swagger and ReDoc.

#### Usage

- Endpoint to authenticate and get token:
  `/api/v1/auth-token/`{.language-plaintext .highlighter-rouge}

- Once authenticated, use header in all requests:
  `Authorization: Token <ApiKey>`{.language-plaintext
  .highlighter-rouge}

#### Swagger

![Swagger](assets/images/swagger.png)

#### ReDoc

![ReDoc](assets/images/redoc.png)

#### Endpoints

- A JSON view of the API specification at
  `/swagger.json`{.language-plaintext .highlighter-rouge}
- A YAML view of the API specification at
  `/swagger.yaml`{.language-plaintext .highlighter-rouge}
- A swagger-ui view of your API specification at
  `/swagger/`{.language-plaintext .highlighter-rouge}
- A ReDoc view of your API specification at
  `/redoc/`{.language-plaintext .highlighter-rouge}

### Configuration

#### Nginx configuration

- TLS - port 443: `nginx/app_tls.conf`{.language-plaintext
  .highlighter-rouge}
- Standard - port 8888: `nginx/app.conf`{.language-plaintext
  .highlighter-rouge}

#### Docker configuration

There are two volumes in `docker-compose.yml`{.language-plaintext
.highlighter-rouge} with the configurations. By default both 443 and
8888 ports will be available, but **use only TLS configuration for
production deployments**.

:::: {.language-yml .highlighter-rouge}
::: highlight
``` highlight
- ./nginx/app.conf:/etc/nginx/conf.d/app.conf
- ./nginx/app_tls.conf:/etc/nginx/conf.d/app_tls.conf
```
:::
::::

#### Environment variables

All the environment variables are in a `.env`{.language-plaintext
.highlighter-rouge} file, there is an `.env.example`{.language-plaintext
.highlighter-rouge} with all the variables needed. Also there are
collected in `app/config/settings.py`{.language-plaintext
.highlighter-rouge}:

:::: {.language-py .highlighter-rouge}
::: highlight
``` highlight
CWE_URL = env('CWE_URL', 'https://cwe.mitre.org/data/definitions/')

MALWAREDB_ENABLED = env('MALWAREDB_ENABLED', True)
MALWAREDB_URL = env('MALWAREDB_URL', 'https://www.malwaredomainlist.com/mdlcsv.php')

VIRUSTOTAL_ENABLED = env('VIRUSTOTAL_ENABLED', False)
VIRUSTOTAL_URL = env('VIRUSTOTAL_URL', 'https://www.virustotal.com/')
VIRUSTOTAL_FILE_URL = env('VIRUSTOTAL_FILE_URL', 'https://www.virustotal.com/gui/file/')
VIRUSTOTAL_API_URL_V3 = env('VIRUSTOTAL_API_URL_V3', 'https://www.virustotal.com/api/v3/')
VIRUSTOTAL_URL_V2 = env('VIRUSTOTAL_API_URL_V2', 'https://www.virustotal.com/vtapi/v2/file/')
VIRUSTOTAL_API_KEY = env('VIRUSTOTAL_API_KEY', '')
VIRUSTOTAL_UPLOAD = env('VIRUSTOTAL_UPLOAD', False)

DEFECTDOJO_ENABLED = env('DEFECTDOJO_ENABLED', False)
DEFECTDOJO_URL = env('DEFECTDOJO_URL', 'http://defectdojo:8080/finding/')
DEFECTDOJO_API_URL = env('DEFECTDOJO_API_URL', 'http://defectdojo:8080/api/v2/')
DEFECTDOJO_API_KEY = env('DEFECTDOJO_API_KEY', '')
```
:::
::::
:::::::::::
:::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-mobile-audit/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-mobile-audit){.github-button
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

### Mobile Audit

-  Tool
-  Builder
-  Defender
-  [Version
  3.1.0](https://github.com/mpast/mobileAudit/releases/tag/3.1.0)

### Code Repository

- [Repository](https://github.com/mpast/mobileAudit)
- [Releases](https://github.com/mpast/mobileAudit/releases)

### Change Log

- [Changes](https://github.com/mpast/mobileAudit/releases)

### Leaders

- [Monica
  Pastor](../cdn-cgi/l/email-protection.html#d2a2b3a1a6bda0b3b0b3bcb3b6b7a192b5bfb3bbbefcb1bdbf)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::::
