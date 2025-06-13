:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Response Headers](#div-headers){#headers-link .tab-link role="tab"
  aria-selected="false" aria-controls="headers"}
- [Browser Support](#div-browsersupport){#browsersupport-link .tab-link
  role="tab" aria-selected="false" aria-controls="browsersupport"}
- [Best Practices](#div-bestpractices){#bestpractices-link .tab-link
  role="tab" aria-selected="false" aria-controls="bestpractices"}
- [Technical Resources](#div-technical){#technical-link .tab-link
  role="tab" aria-selected="false" aria-controls="technical"}
- [Code Snippets](#div-codesnippets){#codesnippets-link .tab-link
  role="tab" aria-selected="false" aria-controls="codesnippets"}
- [Miscellaneous](#div-misc){#misc-link .tab-link role="tab"
  aria-selected="false" aria-controls="misc"}
- [Statistics](#div-statistics){#statistics-link .tab-link role="tab"
  aria-selected="false" aria-controls="statistics"}
- [Case Studies](#div-casestudies){#casestudies-link .tab-link
  role="tab" aria-selected="false" aria-controls="casestudies"}
- [Logo](#div-logo){#logo-link .tab-link role="tab"
  aria-selected="false" aria-controls="logo"}

# OWASP Secure Headers Project {#owasp-secure-headers-project .page-title}

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## Introduction

![OSHP Logo](assets/images/oshp_logo.png)

[![OWASP
Production](https://img.shields.io/badge/owasp-production%20project-800080.svg)](https://www.owasp.org/projects)

[![External Links Validity
Check](https://github.com/OWASP/www-project-secure-headers/actions/workflows/check-external-links.yml/badge.svg?branch=master)](https://github.com/OWASP/www-project-secure-headers/actions/workflows/check-external-links.yml)

[![Update headers reference JSON
files](https://github.com/OWASP/www-project-secure-headers/actions/workflows/headers-generate-json-files.yml/badge.svg?branch=master)](https://github.com/OWASP/www-project-secure-headers/actions/workflows/headers-generate-json-files.yml)

[![Update monitoring technical references
dashboard](https://github.com/OWASP/www-project-secure-headers/actions/workflows/monitoring-technical-references-generate-dashboard.yml/badge.svg?branch=master)](https://github.com/OWASP/www-project-secure-headers/actions/workflows/monitoring-technical-references-generate-dashboard.yml)

[![Perform_monitoring_oshp_site_references](https://github.com/OWASP/www-project-secure-headers/actions/workflows/monitoring-oshp-site-references.yml/badge.svg?branch=master)](https://github.com/OWASP/www-project-secure-headers/actions/workflows/monitoring-oshp-site-references.yml)

[![update_tab_stats_related_files](https://github.com/OWASP/www-project-secure-headers/actions/workflows/tab-stats-headers-generate-related-files.yml/badge.svg?branch=master)](https://github.com/OWASP/www-project-secure-headers/actions/workflows/tab-stats-headers-generate-related-files.yml)

🎯 The **OWASP Secure Headers Project** (also called **OSHP**) describes
HTTP response headers that your application can use to increase the
security of your application. Once set, these HTTP response headers can
restrict modern browsers from running into easily preventable
vulnerabilities. The OWASP Secure Headers Project intends to raise
awareness and use of these headers.

🤔 HTTP headers are well known and also despised. Seeking a balance
between usability and security, developers implement functionality
through the headers that can make applications more versatile or secure.
But in practice how are the headers being implemented? What sites follow
the best implementation practices? Big companies, small, all or none?

## Description

📚 The OWASP Secure Headers Project aim to provide elements about the
following aspects regarding HTTP security headers:

- [Guidance](index-2.html#div-bestpractices_configuration-proposal)
  about the recommended HTTP security headers that can be leveraged.
- [Guidance](index-2.html#div-bestpractices_prevent-information-disclosure-via-http-headers)
  about the HTTP headers that should be removed.
- [Tools](https://github.com/oshp/oshp-validator) to validate an HTTP
  security header configuration.
- [Code](index-2.html#div-technical) libraries that can be leveraged to
  configure recommended HTTP security headers.
- [Statistics](https://github.com/oshp/oshp-stats) about usage of the
  recommended HTTP security headers.

🏭 All the tools provided by the OSHP are gathered under this [GitHub
organization](https://github.com/oshp/).

📺 A presentation of the project is available on the following
locations:

- [OWASP Spotlight Youtube
  playlists](https://www.youtube.com/watch?v=N4F3VWQYU9E).
- [Application Security Podcast Youtube
  playlists](https://www.youtube.com/watch?v=0SNU9clVhKU).
- [NoLimitSecu
  Podcast](https://www.nolimitsecu.fr/owasp-secure-headers-project/)
  (*French*).

## Migration

🌎 The OWASP Secure Headers Project was migrated from the [old
website](https://wiki.owasp.org/index.php/OWASP_Secure_Headers_Project)
to the [GitHub OWASP
organization](https://github.com/OWASP/www-project-secure-headers).

📦 The following projects are now **archived**, they are initiatives
that are now replaced by new projects:

- [headers](https://github.com/oshp/headers).
- [headers-ui-container](https://github.com/oshp/headers-ui-container).

## Security headers usage statistics

📈 We provide statistics, updated every month, about HTTP response
security headers usage mentioned by the OWASP Secure Headers Project:

- They are available through [this GitHub
  project](https://github.com/oshp/oshp-stats) and the tab named
  [Statistics](index-2.html#div-statistics).

## Security headers usage validator

✅ We provide a [venom](https://github.com/ovh/venom) tests suite to
validate an HTTP security response header configuration against OWASP
Secure Headers Project recommendation:

- It is available through [this GitHub
  project](https://github.com/oshp/oshp-validator).

🧪 We also provide a *online mock endpoint* returning an HTTP response,
for which, all HTTP response headers recommended by the OSHP will be
set:

- It is automatically deployed on
  `https://oshp-validator-mock.onrender.com`{.language-plaintext
  .highlighter-rouge}
- Technical details about this endpoint are
  [here](https://github.com/oshp/oshp-validator#tests-suite-mock-service).

## Security headers reference files

📖 As mentioned in previous sections, we provide the collection of HTTP
response security headers to add as well as HTTP response headers to
remove, both in table form.

💡 Additionally, we provide this information as two JSON files to enable
automation in the context of a provisioning workflow:

- Collection of [HTTP response security headers to
  add](ci/headers_add.json).
- Collection of [HTTP response headers to
  remove](ci/headers_remove.json).

📡 These json files are automatically updated.

## Technical references health dashboard

📍 We automatically generate and monitor this
**[dashboard](https://github.com/OWASP/www-project-secure-headers/blob/master/monitoring_technical_references_dashboard.md)**
to identify any dead project referenced in the **[Technical
Resources](index.html#div-technical)** tab.

## Discussions, information and roadmap

💬 We use the GitHub [discussions
feature](https://github.com/OWASP/www-project-secure-headers/discussions)
for discussions about the project as well as spreading global
information about it.

👩‍💻 The work on the OSHP projects and associated components is tracked
using the GitHub [project
feature](https://github.com/orgs/OWASP/projects/44).

## Create a link to the OSHP site

📖 This is documented into the **[Case
Studies](index-2.html#div-casestudies)** tab.

## Contributors

💌 Contributors to OSHP, before the migration of the project to
[GitHub](https://github.com/OWASP/www-project-secure-headers):

- [Alexandre
  Menezes](../cdn-cgi/l/email-protection.html#62030e071a030c0610074c040f070c07180711220d150311124c0d1005)
- [Adam Averay](https://github.com/adamaveray)
- [Jim Manico](https://github.com/jmanico)

💌 Visit this
[page](https://github.com/OWASP/www-project-secure-headers/graphs/contributors)
for updated information about the contributors since the migration of
the project to GitHub.

## Licensing

📑 This project content is free to use. It is licensed under the [Apache
2.0 License](https://www.apache.org/licenses/LICENSE-2.0).
:::

::::::::::::::::::::::::::::::::::::::::::: {#sec-headers .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Response Headers

💡 The collection of HTTP response security headers mentioned in this
section is applicable when the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
processing the HTTP response is a browser. The support for these headers
by non-browser API clients (user agent), like for example an HTTP client
in a programming language, **is not standardized**. So, it requires
specific testing to identify if an HTTP response security header is
supported or not by such HTTP client.

🚦 Header lifecycle flow:

![Header lifecycle
flow](assets/images/response_headers_header_lifecycle_flow.png)

📐 **Working draft**

- [Permissions-Policy](#permissions-policy)

✅ **Active**

- [Strict-Transport-Security](#strict-transport-security)
- [X-Frame-Options](#x-frame-options)
- [X-Content-Type-Options](#x-content-type-options)
- [Content-Security-Policy](#content-security-policy)
- [X-Permitted-Cross-Domain-Policies](#x-permitted-cross-domain-policies)
- [Referrer-Policy](#referrer-policy)
- [Clear-Site-Data](#clear-site-data)
- [Cross-Origin-Embedder-Policy](#cross-origin-embedder-policy)
- [Cross-Origin-Opener-Policy](#cross-origin-opener-policy)
- [Cross-Origin-Resource-Policy](#cross-origin-resource-policy)
- [Cache-Control](#cache-control)

⏰ **Almost deprecated**

None

❌ **Deprecated**

- [Feature-Policy](#feature-policy)
- [Expect-CT](#expect-ct)
- [Public-Key-Pins](#public-key-pins)
- [X-XSS-Protection](#x-xss-protection)
- [Pragma](#pragma)

## Strict-Transport-Security

HTTP Strict Transport Security (also named *HSTS*) is a browser security
policy mechanism which helps to protect websites against protocol
downgrade attacks and cookie hijacking. It allows web servers to declare
that web browsers (or other complying user agents) should only interact
with it using secure HTTPS connections, and within a defined timespan
(max-age) not via the clear text HTTP protocol. HSTS is an IETF standard
track protocol and is specified in [RFC
6797](https://www.rfc-editor.org/rfc/rfc6797). A server implements an
HSTS policy by supplying a header
(`Strict-Transport-Security`{.language-plaintext .highlighter-rouge})
over an HTTPS connection (HSTS headers over HTTP are ignored).

📍 Important note about the behavior of the header over a **HTTP
connection** (source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security#description)):

- The `Strict-Transport-Security`{.language-plaintext
  .highlighter-rouge} header **is ignored by the browser when your site
  has only been accessed using HTTP**.
- Once your site is accessed over HTTPS **with no certificate errors**,
  the browser knows your site is HTTPS capable and will honor the
  `Strict-Transport-Security`{.language-plaintext .highlighter-rouge}
  header.

💡 If you need to let the access open, via HTTP, to the web server but
want to ensure that `Strict-Transport-Security`{.language-plaintext
.highlighter-rouge} header is taken into account for your site then you
can use the
**[preload](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security#preloading_strict_transport_security)**
directive.

### Values

  Value                                                         Description
  ------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `max-age=SECONDS`{.language-plaintext .highlighter-rouge}     The time, in seconds, that the browser should remember that this site is only to be accessed using HTTPS.
  `includeSubDomains`{.language-plaintext .highlighter-rouge}   If this optional parameter is specified, this rule applies to all of the site's subdomains as well.
  `preload`{.language-plaintext .highlighter-rouge}             If this optional parameter is specified, its instruct the browser to always access the site using HTTPS because the site is included into `Strict-Transport-Security`{.language-plaintext .highlighter-rouge} [preload list](https://www.chromium.org/hsts/).

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Strict-Transport-Security: max-age=31536000
```
:::
::::

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Strict-Transport-Security: max-age=31536000 ; includeSubDomains
```
:::
::::

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Strict-Transport-Security: max-age=31536000 ; includeSubDomains ; preload
```
:::
::::

### References

- <https://tools.ietf.org/html/rfc6797>
- <https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html>
- [https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/02-Configuration_and_Deployment_Management_Testing/07-Test_HTTP_Strict_Transport_Security.html](../www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/02-Configuration_and_Deployment_Management_Testing/07-Test_HTTP_Strict_Transport_Security.html)
- <https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security>
- <https://www.chromium.org/hsts>
- <https://hstspreload.org/>
- <https://developer.mozilla.org/en-US/docs/Web/Security/HTTP_strict_transport_security>
- <https://raymii.org/s/tutorials/HTTP_Strict_Transport_Security_for_Apache_NGINX_and_Lighttpd.html>
- <https://blogs.windows.com/msedgedev/2015/06/09/http-strict-transport-security-comes-to-internet-explorer-11-on-windows-8-1-and-windows-7/>

## X-Frame-Options

The `X-Frame-Options`{.language-plaintext .highlighter-rouge} response
header (also named **XFO**) improves the protection of web applications
against
[clickjacking](https://portswigger.net/web-security/clickjacking). It
instructs the browser whether the content can be displayed within
frames.

The Content-Security-Policy (CSP)
[frame-ancestors](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors)
directive obsoletes the X-Frame-Options header. If a resource has both
policies, the CSP frame-ancestors policy will be enforced and the
X-Frame-Options policy will be ignored.

### Values

  Value                                                          Description
  -------------------------------------------------------------- --------------------------------------------------------------------------------------------------
  `deny`{.language-plaintext .highlighter-rouge}                 No rendering within a frame.
  `sameorigin`{.language-plaintext .highlighter-rouge}           No rendering if origin mismatch.
  `allow-from: DOMAIN`{.language-plaintext .highlighter-rouge}   Allows rendering if framed by frame loaded from *DOMAIN* (**not supported by modern browsers**).

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
X-Frame-Options: deny
```
:::
::::

### References

- <https://tools.ietf.org/html/rfc7034>
- <https://tools.ietf.org/html/draft-ietf-websec-x-frame-options-01>
- <https://tools.ietf.org/html/draft-ietf-websec-frame-options-00>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/X-Frame-Options>
- <https://portswigger.net/web-security/clickjacking>
- <https://blogs.msdn.microsoft.com/ieinternals/2010/03/30/combating-clickjacking-with-x-frame-options/>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors>

## X-Content-Type-Options

Setting this header will prevent the browser from interpreting files as
a different MIME type to what is specified in the
`Content-Type`{.language-plaintext .highlighter-rouge} HTTP header (e.g.
treating `text/plain`{.language-plaintext .highlighter-rouge} as
`text/css`{.language-plaintext .highlighter-rouge}).

### Values

  Value                                               Description
  --------------------------------------------------- ---------------------------------------------------------------------------------------------
  `nosniff`{.language-plaintext .highlighter-rouge}   Will prevent the browser from MIME-sniffing a response away from the declared content-type.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
X-Content-Type-Options: nosniff
```
:::
::::

### References

- [https://msdn.microsoft.com/en-us/library/gg622941%28v=vs.85%29.aspx](https://msdn.microsoft.com/en-us/library/gg622941(v=vs.85).aspx)
- <https://blogs.msdn.microsoft.com/ie/2008/09/02/ie8-security-part-vi-beta-2-update/>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options>

## Content-Security-Policy

A Content Security Policy (also named CSP) requires careful tuning and
testing after definition of the policy. A content security policy can
have significant impact on the way browsers render pages (e.g., inline
JavaScript or CSS can disabled). A proper CSP can prevents a wide range
of attacks, including cross-site scripting, other cross-site injections
and click jacking.

### Values

  Directive                                                             Description
  --------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `base-uri`{.language-plaintext .highlighter-rouge}                    Define the base URI for relative URIs.
  `default-src`{.language-plaintext .highlighter-rouge}                 Define loading policy for all resources type in case a resource type's dedicated directive is not defined (fallback).
  `script-src`{.language-plaintext .highlighter-rouge}                  Define which scripts the protected resource can execute.
  `object-src`{.language-plaintext .highlighter-rouge}                  Define from where the protected resource can load plugins.
  `style-src`{.language-plaintext .highlighter-rouge}                   Define which styles (CSS) can be applied to the protected resource.
  `img-src`{.language-plaintext .highlighter-rouge}                     Define from where the protected resource can load images.
  `media-src`{.language-plaintext .highlighter-rouge}                   Define from where the protected resource can load video and audio.
  `frame-src`{.language-plaintext .highlighter-rouge}                   *(Deprecated and replaced by `child-src`{.language-plaintext .highlighter-rouge})* Define from where the protected resource can embed frames.
  `child-src`{.language-plaintext .highlighter-rouge}                   Define from where the protected resource can embed frames.
  `frame-ancestors`{.language-plaintext .highlighter-rouge}             Define from where the protected resource can be embedded in frames. Useful against [click jacking](../www-community/attacks/Clickjacking.html)
  `font-src`{.language-plaintext .highlighter-rouge}                    Define from where the protected resource can load fonts.
  `connect-src`{.language-plaintext .highlighter-rouge}                 Define which URIs the protected resource can load using script interfaces.
  `manifest-src`{.language-plaintext .highlighter-rouge}                Define from where the protected resource can load manifests.
  `form-action`{.language-plaintext .highlighter-rouge}                 Define which URIs can be used as the action of HTML form elements.
  `sandbox`{.language-plaintext .highlighter-rouge}                     Specifies an HTML sandbox policy that the user agent applies to the protected resource.
  `script-nonce`{.language-plaintext .highlighter-rouge}                Define script execution by requiring the presence of the specified nonce on script elements.
  `plugin-types`{.language-plaintext .highlighter-rouge}                Define the set of plugins that can be invoked by the protected resource by limiting the types of resources that can be embedded.
  `reflected-xss`{.language-plaintext .highlighter-rouge}               Instruct the user agent to activate or deactivate any heuristics used to filter or block reflected cross-site scripting attacks, equivalent to the effects of the non-standard `X-XSS-Protection`{.language-plaintext .highlighter-rouge} header.
  `block-all-mixed-content`{.language-plaintext .highlighter-rouge}     *(Deprecated)* Prevent the user agent from loading mixed content.
  `upgrade-insecure-requests`{.language-plaintext .highlighter-rouge}   Instruct the user agent to using HTTPS when trying to download insecure HTTP resources
  `referrer`{.language-plaintext .highlighter-rouge}                    *(Deprecated)* Define information the user agent can send in the `Referer`{.language-plaintext .highlighter-rouge} header.
  `report-uri`{.language-plaintext .highlighter-rouge}                  *(Deprecated and replaced by `report-to`{.language-plaintext .highlighter-rouge})* Specifies a URI to which the user agent sends reports about policy violation.
  `report-to`{.language-plaintext .highlighter-rouge}                   Specifies a group (defined in the `Report-To`{.language-plaintext .highlighter-rouge} header) to which the user agent sends reports about policy violation.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Content-Security-Policy: script-src 'self'
```
:::
::::

### References

- <https://www.w3.org/TR/CSP/>
- <https://developer.mozilla.org/en-US/docs/Web/Security/CSP>
- <https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html>
- <https://scotthelme.co.uk/content-security-policy-an-introduction/>
- [https://report-uri.io](https://report-uri.io/)
- [https://content-security-policy.com](https://content-security-policy.com/)
- <https://report-uri.com/home/generate>
- <https://csp-evaluator.withgoogle.com/>

## X-Permitted-Cross-Domain-Policies

A cross-domain policy file is an XML document that grants a web client,
such as Adobe Flash Player or Adobe Acrobat (though not necessarily
limited to these), permission to handle data across domains. When
clients request content hosted on a particular source domain and that
content makes requests directed towards a domain other than its own, the
remote domain needs to host a cross-domain policy file that grants
access to the source domain, allowing the client to continue the
transaction. Normally a meta-policy is declared in the master policy
file, but for those who can't write to the root directory, they can also
declare a meta-policy using the
`X-Permitted-Cross-Domain-Policies`{.language-plaintext
.highlighter-rouge} HTTP response header.

### Values

  Value                                                       Description
  ----------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------
  `none`{.language-plaintext .highlighter-rouge}              No policy files are allowed anywhere on the target server, including this master policy file.
  `master-only`{.language-plaintext .highlighter-rouge}       Only this master policy file is allowed.
  `by-content-type`{.language-plaintext .highlighter-rouge}   \[HTTP/HTTPS only\] Only policy files served with Content-Type: text/x-cross-domain-policy are allowed.
  `by-ftp-filename`{.language-plaintext .highlighter-rouge}   \[FTP only\] Only policy files whose file names are crossdomain.xml (i.e. URLs ending in /crossdomain.xml) are allowed.
  `all`{.language-plaintext .highlighter-rouge}               All policy files on this target domain are allowed.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
X-Permitted-Cross-Domain-Policies: none
```
:::
::::

### References

- <https://www.adobe.com/devnet-docs/acrobatetk/tools/AppSec/xdomain.html>
- <https://rorsecurity.info/portfolio/new-http-headers-for-more-security>
- <https://gf.dev/cross-domain-policy-test>

## Referrer-Policy

The `Referrer-Policy`{.language-plaintext .highlighter-rouge} HTTP
header governs which referrer information, sent in the
`Referer`{.language-plaintext .highlighter-rouge} header, should be
included with requests made.

### Values

  Value                                                                       Description
  --------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `no-referrer`{.language-plaintext .highlighter-rouge}                       The `Referer`{.language-plaintext .highlighter-rouge} header will be omitted entirely. No referrer information is sent along with requests.
  `no-referrer-when-downgrade`{.language-plaintext .highlighter-rouge}        This is the user agent's default behavior if no policy is specified. The origin is sent as referrer to a-priori as-much-secure destination (HTTPS → HTTPS), but isn't sent to a less secure destination (HTTPS → HTTP).
  `origin`{.language-plaintext .highlighter-rouge}                            Only send the origin of the document as the referrer in all cases. (e.g. the document `https://example.com/page.html`{.language-plaintext .highlighter-rouge} will send the referrer `https://example.com/`{.language-plaintext .highlighter-rouge}.)
  `origin-when-cross-origin`{.language-plaintext .highlighter-rouge}          Send a full URL when performing a same-origin request, but only send the origin of the document for other cases.
  `same-origin`{.language-plaintext .highlighter-rouge}                       A referrer will be sent for same-site origins, but cross-origin requests will contain no referrer information.
  `strict-origin`{.language-plaintext .highlighter-rouge}                     Only send the origin of the document as the referrer to a-priori as-much-secure destination (HTTPS → HTTPS), but don't send it to a less secure destination (HTTPS → HTTP).
  `strict-origin-when-cross-origin`{.language-plaintext .highlighter-rouge}   Send a full URL when performing a same-origin request, only send the origin of the document to a-priori as-much-secure destination (HTTPS → HTTPS), and send no header to a less secure destination (HTTPS → HTTP).
  `unsafe-url`{.language-plaintext .highlighter-rouge}                        Send a full URL (stripped from parameters) when performing a same-origin or cross-origin request.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Referrer-Policy: no-referrer
```
:::
::::

### References

- <https://www.w3.org/TR/referrer-policy/>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy>

## Clear-Site-Data

The Clear-Site-Data header clears browsing data (cookies, storage,
cache) associated with the requesting website. It allows web developers
to have more control over the data stored locally by a browser for their
origins (source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Clear-Site-Data)).
This header is useful for example, during a logout process, in order to
ensure that all stored content on the client side like cookies, storage
and cache are removed.

### Values

  Value                                                           Description
  --------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `"cache"`{.language-plaintext .highlighter-rouge}               Indicates that the server wishes to remove locally cached data for the origin of the response URL.
  `"cookies"`{.language-plaintext .highlighter-rouge}             Indicates that the server wishes to remove all cookies for the origin of the response URL. HTTP authentication credentials are also cleared out. This affects the entire registered domain, including subdomains.
  `"storage"`{.language-plaintext .highlighter-rouge}             Indicates that the server wishes to remove all DOM storage for the origin of the response URL.
  `"executionContexts"`{.language-plaintext .highlighter-rouge}   Indicates that the server wishes to reload all browsing contexts for the origin of the response. Currently, this value is only supported by a small subset of browsers.
  `"*"`{.language-plaintext .highlighter-rouge}                   Indicates that the server wishes to clear all types of data for the origin of the response. If more data types are added in future versions of this header, they will also be covered by it.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Clear-Site-Data: "cache","cookies","storage"
```
:::
::::

### References

- <https://w3c.github.io/webappsec-clear-site-data/>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Clear-Site-Data>
- <https://www.chromestatus.com/feature/4713262029471744>
- <https://github.com/w3c/webappsec-clear-site-data>
- <https://github.com/w3c/webappsec-clear-site-data/tree/master/demo>

## Cross-Origin-Resource-Policy

This response header (also named CORP) allows to define a policy that
lets web sites and applications opt in to protection against certain
requests from other origins (such as those issued with elements like
`<script>`{.language-plaintext .highlighter-rouge} and
`<img>`{.language-plaintext .highlighter-rouge}), to mitigate
speculative [side-channel
attacks](https://en.wikipedia.org/wiki/Side-channel_attack), like
[Spectre](https://spectreattack.com/), as well as [Cross-Site Script
Inclusion (XSSI)](https://www.scip.ch/en/?labs.20160414) attacks (source
[Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Resource-Policy)).

💡 To fully understand where **CORP** and **COEP** work:

- CORP applies on the loaded resource side (resource owner).
- COEP applies on the "loader" of the resource side (consumer of the
  resource).

### Values

  Value                                                    Description
  -------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `same-site`{.language-plaintext .highlighter-rouge}      Only requests from the same [Site](https://developer.mozilla.org/en-US/docs/Glossary/Site) can read the resource.
  `same-origin`{.language-plaintext .highlighter-rouge}    Only requests from the same [Origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin) (i.e. scheme + host + port) can read the resource.
  `cross-origin`{.language-plaintext .highlighter-rouge}   Requests from any [Origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin) (both `same-site`{.language-plaintext .highlighter-rouge} and `cross-site`{.language-plaintext .highlighter-rouge}) can read the resource. Browsers are using this policy when an [CORP header is not specified](https://resourcepolicy.fyi/#corp-and-isolation).

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Cross-Origin-Resource-Policy: same-origin
```
:::
::::

### References

- <https://fetch.spec.whatwg.org/#cross-origin-resource-policy-header>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Resource-Policy>
- <https://caniuse.com/mdn-http_headers_cross-origin-resource-policy>
- <https://web.dev/articles/why-coop-coep#corp>
- <https://web.dev/articles/cross-origin-isolation-guide>
- <https://resourcepolicy.fyi/>
- <https://andrewlock.net/understanding-security-headers-part-2-cross-origin-resource-policy-preventing-hotlinking/>

## Cross-Origin-Embedder-Policy

This response header (also named COEP) prevents a document from loading
any cross-origin resources that don't explicitly grant the document
permission (source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy)).

💡 To fully understand where **CORP** and **COEP** work:

- CORP applies on the loaded resource side (resource owner).
- COEP applies on the "loader" of the resource side (consumer of the
  resource).

### Values

  Value                                                    Description
  -------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `unsafe-none`{.language-plaintext .highlighter-rouge}    Allows the document to fetch cross-origin resources without giving explicit permission through the [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) protocol or the [Cross-Origin-Resource-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Cross-Origin_Resource_Policy) header (it is the default value).
  `require-corp`{.language-plaintext .highlighter-rouge}   A document can only load resources from the same origin, or resources explicitly marked as loadable from another origin.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Cross-Origin-Embedder-Policy: require-corp
```
:::
::::

### References

- <https://html.spec.whatwg.org/multipage/origin.html#coep>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy>
- <https://caniuse.com/mdn-http_headers_cross-origin-embedder-policy>
- <https://web.dev/articles/why-coop-coep#coep>
- <https://web.dev/articles/cross-origin-isolation-guide>
- <https://andrewlock.net/understanding-security-headers-part-3-cross-origin-embedder-policy/>

## Cross-Origin-Opener-Policy

This response header (also named COOP) allows you to ensure a top-level
document does not share a browsing context group with cross-origin
documents. COOP will process-isolate your document and potential
attackers can't access to your global object if they were opening it in
a popup, preventing a set of cross-origin attacks dubbed
[XS-Leaks](https://xsleaks.dev/) (source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Opener-Policy)).

### Values

  Value                                                                Description
  -------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `unsafe-none`{.language-plaintext .highlighter-rouge}                Allows the document to be added to its opener's browsing context group unless the opener itself has a COOP of `same-origin`{.language-plaintext .highlighter-rouge} or `same-origin-allow-popups`{.language-plaintext .highlighter-rouge} (it is the default value).
  `same-origin-allow-popups`{.language-plaintext .highlighter-rouge}   Retains references to newly opened windows or tabs which either don't set COOP or which opt out of isolation by setting a COOP of `unsafe-none`{.language-plaintext .highlighter-rouge}.
  `same-origin`{.language-plaintext .highlighter-rouge}                Isolates the browsing context exclusively to same-origin documents. Cross-origin documents are not loaded in the same browsing context.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Cross-Origin-Opener-Policy: same-origin
```
:::
::::

### References

- <https://html.spec.whatwg.org/multipage/origin.html#cross-origin-opener-policies>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Opener-Policy>
- <https://caniuse.com/mdn-http_headers_cross-origin-opener-policy>
- <https://web.dev/articles/why-coop-coep#coop>
- <https://web.dev/articles/cross-origin-isolation-guide>
- <https://xsleaks.dev/>
- <https://github.com/xsleaks/xsleaks>
- <https://portswigger.net/daily-swig/xs-leak>
- <https://portswigger.net/research/xs-leak-detecting-ids-using-portal>
- <https://andrewlock.net/understanding-security-headers-part-1-cross-origin-opener-policy-preventing-attacks-from-popups/>

## Cache-Control

This header holds directives (instructions) for caching in both
**requests** and **responses**. If a given directive is in a request, it
does not mean this directive is in the response (source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)).
Specify the capability of a resource to be cached is important to
prevent [exposure of information via the
cache](https://cwe.mitre.org/data/definitions/525.html).

The headers named
[Expires](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Expires)
and
[Pragma](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Pragma)
can be used in addition to the
[Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)
header.
[Pragma](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Pragma)
header can be used for backwards compatibility with the HTTP/1.0 caches.
However, *Cache-Control* is the recommended way to define the caching
policy.

### Values applicable for HTTP responses

  Value                                                          Description
  -------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `must-revalidate`{.language-plaintext .highlighter-rouge}      Indicates that once a resource becomes stale, caches do not use their stale copy without successful validation on the origin server.
  `no-cache`{.language-plaintext .highlighter-rouge}             The response may be stored by any cache, even if the response is normally non-cacheable. However, the stored response **MUST always** go through validation with the origin server first before using it.
  `no-store`{.language-plaintext .highlighter-rouge}             The response may not be stored in any cache.
  `no-transform`{.language-plaintext .highlighter-rouge}         An intermediate cache or proxy cannot edit the response body, `Content-Encoding`{.language-plaintext .highlighter-rouge}, `Content-Range`{.language-plaintext .highlighter-rouge}, or `Content-Type`{.language-plaintext .highlighter-rouge}.
  `public`{.language-plaintext .highlighter-rouge}               The response may be stored by any cache, even if the response is normally non-cacheable.
  `private`{.language-plaintext .highlighter-rouge}              The response may be stored only by a browser's cache, even if the response is normally non-cacheable.
  `proxy-revalidate`{.language-plaintext .highlighter-rouge}     Like `must-revalidate`{.language-plaintext .highlighter-rouge}, but only for shared caches (e.g., proxies). Ignored by private caches.
  `max-age=<seconds>`{.language-plaintext .highlighter-rouge}    The maximum amount of time a resource is considered fresh. Unlike [Expires](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Expires), this directive is relative to the time of the request.
  `s-maxage=<seconds>`{.language-plaintext .highlighter-rouge}   Overrides `max-age`{.language-plaintext .highlighter-rouge} or the [Expires](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Expires) header, but only for shared caches (e.g., proxies). Ignored by private caches.

### Extended values

The following directives are not part of the core [HTTP caching
standards document](https://datatracker.ietf.org/doc/html/rfc7234).
Therefore, check this
[table](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control#browser_compatibility)
for their support.

  Value                                                                        Description
  ---------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `immutable`{.language-plaintext .highlighter-rouge}                          Indicates that the response body will not change over time.
  `stale-while-revalidate=<seconds>`{.language-plaintext .highlighter-rouge}   Indicates the client can accept a stale response, while asynchronously checking in the background for a fresh one. The **seconds** value indicates how long the client can accept a stale response.
  `stale-if-error=<seconds>`{.language-plaintext .highlighter-rouge}           Indicates the client can accept a stale response if the check for a fresh one fails. The **seconds** value indicates how long the client can accept the stale response after the initial expiration.

### Example

No caching allowed, clear any previously cached resources and include
support for HTTP/1.0 caches:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Cache-Control: no-store, max-age=0
Pragma: no-cache
```
:::
::::

Caching allowed with a cache duration of one week:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Cache-Control: public, max-age=604800
```
:::
::::

### References

- [https://redbot.org](https://redbot.org/)
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Pragma>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Expires>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching>
- <https://datatracker.ietf.org/doc/html/rfc7234>
- <https://cwe.mitre.org/data/definitions/524.html>
- <https://cwe.mitre.org/data/definitions/525.html>
- <https://portswigger.net/web-security/web-cache-poisoning>
- <https://portswigger.net/research/practical-web-cache-poisoning>
- <https://portswigger.net/research/web-cache-entanglement>
- <https://portswigger.net/web-security/web-cache-deception>
- <https://portswigger.net/research/gotta-cache-em-all>

## Permissions Policy

> 💻 **Working draft.**

The Permissions-Policy header replaces the existing **Feature-Policy**
header for controlling delegation of permissions and powerful features.
The header uses a structured syntax, and allows sites to more tightly
restrict which origins can be granted access to features (source [Chrome
platform
status](https://www.chromestatus.com/feature/5745992911552512)).

### Values

🧭 As the specification is still under development, it is better to
consult this
[page](https://github.com/w3c/webappsec-permissions-policy/blob/main/features.md)
to obtain the current list of supported directives.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Permissions-Policy: accelerometer=(), autoplay=(), camera=(), cross-origin-isolated=(), display-capture=(), encrypted-media=(), fullscreen=(), geolocation=(), gyroscope=(), keyboard-map=(), magnetometer=(), microphone=(), midi=(), payment=(), picture-in-picture=(), publickey-credentials-get=(), screen-wake-lock=(), sync-xhr=(self), usb=(), web-share=(), xr-spatial-tracking=(), clipboard-read=(), clipboard-write=(), gamepad=(), hid=(), idle-detection=(), interest-cohort=(), serial=(), unload=()
```
:::
::::

### References

- <https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md>
- <https://caniuse.com/permissions-policy>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy#directives>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Permissions-Policy>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Permissions-Policy#directives>
- <https://www.w3.org/TR/permissions-policy-1/>
- <https://www.chromestatus.com/feature/5745992911552512>
- <https://www.permissionspolicy.com/>

## Feature-Policy

> **Deprecated**: Replaced by the header
> *[Permissions-Policy](#permissions-policy)*.

Feature Policy allows web developers to selectively enable, disable, and
modify the behavior of certain features and APIs in the browser. It is
similar to [Content Security Policy](#content-security-policy) but
controls features instead of security behavior (Source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Feature_Policy)).

### Values

Refer to this
[page](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy#directives)
to obtains the list of supported directives.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Feature-Policy: vibrate 'none'; geolocation 'none'
```
:::
::::

### References

- <https://w3c.github.io/webappsec-feature-policy/>
- <https://scotthelme.co.uk/a-new-security-header-feature-policy/>
- <https://github.com/w3c/webappsec-feature-policy/blob/master/features.md>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy>
- <https://caniuse.com/feature-policy>

## Expect-CT

> **Deprecated.**

> **⚠️ Warning:** This header will likely become obsolete in June 2021.
> Since May 2018 new certificates are expected to support SCTs by
> default. Certificates before March 2018 were allowed to have a
> lifetime of 39 months, those will all be expired in June 2021.

The `Expect-CT`{.language-plaintext .highlighter-rouge} header is used
by a server to indicate that browsers should evaluate connections to the
host for Certificate Transparency compliance.\
In Chrome 61 (Aug 2017) Chrome enabled its enforcement via SCT by
default
([source](https://www.chromestatus.com/feature/5677171733430272)). You
can still use this header to specify an `report-uri`{.language-plaintext
.highlighter-rouge}.

This header comes from the (now expired) internet draft [Expect-CT
Extension for HTTP](https://datatracker.ietf.org/doc/html/rfc9163).

### Values

  Value                                                  Description
  ------------------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `report-uri`{.language-plaintext .highlighter-rouge}   *(Optional)* Indicates the URL to which the browser should report Expect-CT failures.
  `enforce`{.language-plaintext .highlighter-rouge}      *(Optional)* A valueless directive that, if present, signals to the browser that compliance to the CT Policy should be enforced (rather than report-only) and that the browser should refuse future connections that violate its CT Policy. When both the `enforce`{.language-plaintext .highlighter-rouge} and `report-uri`{.language-plaintext .highlighter-rouge} directives are present, the configuration is referred to as an "enforce-and-report" configuration, signalling to the browser both that compliance to the CT Policy should be enforced and that violations should be reported.
  `max-age`{.language-plaintext .highlighter-rouge}      Specifies the number of seconds after the response is received the browser should remember and enforce certificate transparency compliance.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Expect-CT: max-age=86400, enforce, report-uri="https://foo.example/report"
```
:::
::::

### References

- <https://datatracker.ietf.org/doc/html/rfc9163>
- <https://scotthelme.co.uk/a-new-security-header-expect-ct/>
- <https://www.chromestatus.com/feature/5677171733430272>

## Public-Key-Pins

> **Deprecated.**

> **⚠️ Warning:** This header has been deprecated by all major browsers
> and is no longer recommended. **Avoid using it**, and update existing
> code if possible;

HTTP Public Key Pinning (HPKP) is a security mechanism which allows
HTTPS websites to resist impersonation by attackers using mis-issued or
otherwise fraudulent certificates. (For example, sometimes attackers can
compromise certificate authorities, and then can mis-issue certificates
for a web origin.).

The HTTPS web server serves a list of public key hashes, and on
subsequent connections clients expect that server to use one or more of
those public keys in its certificate chain. Deploying HPKP safely will
require operational and organizational maturity due to the risk that
hosts may make themselves unavailable by pinning to a set of public key
hashes that becomes invalid. With care, host operators can greatly
reduce the risk of man-in-the-middle (MITM) attacks and other false
authentication problems for their users without incurring undue risk.

### Deprecation Reason

Criticism and concern revolved around malicious or human error scenarios
known as [HPKP Suicide and Ransom
PKP](https://scotthelme.co.uk/using-security-features-to-do-bad-things/).
In such scenarios, a website owner would have their ability to publish
new contents to their domain severely hampered by either losing access
to their own keys or having new keys announced by a malicious attacker.

### Values

  Value                                                             Description
  ----------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `pin-sha256="<sha256>"`{.language-plaintext .highlighter-rouge}   The quoted string is the Base64 encoded Subject Public Key Information (SPKI) fingerprint. It is possible to specify multiple pins for different public keys. Some browsers might allow other hashing algorithms than SHA-256 in the future.
  `max-age=SECONDS`{.language-plaintext .highlighter-rouge}         The time, in seconds, that the browser should remember that this site is only to be accessed using one of the pinned keys.
  `includeSubDomains`{.language-plaintext .highlighter-rouge}       If this optional parameter is specified, this rule applies to all of the site's subdomains as well.
  `report-uri="<URL>"`{.language-plaintext .highlighter-rouge}      If this optional parameter is specified, pin validation failures are reported to the given URL.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Public-Key-Pins: pin-sha256="d6qzRu9zOECb90Uez27xWltNsj0e1Md7GkYYkVoZWmM="; pin-sha256="E9CZ9INDbd+2eRQozYqqbQ2yXLVKB9+xcprMF+44U1g="; report-uri="http://example.com/pkp-report"; max-age=10000; includeSubDomains
```
:::
::::

### References

- <https://tools.ietf.org/html/rfc7469>
- [https://owasp.org/www-community/controls/Certificate_and_Public_Key_Pinning#HTTP_pinning](../www-community/controls/Certificate_and_Public_Key_Pinning.html#HTTP_pinning)
- <https://en.wikipedia.org/wiki/HTTP_Public_Key_Pinning>
- <https://developer.mozilla.org/en-US/docs/Web/Security/Public_Key_Pinning>
- <https://raymii.org/s/articles/HTTP_Public_Key_Pinning_Extension_HPKP.html>
- <https://labs.detectify.com/2016/07/05/what-hpkp-is-but-isnt/>
- <https://blog.qualys.com/ssllabs/2016/09/06/is-http-public-key-pinning-dead>
- <https://scotthelme.co.uk/im-giving-up-on-hpkp/>
- <https://groups.google.com/a/chromium.org/forum/m/#!msg/blink-dev/he9tr7p3rZ8/eNMwKPmUBAAJ>

## X-XSS-Protection

> **Deprecated.**

> **⚠️ Warning:** The X-XSS-Protection header has been deprecated by
> modern browsers and its use can introduce additional security issues
> on the client side. As such, it is recommended to set the header as
> `X-XSS-Protection: 0`{.language-plaintext .highlighter-rouge} in order
> to disable the XSS Auditor, and not allow it to take the default
> behavior of the browser handling the response. Please use
> `Content-Security-Policy`{.language-plaintext .highlighter-rouge}
> instead.

This header enables the cross-site scripting (XSS) filter in your
browser.

### Values

  Value                                                                                     Description
  ----------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `0`{.language-plaintext .highlighter-rouge}                                               Filter disabled.
  `1`{.language-plaintext .highlighter-rouge}                                               Filter enabled. If a cross-site scripting attack is detected, in order to stop the attack, the browser will sanitize the page.
  `1; mode=block`{.language-plaintext .highlighter-rouge}                                   Filter enabled. Rather than sanitize the page, when a XSS attack is detected, the browser will prevent rendering of the page.
  `1; report=http://[YOURDOMAIN]/your_report_URI`{.language-plaintext .highlighter-rouge}   Filter enabled. The browser will sanitize the page and report the violation. This is a Chromium function utilizing CSP violation reports to send details to a URI of your choice.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
X-XSS-Protection: 0
```
:::
::::

### References

- <https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html>
- <https://www.chromestatus.com/feature/5021976655560704>
- <https://bugzilla.mozilla.org/show_bug.cgi?id=528661>
- <https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/>
- <https://github.com/zaproxy/zaproxy/issues/5849>
- <https://scotthelme.co.uk/security-headers-updates/#removing-the-x-xss-protection-header>
- <https://portswigger.net/daily-swig/google-chromes-xss-auditor-goes-back-to-filter-mode>
- [https://owasp.org/www-community/attacks/xss/](../www-community/attacks/xss/index.html)
- <https://www.virtuesecurity.com/blog/understanding-xss-auditor/>
- <https://www.veracode.com/blog/2014/03/guidelines-for-setting-security-headers>

## Pragma

> **Deprecated.**

The `Pragma`{.language-plaintext .highlighter-rouge} **HTTP/1.0**
general header is an implementation-specific header that may have
various effects along the request-response chain.

This header serves for backwards compatibility with the **HTTP/1.0**
caches that do not have a [Cache-Control](#cache-control) **HTTP/1.1**
header (source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Pragma)).

### Values

  Value                                                Description
  ---------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `no-cache`{.language-plaintext .highlighter-rouge}   Same as `Cache-Control: no-cache`{.language-plaintext .highlighter-rouge}. Forces caches to submit the request to the origin server for validation before a cached copy is released.

### Example

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
Pragma: no-cache
```
:::
::::

### References

- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Pragma>
- <https://http.dev/pragma>
- <https://caniuse.com/mdn-http_headers_pragma>
:::::::::::::::::::::::::::::::::::::::::::

::: {#sec-browsersupport .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Browser Support

📚 A reference is provided, for each header, to a site always providing
up-to-date information.

  Feature                                 Reference
  --------------------------------------- --------------------------------------------------------------------------
  HTTP Strict Transport Security (HSTS)   <https://caniuse.com/stricttransportsecurity>
  X-Frame-Options                         <https://caniuse.com/x-frame-options>
  X-Content-Type-Options                  <https://caniuse.com/mdn-http_headers_x-content-type-options>
  Content-Security-Policy                 <https://caniuse.com/?search=content-security-policy>
  X-Permitted-Cross-Domain-Policies       <https://www.adobe.com/devnet-docs/acrobatetk/tools/AppSec/xdomain.html>
  Referrer-Policy                         <https://caniuse.com/referrer-policy>
  Feature-Policy                          <https://caniuse.com/feature-policy>
  HTTP Public-Key-Pins (HPKP)             <https://caniuse.com/publickeypinning>
  Expect-CT                               <https://caniuse.com/mdn-http_headers_expect-ct>
  X-XSS-Protection                        <https://caniuse.com/mdn-http_headers_x-xss-protection>
  Clear-Site-Data                         <https://caniuse.com/?search=Clear-Site-Data>
  Cross-Origin-Embedder-Policy (COEP)     <https://caniuse.com/mdn-http_headers_cross-origin-embedder-policy>
  Cross-Origin-Opener-Policy (COOP)       <https://caniuse.com/mdn-http_headers_cross-origin-opener-policy>
  Cross-Origin-Resource-Policy (CORP)     <https://caniuse.com/mdn-http_headers_cross-origin-resource-policy>
  Permissions Policy                      <https://caniuse.com/permissions-policy>
  Cache-Control                           <https://caniuse.com/mdn-http_headers_cache-control>
  Pragma                                  <https://caniuse.com/mdn-http_headers_pragma>
:::

::::::::::::::::::::: {#sec-bestpractices .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Best Practices

- [Configuration proposal](#configuration-proposal)
- [Prevent information disclosure via HTTP
  headers](#prevent-information-disclosure-via-http-headers)
- [Prevent exposure to cross-site scripting when hosting uploaded
  files](#prevent-exposure-to-cross-site-scripting-when-hosting-uploaded-files)
- [Prevent CORS misconfiguration
  issues](#prevent-cors-misconfiguration-issues)
- [Prevent information disclosure via the browser local cached
  files](#prevent-information-disclosure-via-the-browser-local-cached-files)
- [Prevent CSP bypasses](#prevent-csp-bypasses)
- [Support for a large CSP policy](#support-for-a-large-csp-policy)

## Configuration proposal

Please note the best practices below suggest methods to change web
server configuration to add headers. Security headers can also be
successfully added to your application at the software level as well in
almost every web language. Many web frameworks add some of these headers
automatically.

The following section proposes a configuration for the [actively
supported and working draft security headers](index.html#div-headers).

💡 Additional information about HTTP security headers on
[OpenCRE](https://opencre.org/cre/636-347?name=OWASP+Secure+Headers+Project&section=configuration&link=https%3A%2F%2Fowasp.org%2Fwww-project-secure-headers%2F%23div-bestpractices).

📖 The headers proposed below can be applied both in the context of a
*classic web application* and in that of a *web API*.

🚩 Regarding the header `Content-Security-Policy`{.language-plaintext
.highlighter-rouge}, keep in mind that the policy applicability depends
on the execution context. Technical details are available
[here](https://www.w3.org/TR/CSP2/#which-policy-applies). Therefore, CSP
usage in a web API application implies to **define the CSP in the
document consuming the content of the web API**.

🚩 The header `Clear-Site-Data`{.language-plaintext .highlighter-rouge}
will cause the browser to take additional processing time for the HTTP
response, so, set it to the logout function when possible.

🔬 For the header `Permissions-Policy`{.language-plaintext
.highlighter-rouge}, as it is currently only supported by [Chromium
based browsers](https://caniuse.com/permissions-policy), the proposed
value was generated with this [site](https://www.permissionspolicy.com/)
and tested against the version `137.0.7124.0`{.language-plaintext
.highlighter-rouge} of
[Chromium](https://chromium.woolyss.com/download/en/) to only specify
supported features.

💡 Content of the table below is also provided, as JSON, via this
[file](ci/headers_add.json) (automatically updated).

  Header name                         Proposed value
  ----------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Strict-Transport-Security           `max-age=31536000; includeSubDomains`{.language-plaintext .highlighter-rouge}
  X-Frame-Options                     `deny`{.language-plaintext .highlighter-rouge}
  X-Content-Type-Options              `nosniff`{.language-plaintext .highlighter-rouge}
  Content-Security-Policy             `default-src 'self'; form-action 'self'; base-uri 'self'; object-src 'none'; frame-ancestors 'none'; upgrade-insecure-requests`{.language-plaintext .highlighter-rouge}
  X-Permitted-Cross-Domain-Policies   `none`{.language-plaintext .highlighter-rouge}
  Referrer-Policy                     `no-referrer`{.language-plaintext .highlighter-rouge}
  Clear-Site-Data                     `"cache","cookies","storage"`{.language-plaintext .highlighter-rouge}
  Cross-Origin-Embedder-Policy        `require-corp`{.language-plaintext .highlighter-rouge}
  Cross-Origin-Opener-Policy          `same-origin`{.language-plaintext .highlighter-rouge}
  Cross-Origin-Resource-Policy        `same-origin`{.language-plaintext .highlighter-rouge}
  Permissions-Policy                  `accelerometer=(), autoplay=(), camera=(), cross-origin-isolated=(), display-capture=(), encrypted-media=(), fullscreen=(), geolocation=(), gyroscope=(), keyboard-map=(), magnetometer=(), microphone=(), midi=(), payment=(), picture-in-picture=(), publickey-credentials-get=(), screen-wake-lock=(), sync-xhr=(self), usb=(), web-share=(), xr-spatial-tracking=(), clipboard-read=(), clipboard-write=(), gamepad=(), hid=(), idle-detection=(), interest-cohort=(), serial=(), unload=()`{.language-plaintext .highlighter-rouge}
  Cache-Control                       `no-store, max-age=0`{.language-plaintext .highlighter-rouge}

## Prevent information disclosure via HTTP headers

This section provides a collection of HTTP response headers to remove,
when possible, from any HTTP response to prevent any [disclosure of
technical information](https://cwe.mitre.org/data/definitions/200.html)
about environment. The following list of headers can be used to
configure a [reverse
proxy](https://www.nginx.com/resources/glossary/reverse-proxy-server/)
or a [web application
firewall](https://en.wikipedia.org/wiki/Web_application_firewall) to
handle removal operation of the mentioned headers.

💡 Additional information about technical information disclosure in HTTP
header on
[OpenCRE](https://www.opencre.org/cre/403-005?name=OWASP+Secure+Headers+Project&section=Prevent+information+disclosure+via+HTTP+headers&link=https%3A%2F%2Fowasp.org%2Fwww-project-secure-headers%2F%23div-bestpractices_prevent-information-disclosure-via-http-headers).

💡 When an HTTP response header is known by the analytics site
[WebTechSurvey](https://webtechsurvey.com/), then, a reference link is
added to its usage statistics page. Otherwise, a reference link
regarding the documentation of the header is provided.

🚩 The response header `Content-Type`{.language-plaintext
.highlighter-rouge} can sometimes discloses the web framework used. It
is the case for the following ones:

- [Spring Boot Actuator REST
  API](https://docs.spring.io/spring-boot/api/rest/actuator/auditevents.html):
  `Content-Type: application/vnd.spring-boot.actuator.v3+json`{.language-plaintext
  .highlighter-rouge}.

💡 Content of the table below is also provided, as JSON, via this
[file](ci/headers_remove.json) (automatically updated).

  Header name                                                                                                                                                     Header value example                                                                                       Description
  --------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  [Server](https://webtechsurvey.com/response-header/server)                                                                                                      `Apache/2.4.6 (CentOS) OpenSSL/1.0.2k-fips`{.language-plaintext .highlighter-rouge}                        Contain information about the server handling the request.
  [Liferay-Portal](https://webtechsurvey.com/response-header/liferay-portal)                                                                                      `Liferay Digital Experience Platform 7.2.10 GA1`{.language-plaintext .highlighter-rouge}                   Contain the version of the [Liferay](https://www.liferay.com/) software in use.
  [X-Turbo-Charged-By](https://webtechsurvey.com/response-header/x-turbo-charged-by)                                                                              `LiteSpeed/5.4.12 Enterprise`{.language-plaintext .highlighter-rouge}                                      Contain information about the server handling the request.
  [X-Powered-By](https://webtechsurvey.com/response-header/x-powered-by)                                                                                          `PHP/5.3.3`{.language-plaintext .highlighter-rouge}                                                        Contain information about hosting environments or other frameworks in use.
  [X-Server-Powered-By](https://webtechsurvey.com/response-header/x-server-powered-by)                                                                            `Engintron`{.language-plaintext .highlighter-rouge}                                                        Contain information about hosting environments or other frameworks in use.
  [X-Powered-CMS](https://webtechsurvey.com/response-header/x-powered-cms)                                                                                        `Bitrix Site Manager (DEMO)`{.language-plaintext .highlighter-rouge}                                       Contain the information about the [CMS](https://en.wikipedia.org/wiki/Content_management_system) that generated the HTTP response.
  [SourceMap](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/SourceMap)                                                                                `https://mysite.com/js/mylib.js.map`{.language-plaintext .highlighter-rouge}                               Links generated code to a [source map](https://developer.mozilla.org/en-US/docs/Tools/Debugger/How_to/Use_a_source_map) file, enabling the browser to reconstruct the original source and present the reconstructed original in the debugger.
  [X-SourceMap](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/SourceMap)                                                                              `https://mysite.com/js/mylib.js.map`{.language-plaintext .highlighter-rouge}                               Links generated code to a [source map](https://developer.mozilla.org/en-US/docs/Tools/Debugger/How_to/Use_a_source_map) file, enabling the browser to reconstruct the original source and present the reconstructed original in the debugger.
  [X-AspNetMvc-Version](https://webtechsurvey.com/response-header/x-aspnetmvc-version)                                                                            `5.2`{.language-plaintext .highlighter-rouge}                                                              Contain the version of the ASP .Net MVC framework in use.
  [X-AspNet-Version](https://webtechsurvey.com/response-header/x-aspnet-version)                                                                                  `4.0.30319`{.language-plaintext .highlighter-rouge}                                                        Contain the version of the ASP .Net framework Common Language Runtime (CLR) in use (see [here](https://github.com/OWASP/www-project-secure-headers/issues/215) for more details).
  [X-SourceFiles](https://webtechsurvey.com/response-header/x-sourcefiles)                                                                                        `=?UTF-8?B?QzpcVXNlcnN?=`{.language-plaintext .highlighter-rouge}                                          Contain information needed by the .Net SDK debugger during debugging operation on a project.
  [X-Redirect-By](https://webtechsurvey.com/response-header/x-redirect-by)                                                                                        `TYPO3 Shortcut/Mountpoint`{.language-plaintext .highlighter-rouge}                                        Specifies the component that is responsible for a particular redirect (source [Wikipedia](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields)).
  [X-Generator](https://webtechsurvey.com/response-header/x-generator)                                                                                            `Drupal 8`{.language-plaintext .highlighter-rouge}                                                         Contain the information about the [CMS](https://en.wikipedia.org/wiki/Content_management_system) that generated the HTTP response.
  [X-Generated-By](https://webtechsurvey.com/response-header/x-generated-by)                                                                                      `Smartsite version 7.11.1.3`{.language-plaintext .highlighter-rouge}                                       Contain the information about the [CMS](https://en.wikipedia.org/wiki/Content_management_system) that generated the HTTP response.
  [X-CMS](https://webtechsurvey.com/response-header/x-cms)                                                                                                        `Thinq CMS 1.7.0.0`{.language-plaintext .highlighter-rouge}                                                Contain the information about the [CMS](https://en.wikipedia.org/wiki/Content_management_system) that generated the HTTP response.
  [X-Powered-By-Plesk](https://webtechsurvey.com/response-header/x-powered-by-plesk)                                                                              `PleskLin`{.language-plaintext .highlighter-rouge} or `PleskWin`{.language-plaintext .highlighter-rouge}   Indicate that the platform is based on the [Plesk](https://www.plesk.com/) software in addition to the underlying operating system.
  [X-Php-Version](https://webtechsurvey.com/response-header/x-php-version)                                                                                        `7.4`{.language-plaintext .highlighter-rouge}                                                              Indicate the version of [PHP](https://www.php.net/) technology used.
  [Powered-By](https://webtechsurvey.com/response-header/powered-by)                                                                                              `PrestaShop`{.language-plaintext .highlighter-rouge}                                                       Indicate the name of the framework or platform used.
  [X-Content-Encoded-By](https://webtechsurvey.com/response-header/x-content-encoded-by)                                                                          `Joomla! 2.5`{.language-plaintext .highlighter-rouge}                                                      Indicate the name of the framework or platform used.
  [Product](https://webtechsurvey.com/response-header/product)                                                                                                    `Z-BlogPHP 1.7.2`{.language-plaintext .highlighter-rouge}                                                  Indicate the name of the framework or platform used.
  [X-CF-Powered-By](https://webtechsurvey.com/response-header/x-cf-powered-by)                                                                                    `CF-Joomla 0.1.5`{.language-plaintext .highlighter-rouge}                                                  Indicate the name of the framework or platform used.
  [X-Framework](https://webtechsurvey.com/response-header/x-framework)                                                                                            `JP/4.01`{.language-plaintext .highlighter-rouge}                                                          Indicate the name of the framework or platform used.
  [Host-Header](https://webtechsurvey.com/response-header/host-header)                                                                                            `owasp.org`{.language-plaintext .highlighter-rouge}                                                        Indicate which virtual host of the web server the response is coming from.
  [Pega-Host](https://webtechsurvey.com/response-header/pega-host)                                                                                                `srv-pega11`{.language-plaintext .highlighter-rouge}                                                       Indicate the internal host name of the server that handled the request in the context of usage of a software from the [PEGA](https://www.pega.com/) company.
  [X-Atmosphere-first-request](https://github.com/Atmosphere/atmosphere)                                                                                          `true`{.language-plaintext .highlighter-rouge}                                                             Indicate that the java framework [Atmosphere](https://github.com/Atmosphere/atmosphere) is used.
  [X-Atmosphere-tracking-id](https://github.com/Atmosphere/atmosphere)                                                                                            `7852fcbf-f8a9-4667-9dcc-a0b5b162499c`{.language-plaintext .highlighter-rouge}                             Indicate that the java framework [Atmosphere](https://github.com/Atmosphere/atmosphere) is used.
  [X-Atmosphere-error](https://github.com/Atmosphere/atmosphere)                                                                                                  `Websocket protocol not supported`{.language-plaintext .highlighter-rouge}                                 Indicate that the java framework [Atmosphere](https://github.com/Atmosphere/atmosphere) is used.
  [X-Mod-Pagespeed](https://webtechsurvey.com/response-header/x-mod-pagespeed)                                                                                    `1.13.35.2-0`{.language-plaintext .highlighter-rouge}                                                      Indicate the presence of the Apache module [mod_pagespeed](https://github.com/apache/incubator-pagespeed-mod) in the call flow.
  [X-Page-Speed](https://webtechsurvey.com/response-header/x-page-speed)                                                                                          `1.13.35.2-0`{.language-plaintext .highlighter-rouge}                                                      Indicate the presence of the Nginx module [mod_pagespeed](https://github.com/apache/incubator-pagespeed-ngx) in the call flow.
  [X-Varnish-Backend](https://webtechsurvey.com/response-header/x-varnish-backend)                                                                                `pb01`{.language-plaintext .highlighter-rouge}                                                             Indicate the name of the backend server from which the [Varnish](https://varnish-cache.org/) instance will accelerate the content.
  [X-Varnish-Server](https://webtechsurvey.com/response-header/x-varnish-server)                                                                                  `proxy01`{.language-plaintext .highlighter-rouge}                                                          Indicate the name of the [Varnish](https://varnish-cache.org/) server instance that provided the accelerated content.
  [X-Envoy-Upstream-Service-Time](https://webtechsurvey.com/response-header/x-envoy-upstream-service-time)                                                        `42`{.language-plaintext .highlighter-rouge}                                                               Indicate the presence of the proxy software [Envoy](https://www.envoyproxy.io/) in the call flow.
  [X-Envoy-Attempt-Count](https://webtechsurvey.com/response-header/x-envoy-attempt-count)                                                                        `1`{.language-plaintext .highlighter-rouge}                                                                Indicate the presence of the proxy software [Envoy](https://www.envoyproxy.io/) in the call flow.
  [X-Envoy-External-Address](https://www.envoyproxy.io/docs/envoy/latest/configuration/http/http_conn_man/headers)                                                `124.128.159.165`{.language-plaintext .highlighter-rouge}                                                  Indicate the presence of the proxy software [Envoy](https://www.envoyproxy.io/) in the call flow.
  [X-Envoy-Internal](https://www.envoyproxy.io/docs/envoy/latest/configuration/http/http_conn_man/headers)                                                        `true`{.language-plaintext .highlighter-rouge}                                                             Indicate the presence of the proxy software [Envoy](https://www.envoyproxy.io/) in the call flow.
  [X-Envoy-Original-Dst-Host](https://www.envoyproxy.io/docs/envoy/latest/configuration/http/http_conn_man/headers)                                               `10.195.16.237:8888`{.language-plaintext .highlighter-rouge}                                               Indicate the presence of the proxy software [Envoy](https://www.envoyproxy.io/) in the call flow.
  [X-B3-ParentSpanId](https://webtechsurvey.com/response-header/x-b3-parentspanid)                                                                                `dea3f6d0324583db`{.language-plaintext .highlighter-rouge}                                                 Indicate the presence of the software [Zipkin](https://zipkin.io/) that is a distributed tracing system.
  [X-B3-Sampled](https://webtechsurvey.com/response-header/x-b3-sampled)                                                                                          `0`{.language-plaintext .highlighter-rouge}                                                                Indicate the presence of the software [Zipkin](https://zipkin.io/) that is a distributed tracing system.
  [X-B3-SpanId](https://webtechsurvey.com/response-header/x-b3-spanid)                                                                                            `244753d494e83353`{.language-plaintext .highlighter-rouge}                                                 Indicate the presence of the software [Zipkin](https://zipkin.io/) that is a distributed tracing system.
  [X-B3-TraceId](https://webtechsurvey.com/response-header/x-b3-traceid)                                                                                          `11bef07b0f5c0468`{.language-plaintext .highlighter-rouge}                                                 Indicate the presence of the software [Zipkin](https://zipkin.io/) that is a distributed tracing system.
  [K-Proxy-Request](https://knative.dev/docs/serving/istio-authorization/)                                                                                        `activator`{.language-plaintext .highlighter-rouge}                                                        Indicate the presence of the software [Knative](https://knative.dev/) that is an Open-Source Enterprise-level solution to build Serverless and Event Driven Applications in Kubernetes environments.
  [X-Old-Content-Length](https://webtechsurvey.com/response-header/x-old-content-length)                                                                          `135`{.language-plaintext .highlighter-rouge}                                                              Indicate the presence of the software [WebSEAL](https://www.ibm.com/docs/en/samfm/8.0.1.2?topic=overview-webseal-introduction) that is a high performance, multithreaded web server by IBM.
  [\$wsep](https://www.ibm.com/docs/en/was/8.5.5?topic=SSEQTP_8.5.5/com.ibm.websphere.nd.multiplatform.doc/ae/rweb_custom_props.htm)                              `empty value`{.language-plaintext .highlighter-rouge}                                                      Indicate the presence of the software [WebSphere Application Server](https://www.ibm.com/products/websphere-application-server) that is a JavaEE application server by IBM.
  [X-Nextjs-Matched-Path](https://webtechsurvey.com/response-header/x-nextjs-matched-path)                                                                        `/blog`{.language-plaintext .highlighter-rouge}                                                            Indicate that the web framework [Next.js](https://nextjs.org/) is used.
  [X-Nextjs-Page](https://webtechsurvey.com/response-header/x-nextjs-page)                                                                                        `/articles`{.language-plaintext .highlighter-rouge}                                                        Indicate that the web framework [Next.js](https://nextjs.org/) is used.
  [X-Nextjs-Cache](https://webtechsurvey.com/response-header/x-nextjs-cache)                                                                                      `REVALIDATED`{.language-plaintext .highlighter-rouge}                                                      Indicate that the web framework [Next.js](https://nextjs.org/) is used.
  [X-Nextjs-Redirect](https://github.com/search?q=repo%3Avercel%2Fnext.js%20X-Nextjs-Redirect&type=code)                                                          `/home`{.language-plaintext .highlighter-rouge}                                                            Indicate that the web framework [Next.js](https://nextjs.org/) is used.
  [X-OneAgent-JS-Injection](https://webtechsurvey.com/response-header/x-oneagent-js-injection)                                                                    `true`{.language-plaintext .highlighter-rouge}                                                             Indicate that the [Dynatrace](https://www.dynatrace.com/) analytics and automation platform is used.
  [X-ruxit-JS-Agent](https://webtechsurvey.com/response-header/X-ruxit-JS-Agent)                                                                                  `true`{.language-plaintext .highlighter-rouge}                                                             Indicate that the [Dynatrace](https://www.dynatrace.com/) analytics and automation platform is used.
  [X-dtHealthCheck](https://www.dynatrace.com/support/help/platform-modules/digital-experience/web-applications/initial-setup/firewall-constraints-for-rum)       `Technical diagnostic data`{.language-plaintext .highlighter-rouge}                                        Indicate that the [Dynatrace](https://www.dynatrace.com/) analytics and automation platform is used.
  [X-dtAgentId](https://www.dynatrace.com/support/help/platform-modules/digital-experience/web-applications/initial-setup/firewall-constraints-for-rum)           `95b3121c36`{.language-plaintext .highlighter-rouge}                                                       Indicate that the [Dynatrace](https://www.dynatrace.com/) analytics and automation platform is used.
  [X-dtInjectedServlet](https://www.dynatrace.com/support/help/platform-modules/digital-experience/web-applications/initial-setup/firewall-constraints-for-rum)   `com.company.ReportServlet`{.language-plaintext .highlighter-rouge}                                        Indicate that the [Dynatrace](https://www.dynatrace.com/) analytics and automation platform is used.
  [X-Litespeed-Cache-Control](https://webtechsurvey.com/response-header/X-Litespeed-Cache-Control)                                                                `no-cache`{.language-plaintext .highlighter-rouge}                                                         Indicate the presence of the [LiteSpeed](https://litespeedtech.com/) web server.
  [X-LiteSpeed-Purge](https://webtechsurvey.com/response-header/X-LiteSpeed-Purge)                                                                                `/phpinfo.php`{.language-plaintext .highlighter-rouge}                                                     Indicate the presence of the [LiteSpeed](https://litespeedtech.com/) web server.
  [X-LiteSpeed-Tag](https://webtechsurvey.com/response-header/X-LiteSpeed-Tag)                                                                                    `pubtag1,pubtag2`{.language-plaintext .highlighter-rouge}                                                  Indicate the presence of the [LiteSpeed](https://litespeedtech.com/) web server.
  [X-LiteSpeed-Vary](https://webtechsurvey.com/response-header/X-LiteSpeed-Vary)                                                                                  `value=ismobile`{.language-plaintext .highlighter-rouge}                                                   Indicate the presence of the [LiteSpeed](https://litespeedtech.com/) web server.
  [X-LiteSpeed-Cache](https://webtechsurvey.com/response-header/X-LiteSpeed-Cache)                                                                                `hit,litemage`{.language-plaintext .highlighter-rouge}                                                     Indicate the presence of the [LiteSpeed](https://litespeedtech.com/) web server.
  [X-Umbraco-Version](https://webtechsurvey.com/response-header/X-Umbraco-Version)                                                                                `4.7`{.language-plaintext .highlighter-rouge}                                                              Indicate the usage of the [Umbraco CMS](https://umbraco.com/products/umbraco-cms/) software as well as its version.
  [OracleCommerceCloud-Version](https://webtechsurvey.com/response-header/OracleCommerceCloud-Version)                                                            `23.08.01`{.language-plaintext .highlighter-rouge}                                                         Indicate the usage of the [Oracle Commerce](https://www.oracle.com/cx/ecommerce/) software as well as its version.
  [X-BEServer](https://webtechsurvey.com/response-header/x-beserver)                                                                                              `EXSRV01`{.language-plaintext .highlighter-rouge}                                                          Indicate the internal host name of the server that handled the request in the context of usage of the [Microsoft Exchange](https://learn.microsoft.com/en-us/openspecs/exchange_server_protocols/ms-ashttp/08ad30b6-5b73-41bc-890b-1cab2cf49827) software.
  [X-DiagInfo](https://webtechsurvey.com/response-header/x-diaginfo)                                                                                              `EXSRV01`{.language-plaintext .highlighter-rouge}                                                          Indicate the internal host name of the server that handled the request in the context of usage of the [Microsoft Exchange](https://learn.microsoft.com/en-us/openspecs/exchange_server_protocols/ms-ashttp/08ad30b6-5b73-41bc-890b-1cab2cf49827) software.
  [X-FEServer](https://webtechsurvey.com/response-header/x-feserver)                                                                                              `EXSRV01`{.language-plaintext .highlighter-rouge}                                                          Indicate the internal host name of the server that handled the request in the context of usage of the [Microsoft Exchange](https://learn.microsoft.com/en-us/openspecs/exchange_server_protocols/ms-ashttp/08ad30b6-5b73-41bc-890b-1cab2cf49827) software.
  [X-CalculatedBETarget](https://webtechsurvey.com/response-header/x-calculatedbetarget)                                                                          `exsrv01.mydomain.com`{.language-plaintext .highlighter-rouge}                                             Indicate the internal host name of the server that handled the request in the context of usage of the [Microsoft Exchange](https://learn.microsoft.com/en-us/openspecs/exchange_server_protocols/ms-ashttp/08ad30b6-5b73-41bc-890b-1cab2cf49827) software.
  [X-OWA-Version](https://webtechsurvey.com/response-header/x-owa-version)                                                                                        `15.2.1258.27`{.language-plaintext .highlighter-rouge}                                                     Indicate the version of the Microsoft Exchange software in use.
  [X-Cocoon-Version](https://webtechsurvey.com/response-header/x-cocoon-version)                                                                                  `2.1.13`{.language-plaintext .highlighter-rouge}                                                           Indicate that the web framework [Apache Cocoon](https://cocoon.apache.org/) is used as well as the version used.
  [X-Kubernetes-PF-FlowSchema-UI](https://kubernetes.io/docs/reference/debug-cluster/flow-control)                                                                `cf931e2d-5a5e-4c12-892c-9bafa71f30dc`{.language-plaintext .highlighter-rouge}                             Indicate that the web application issuing the HTTP response is deployed on a [Kubernetes](https://kubernetes.io/) cluster.
  [X-Kubernetes-PF-PriorityLevel-UID](https://kubernetes.io/docs/reference/debug-cluster/flow-control)                                                            `78b3face-e1cf-4fc6-a27e-08eb7f0f5b23`{.language-plaintext .highlighter-rouge}                             Indicate that the web application issuing the HTTP response is deployed on a [Kubernetes](https://kubernetes.io/) cluster.
  [X-Jitsi-Release](https://webtechsurvey.com/response-header/x-jitsi-release)                                                                                    `5082`{.language-plaintext .highlighter-rouge}                                                             Indicate the version of [Jitsi](https://github.com/jitsi/jitsi) software in use.
  [X-Joomla-Version](https://webtechsurvey.com/response-header/x-joomla-version)                                                                                  `3.9.25`{.language-plaintext .highlighter-rouge}                                                           Indicate that the CMS [Joomla](https://www.joomla.org/) is used as well as the version used.
  [X-Backside-Transport](https://webtechsurvey.com/response-header/x-backside-transport)                                                                          `OK OK`{.language-plaintext .highlighter-rouge}                                                            Indicate the presence of the products [IBM WebSphere DataPower](https://www.ibm.com/products/datapower-gateway) in the call flow.

## Prevent exposure to cross-site scripting when hosting uploaded files

This section describes, how the HTTP response header named
[Content-Disposition](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Disposition),
can be used to prevent exposure to cross-site scripting when hosting
uploaded files and opening them in the same web browsing context than
the application.

It can happen a case in which an application allows a user to upload a
file and then allow this file to be accessed by other users. If such
feature allows uploading of HTML files (also apply for [SVG
file](https://hackerone.com/reports/1276742)) then it can be used, as a
vector, to store an HTML file containing JavaScript code. Therefore, the
feature become prone to [stored cross-site
scripting](https://portswigger.net/web-security/cross-site-scripting/stored)
vulnerability.

To prevent this exposure, the HTTP response header named
[Content-Disposition](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Disposition),
can be used with the following value to instruct browsers to download
the file instead of open it in the same web browsing context than the
application:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
Content-Disposition: attachment; filename="myfile.html"
```
:::
::::

## Prevent CORS misconfiguration issues

> 📖 An excellent tutorial about [Cross-Origin Resource
> Sharing](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
> (called **CORS**) is provided on the [Mozilla
> MDN](https://developer.mozilla.org/en-US/). In addition, [Julien
> Cretel](https://jub0bs.com/about/) provided a great [blog
> post](https://jub0bs.com/posts/2023-02-08-fearless-cors/) about CORS
> pitfalls.

This section proposes an approach to help preventing [CORS
misconfiguration
issues](https://portswigger.net/research/exploiting-cors-misconfigurations-for-bitcoins-and-bounties)
using a simple idea: *Provide the collection of [CORS related HTTP
response
headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#the_http_response_headers)
to use according to different contexts.*

### Key points to consider

- 💡 If the web framework/web server you are using provides CORS
  features then always leverage them instead of implements it manually:
  - [List of web framework/web
    server](https://enable-cors.org/server.html) supporting CORS.
  - [CORS middleware for Go](https://pkg.go.dev/github.com/jub0bs/cors)
    by Julien Cretel.

- 🚩 Whatever the context, when the request is a **HTTP OPTIONS**
  ([preflight
  request](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#preflighted_requests))
  then the value provided by the following headers must be validated
  against expected values. If the validation failed then return an HTTP
  403 **without any [CORS related HTTP response
  headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#the_http_response_headers)**:

  - [Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#origin)
  - [Access-Control-Request-Method](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#access-control-request-method)
  - [Access-Control-Request-Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#access-control-request-headers)

- 🚩 Validation of the `Origin`{.language-plaintext .highlighter-rouge}
  / `Access-Control-Request-Method`{.language-plaintext
  .highlighter-rouge} /
  `Access-Control-Request-Headers`{.language-plaintext
  .highlighter-rouge} request header value, against a list of allowed
  ones, must be performed using [strict case sensitive string
  comparison](https://jub0bs.com/posts/2023-02-08-fearless-cors/#violation-of-the-case-sensitivity-of-method-names)
  to prevent, as much as possible, the [presence of bypasses into the
  validation
  logic](https://portswigger.net/web-security/cors#errors-parsing-origin-headers).
  If possible, does not use regular expression for the implementation of
  the validation, see
  [here](https://jub0bs.com/posts/2023-02-08-fearless-cors/#disallow-dangerous-origin-patterns)
  for an explanation of the source of this recommendation.

- 🚩 CORS scope is the access control aspect, from a browser perspective
  (client side), regarding [cross
  origins](https://developer.mozilla.org/en-US/docs/Glossary/Origin)
  access to a resource. Thus, it **does NOT replace** the requirement to
  implements access control on the server side too. CORS and server-side
  access controls are complementary.

- 🚩 Never take the value of the request header
  [Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#origin)
  to add it into the response header
  [Access-Control-Allow-Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#access-control-allow-origin)
  (mirroring), see
  [here](https://portswigger.net/web-security/cors#server-generated-acao-header-from-client-specified-origin-header)
  for an explanation of the source of this recommendation. Indeed,
  always use a list of allowed origins when only a restricted collection
  of origins is expected to call your endpoints.

### Contexts

#### Public without authentication

💬 Context:

Your endpoints are expected to be consumed, by a browser, from any
origins without any authentication.

💻 Configuration proposal:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
Access-Control-Allow-Origin: *
Access-Control-Max-Age: 3600
Access-Control-Allow-Credentials: false
```
:::
::::

#### Public with authentication

💬 Context:

Your endpoints are expected to be consumed, by a browser, from any
origins with authentication.

🚩 The value `*`{.language-plaintext .highlighter-rouge}, for the
response header `Access-Control-Allow-Origin`{.language-plaintext
.highlighter-rouge}, cannot be used when the response header
`Access-Control-Allow-Credentials`{.language-plaintext
.highlighter-rouge} is allowed (`true`{.language-plaintext
.highlighter-rouge}). Indeed, the browser raises the following error
(tested on Chrome 118.x):

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
The value of the 'Access-Control-Allow-Origin' header in the response must not be 
the wildcard '*' when the request's credentials mode is 'include'.
```
:::
::::

📖 It is explicitly mentioned, into the [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#simple_requests)
documentation, as the following:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
When responding to a "credentialed request" request, the server must specify an origin in the value 
of the Access-Control-Allow-Origin header, instead of specifying the "*" wildcard.
```
:::
::::

Therefore, refer to the [restricted with
authentication](#restricted-with-authentication) case for the
configuration to use.

#### Restricted without authentication

💬 Context:

Your endpoints are expected to be consumed, by a browser, from a
specific collection of origins without any authentication.

💻 Configuration proposal:

- If the value of the request header
  [Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#origin)
  is present into the **list of allowed Origins** then:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
Access-Control-Allow-Origin: [Value_Taken_From_The_List_Of_Allowed_Origins]
Access-Control-Max-Age: 10
Access-Control-Allow-Credentials: false
```
:::
::::

- Otherwise return an HTTP 403 **without any [CORS related HTTP response
  headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#the_http_response_headers)**.

#### Restricted with authentication

💬 Context:

Your endpoints are expected to be consumed, by a browser, from a
specific collection of origins with authentication.

💻 Configuration proposal:

- If the value of the request header
  [Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#origin)
  is present into the **list of allowed Origins** then:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
Access-Control-Allow-Origin: [Value_Taken_From_The_List_Of_Allowed_Origins]
Access-Control-Max-Age: 10
Access-Control-Allow-Credentials: true
```
:::
::::

- Otherwise return an HTTP 403 **without any [CORS related HTTP response
  headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#the_http_response_headers)**.

### Test CORS configuration

The tools [nuclei](https://github.com/projectdiscovery/nuclei) can be
used, via the template named
[cors-misconfig](https://github.com/projectdiscovery/nuclei-templates/blob/main/http/vulnerabilities/generic/cors-misconfig.yaml),
to test a CORS configuration.

💻 Command to use:

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
$ nuclei -silent -template-id cors-misconfig -u https://domain.com
[cors-misconfig:arbitrary-origin] [http] [info] https://domain.com [...]
```
:::
::::

### References {#references}

- <https://portswigger.net/web-security/cors>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS>
- <https://jub0bs.com/posts/2023-02-08-fearless-cors/>
- <https://enable-cors.org/>
- <https://developer.mozilla.org/en-US/docs/Glossary/Origin>
- <https://cwe.mitre.org/data/definitions/942.html>
- <https://cwe.mitre.org/data/definitions/346.html>
- [OWASP WSTG - Testing Cross Origin Resource
  Sharing](../www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/07-Testing_Cross_Origin_Resource_Sharing.html)
- <https://pkg.go.dev/github.com/jub0bs/cors>

## Prevent information disclosure via the browser local cached files

This section describes why it is important to specify a **caching
policy**, via the
[Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)
HTTP response header, when sensitive information is managed by a
web-based application.

### Context

💬 The application allows a user to access to documents containing
information, considered sensitive, from a confidentiality perspective.

Let's assume that the application returns the following HTTP response to
a request, in which, no caching policy is defined:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
HTTP/1.1 200 OK
accept-ranges: bytes
content-length: 433994
content-type: application/pdf
date: Sat, 30 Mar 2024 10:06:34 GMT
server: LiteSpeed
```
:::
::::

So, the browser will store a copy of the file (here a PDF one) into its
cache storage for a certain amount of time.

🚩 **Consequence:** Any application running on the user's computer, will
be able to access to the file (at least if executed as the user identity
or an administrator one) causing an exposure of the resource to
non-expected entities.

📺 This [demonstration
video](assets/misc/demo_information_disclosure_via_browser_file_caching.mp4)
show an example, of such information disclosure, via a file cached by
the browser.

### Configuration proposal

💻 To prevent such issue, the following **caching policy** can be
specified:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
Cache-Control: no-store, max-age=0
```
:::
::::

👀 Where:

- `no-store`{.language-plaintext .highlighter-rouge}: Is used to
  indicate that the response may not be stored in any cache.
- `max-age=0`{.language-plaintext .highlighter-rouge}: Is used to force
  the expiration of any cached version of the resources associated to
  the response.

💡 The HTTP response header
[Clear-Site-Data](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Clear-Site-Data)
can also be leveraged, in addition, to instruct the browser to remove
any cached data related to the application.

### Other vulnerabilities related to caching

📖 An excellent research and course content, about [web cache
poisoning](https://portswigger.net/web-security/web-cache-poisoning), is
provided by the [PortSwigger team](https://portswigger.net/).

### References {#references-1}

- [https://redbot.org](https://redbot.org/)
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching>
- <https://caniuse.com/mdn-http_headers_cache-control>
- <https://cwe.mitre.org/data/definitions/525.html>
- <https://cwe.mitre.org/data/definitions/524.html>
- [OWASP WSTG - Testing for Browser Cache
  Weaknesses](../www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/04-Authentication_Testing/06-Testing_for_Browser_Cache_Weaknesses.html)
- <https://portswigger.net/kb/issues/00700100_cacheable-https-response>
- <https://portswigger.net/web-security/web-cache-poisoning>
- <https://portswigger.net/web-security/web-cache-deception>
- <https://portswigger.net/research/gotta-cache-em-all>

## Prevent CSP bypasses

This section describes some points, to keep in mind, during the creation
of a
[Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)
(called **CSP**) policy to prevent introducing bypasses.

🚩 Not every
**[directives](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy#directives)**
fallback to the
**[default-src](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/default-src)**
directive when it is not specified in the CSP policy.

### Directive form-action

👀 It is the case for the
**[form-action](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/form-action)**
directive. Therefore, an html form can be used to bypass the CSP in
place when the `form-action`{.language-plaintext .highlighter-rouge} is
not defined.

📺 This [demonstration
video](assets/misc/demo_csp_bypass_due_to_no_form_action_directive.mp4)
show an example.

💡 Therefore, ensure to always specify the
`form-action`{.language-plaintext .highlighter-rouge} directive in a CSP
policy to at least, the `'self'`{.language-plaintext .highlighter-rouge}
value, to allow forms only on the current domain.

### Directive frame-ancestors

👀 It is the case for the
**[frame-ancestors](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors)**
directive. Therefore, IF it is not defined **AND** IF the header
[X-Frame-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)
is not/incorrectly specified then the current domain can be embedded
into a frame.

📺 This [demonstration
video](assets/misc/demo_csp_bypass_due_to_no_frame_ancestors_directive.mp4)
show an example.

💡 Therefore, ensure to always specify the
`frame-ancestors`{.language-plaintext .highlighter-rouge} directive in a
CSP policy to at least, the `'none'`{.language-plaintext
.highlighter-rouge} value, to deny the current domain to be "framed".

### Directive base-uri

👀 It is the case for the
**[base-uri](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/base-uri)**
directive.

📺 This [demonstration
video](assets/misc/demo_csp_bypass_due_to_no_base_uri_directive.mp4)
show an example.

💡 Therefore, ensure to always specify the
`base-uri`{.language-plaintext .highlighter-rouge} directive in a CSP
policy to at least, the `'self'`{.language-plaintext .highlighter-rouge}
value, to only allow the current domain to be specified as the
document's base URI via a `<base href="..." />`{.language-plaintext
.highlighter-rouge} html tag.

## Support for a large CSP policy

Tests were performed to identify if any limitation was in place,
regarding the definition and usage of a large CSP policy. Tests were
performed against the following browsers:

- Firefox `132.0.2`{.language-plaintext .highlighter-rouge}.
- Chromium `131.0.6755.0`{.language-plaintext .highlighter-rouge}.
- Edge `131.0.2903.51`{.language-plaintext .highlighter-rouge}.

💡 Based on tests performed, modern browsers supports a sufficient size
to specify a large CSP policy in case of need.

📊 Technical details can be found
[here](https://github.com/oshp/oshp-tracking/discussions/29) ([backup
copy](assets/misc/backup_discussions_29.pdf)).
:::::::::::::::::::::

::: {#sec-technical .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Technical Resources

📚 This section provides a list of tools as well as documents to
understand, analyze, develop and administer HTTP secure headers to help
achieving more secure and trustworthy web systems.

- 📺 [Presentations](#presentations)
- 🏭 [Analysis Tools](#analysis-tools)
- 👩‍💻 [Development Libraries](#development-libraries)
  - [DotNet](#dotnet)
  - [Go](#go)
  - [Java](#java)
  - [NodeJS](#nodejs)
  - [PHP](#php)
  - [Python](#python)
  - [Ruby](#ruby)
  - [Swift](#swift)

## Presentations

- [Trap bad guys in your browser with HTTP security
  headers](https://speakerdeck.com/righettod/trap-bad-guys-in-your-browser-with-http-security-headers).
- [How the Content-Security-Policy HTTP response header can save your
  romantic
  evening?](https://speakerdeck.com/righettod/how-the-content-security-policy-http-response-header-can-save-your-romantic-evening)

## Analysis Tools

  Tool                       Description                                                                                                                                                 Ref
  -------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------
  **hsecscan**               A security scanner for HTTP response headers.                                                                                                               [👩‍💻](https://github.com/riramar/hsecscan)
  **humble**                 A humble, and fast, security-oriented HTTP headers analyzer.                                                                                                [👩‍💻](https://github.com/rfc-st/humble)
  **testssl.sh**             Easy to use shell script which tests not only SSL/TLS encryption but also checks common headers and analyzes those. Output is screen, JSON, CSV and HTML.   [👩‍💻](https://github.com/drwetter/testssl.sh)
  **DrHEADer**               DrHEADer helps with the audit of security headers received in response to a single request or a list of requests.                                           [👩‍💻](https://github.com/Santandersecurityresearch/DrHeader)
  **csp-evaluator**          NPM module allowing developers and security experts to check if a Content Security Policy serves as a strong mitigation against XSS attacks.                [👩‍💻](https://github.com/google/csp-evaluator)
  **mdn-http-observatory**   Service by Mozilla that checks web sites for security-relevant headers.                                                                                     [👩‍💻](https://github.com/mdn/mdn-http-observatory)

## Development Libraries

### Java

  Library               Description                                                                      Ref
  --------------------- -------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------
  **Spring Security**   Spring Security's support for adding various security headers to the response.   [🌎](https://docs.spring.io/spring-security/reference/features/exploits/headers.html)

### DotNet

  Library                                       Description                                                                                    Ref
  --------------------------------------------- ---------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------
  **NetEscapades.AspNetCore.SecurityHeaders**   Small package to allow adding security headers to ASP.NET Core websites.                       [👩‍💻](https://github.com/andrewlock/NetEscapades.AspNetCore.SecurityHeaders)
  **OwaspHeaders.Core**                         .NET Core middleware for injecting the OWASP recommended HTTP Headers for increased security   [👩‍💻](https://github.com/GaProgMan/OwaspHeaders.Core)

### Ruby

  Library              Description                                Ref
  -------------------- ------------------------------------------ ------------------------------------------------
  **secure_headers**   Security related headers all in one gem.   [👩‍💻](https://github.com/github/secure_headers)

### PHP

  Library              Description                                                                        Ref
  -------------------- ---------------------------------------------------------------------------------- ----------------------------------------------------
  **SecureHeaders**    A PHP class aiming to make the use of browser security features more accessible.   [👩‍💻](https://github.com/aidantwoods/SecureHeaders)
  **secure-headers**   PHP Secure Headers for Laravel and non-Laravel projects.                           [👩‍💻](https://github.com/bepsvpt/secure-headers)

### NodeJS

  Library                                 Description                                                                                                                                                                                                                      Ref
  --------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------
  **helmet**                              Module to help secure Express apps with various HTTP headers.                                                                                                                                                                    [👩‍💻](https://github.com/helmetjs/helmet)
  **ember-cli-content-security-policy**   This addon makes it easy to use Content Security Policy (CSP) in your project. It can be deployed either via a Content-Security-Policy header sent from the Ember CLI Express server, or as a meta tag in the index.html file.   [👩‍💻](https://github.com/rwjblue/ember-cli-content-security-policy/)
  **blankie**                             A CSP plugin for [hapi](https://github.com/hapijs/hapi).                                                                                                                                                                         [👩‍💻](https://github.com/nlf/blankie)

### Python

  Library                              Description                                                                                                                  Ref
  ------------------------------------ ---------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------
  **django-csp and django-security**   Content Security Policy for Django. A collection of models, views, middlewares, and forms to help secure a Django project.   [👩‍💻](https://github.com/mozilla/django-csp) / [👩‍💻](https://github.com/sdelements/django-security)
  **Secweb**                           Secweb is a pack of security middlewares for fastApi and starlette server it includes CSP, HSTS, and many more.              [👩‍💻](https://github.com/tmotagam/Secweb)
  **secure**                           Lightweight library to add security headers to Django, Flask, FastAPI, and more.                                             [👩‍💻](https://github.com/TypeError/secure)

### Go

  Library      Description                                                         Ref
  ------------ ------------------------------------------------------------------- ------------------------------------------
  **secure**   HTTP middleware for Go that facilitates some quick security wins.   [👩‍💻](https://github.com/unrolled/secure)

### Swift

  Library                    Description                                                                   Ref
  -------------------------- ----------------------------------------------------------------------------- -------------------------------------------------------------
  **VaporSecurityHeaders**   A Middleware library for adding security headers to your Vapor application.   [👩‍💻](https://github.com/brokenhandsio/VaporSecurityHeaders)
:::

::::::::::::::::: {#sec-codesnippets .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Code Snippets

🧾 The following code collection provides various code snippets to make
working with HTTP security headers easier.

- [Convert a Permissions-Policy back to
  Feature-Policy](#convert-a-permissions-policy-back-to-feature-policy)
- [Test locally a Content-Security-Policy for
  weaknesses](#test-locally-a-content-security-policy-for-weaknesses)
- [Generate configuration code using the OSHP headers reference
  files](#generate-configuration-code-using-the-oshp-headers-reference-files)
- [Quickly check security HTTP
  headers](#quickly-check-security-http-headers)
- [Syntax for adding HTTP response headers on different web or
  application
  servers](#syntax-for-adding-http-response-headers-on-different-web-or-application-servers)

## Convert a Permissions-Policy back to Feature-Policy

As the
[Permissions-Policy](https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md)
header is still in development and is [not yet well
supported](https://caniuse.com/permissions-policy), it can be
interesting to use the two formats to increase the coverage of browsers
according to their support level for **Permissions-Policy** and
**[Feature-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy)**
policy headers.

The following *python3* code snippet can be useful to achieve such
conversion.

📑 Source for the conversion rules was this
[one](https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md#appendix-big-changes-since-this-was-called-feature-policy).

💻 Code snippet:

:::: {.language-python .highlighter-rouge}
::: highlight
``` highlight
permissions_policy = 'fullscreen=(), geolocation=(self "https://game.com" "https://map.example.com"), gyroscope=(self), usb=*'
feature_policy_directives = []
# Collect directives
permissions_policy_directives = permissions_policy.split(",")
# Process each directive
for permissions_policy_directive in permissions_policy_directives:
    # Remove leading and trailing spaces
    directive = permissions_policy_directive.strip(" ")
    # Remove all double quotes
    directive = directive.replace("\"", "")
    # Replace disabling expression () by the corresponding one in Feature-Policy
    directive = directive.replace("()", "'none'")
    # Quote keywords: self
    directive = directive.replace("self", "'self'")
    # Replace the equals affectation character by a space
    directive = directive.replace("=", " ")
    # Remove parenthesis
    directive = directive.replace("(", "").replace(")", "")
    # Add the current directive to the collection
    feature_policy_directives.append(directive)
# Convert the collection of directives to a string with ; as directives separator
feature_policy = "; ".join(feature_policy_directives)
print(feature_policy)
```
:::
::::

💻 Execution example:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
$ python code.py
fullscreen 'none'; geolocation 'self' https://game.com https://map.example.com; gyroscope 'self'; usb *
```
:::
::::

## Test locally a Content-Security-Policy for weaknesses

It can be interesting to validate locally a **Content-Security-Policy**
for presence of weaknesses prior to apply it on deployed web
applications.

The following *JavaScript* code snippet can be useful to achieve such
validation by leveraging the
[csp-evaluator](https://github.com/google/csp-evaluator) NPM module
provided by Google.

💻 Code snippet:

:::: {.language-javascript .highlighter-rouge}
::: highlight
``` highlight
import {CspEvaluator} from "csp_evaluator/dist/evaluator.js";
import {CspParser} from "csp_evaluator/dist/parser.js";

const args = process.argv.slice(2)
if(args.length == 0){
    console.error("[!] Missing CSP!");
}else{
    const csp = args[0]
    console.info(`[+] CSP to evaluate:\n${csp}`);
    const parsed = new CspParser(csp).csp;
    console.info(`[+] Evaluation results:`);
    const results = new CspEvaluator(parsed).evaluate();
    results.forEach(elt => {
        let info = `[Directive '${elt.directive}' - Severity ${elt.severity}]: ${elt.description}`;
        console.info(info);
    });
}
```
:::
::::

💻 Execution example:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
$ node code.js "default-src 'self'; object-src 'none'; frame-ancestors 'none'; upgrade-insecure-requests"
[+] CSP to evaluate:
default-src 'self'; object-src 'none'; frame-ancestors 'none'; upgrade-insecure-requests
[+] Evaluation results:
[Directive 'default-src' - Severity 50]: 'self' can be problematic if you host JSONP, Angular or user uploaded files.
```
:::
::::

## Generate configuration code using the OSHP headers reference files

The following *bash* code snippet, leveraging
[jq](https://stedolan.github.io/jq/), can be used to generate
configuration code using the OSHP headers reference files.

💻 Code snippet and execution example:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
# Generate the Nginx collection of instructions to add the recommended HTTP response headers
$ curl -sk https://owasp.org/www-project-secure-headers/ci/headers_add.json | jq -r '.headers[] | "add_header \(.name) \(.value);"'
add_header Cache-Control no-store, max-age=0;
add_header Clear-Site-Data "cache","cookies","storage";
add_header Cross-Origin-Embedder-Policy require-corp;
...
```
:::
::::

## Quickly check security HTTP headers

The portable cross-platform tool [Venom](https://github.com/ovh/venom)
with the dedicated [OSHP Validator test suites aligned with the OWASP
Secure Headers Project](https://github.com/oshp/oshp-validator) can be
used.

💻 Use the following example set of commands:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
$ venom run --var="target_site=https://mozilla.org" --var="logout_url=/logout" tests_suite.yml
• HTTP security response headers test suites
    • Strict-Transport-Security SUCCESS
    • X-Frame-Options SUCCESS
    • X-Content-Type-Options SUCCESS
    • Content-Security-Policy FAILURE
    • X-Permitted-Cross-Domain-Policies SUCCESS
    • Referrer-Policy SUCCESS
    • Clear-Site-Data SUCCESS
    • Cross-Origin-Embedder-Policy SUCCESS
    • Cross-Origin-Opener-Policy SUCCESS
    • Cross-Origin-Resource-Policy SUCCESS
    • Permissions-Policy SUCCESS    
    • Cache-Control SUCCESS    
    • Feature-Policy SUCCESS
        [info] This header was split into Permissions-Policy and Document-Policy and will be considered deprecated once all impacted features are moved off of feature policy.
    • Public-Key-Pins SUCCESS
        [info] This header has been deprecated by all major browsers and is no longer recommended. Avoid using it, and update existing code if possible!
    • Expect-CT SUCCESS
        [info] This header will likely become obsolete in June 2021. Since May 2018 new certificates are expected to support SCTs by default. Certificates before March 2018 were allowed to have a lifetime of 39 months, those will all be expired in June 2021.
    • X-Xss-Protection SUCCESS
        [info] The X-XSS-Protection header has been deprecated by modern browsers and its use can introduce additional security issues on the client side.
```
:::
::::

## Syntax for adding HTTP response headers on different web or application servers

Use the following steps to leverage an "LLM as a Service" (LLMaaS) to
generate corresponding configuration code snippet for the wanted web or
application server:

1.  Download this [file](ci/headers_add.json).
2.  Join the json file above to the chat.
3.  Use this user prompt in the chat to ask the generation:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
Generate a configuration code snippet to set HTTP response security headers for the '[TARGET_APPLICATION_OR_WEB_SERVER_NAME]'. Use only the information from the json file attached. Only provide the configuration code snippet. The configuration must overwrite any existing value for an HTTP response security header present into the json file attached.
```
:::
::::

🔬 The user prompt proposed was tested against [Google
GEMINI](https://gemini.google.com/) model **2.5 Flash** and the
generated configuration code was submitted to [OpenAI
ChatGPT](https://chatgpt.com/) model **ChatGPT** to indicates if it was
valid for the intended web or application server. The following value
for the `[TARGET_APPLICATION_OR_WEB_SERVER_NAME]`{.language-plaintext
.highlighter-rouge} placeholder were used:

- `apache web server`{.language-plaintext .highlighter-rouge}.
- `nginx web server`{.language-plaintext .highlighter-rouge}.
- `lighttpd web server`{.language-plaintext .highlighter-rouge}.
- `litespeed web server`{.language-plaintext .highlighter-rouge}.
- `caddy web server`{.language-plaintext .highlighter-rouge}.
- `iis web server`{.language-plaintext .highlighter-rouge}.
:::::::::::::::::

::::::::::: {#sec-misc .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Miscellaneous

💡 This section provides extra useful information about HTTP Security
headers.

- [Private Network Access request
  header](#private-network-access-request-header)
- [Fetch metadata request header](#fetch-metadata-request-header)

## Request headers

### Private Network Access request header

⚠️ Work on this feature was **put on hold by Google** in favor of a new
feature called **[Local Network
Access](https://github.com/explainers-by-googlers/local-network-access)**
for which *work is in progress*:

- [Private Network Access on
  hold](https://developer.chrome.com/blog/pna-on-hold).
- [Inquiry About Chrome Origin Trials Extension and Future
  Availability](https://github.com/WICG/private-network-access/issues/148).
- [Discussion thread about this
  topic](https://groups.google.com/a/chromium.org/g/blink-dev/c/NCV3anf1KtU/m/WyL9rKjtAQAJ?pli=1).

#### Description {#description}

The [Private Network
Access](https://wicg.github.io/private-network-access/) specification
provides a feature allowing an application, located on a **[private
address](https://wicg.github.io/private-network-access/#ip-address-space-private)**,
to identify if the incoming HTTP request was sent from an application
located on a **[public
address](https://wicg.github.io/private-network-access/#public-address)**.

🎯 The objective is to prevent attack, in which, a page hosted on a
public network like, the Internet network, try to send a request to an
application hosted on a private network:

![PNA schema](assets/images/miscellaneous_pna_request_header_schema.png)

📑
[Source](https://developer.chrome.com/blog/private-network-access-update/#what-is-private-network-access)
of the schema.

#### Example {#example}

💻 Code of a page hosted on Internet on
`https://example.com/page.html`{.language-plaintext .highlighter-rouge}:

:::: {.language-html .highlighter-rouge}
::: highlight
``` highlight
<!DOCTYPE html>
<html>
<header>
    <title>Evil App</title>
</header>
<body>
    <!-- 
        We try to load an image from the router
        deployed on the local private network.
    -->
    <img src="https://router.local/icon.svg">
</body>
</html>
```
:::
::::

💻 Request sent by the browser when the page is loaded (tested on
`Chrome 116.x`{.language-plaintext .highlighter-rouge}):

:::: {.language-html .highlighter-rouge}
::: highlight
``` highlight
OPTIONS /icon.svg HTTP/1.1
Host: router.local
User-Agent: Chrome/116.0.0.0 Safari/537.36
Accept: */*
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en-GB;q=0.9,en;q=0.8
Access-Control-Request-Method: GET
Access-Control-Request-Private-Network: true
Connection: keep-alive
Origin: https://example.com
Referer: https://example.com
Sec-Fetch-Dest: image
Sec-Fetch-Mode: cors
Sec-Fetch-Site: cross-site
```
:::
::::

💬 The browser sent a [CORS preflight
request](https://fetch.spec.whatwg.org/#cors-preflight-request) to
**notify the application**, located on the private network, about the
**cross-network** request that the application, located on the public
network, want to perform.

💡 Note the special **request** header:
`Access-Control-Request-Private-Network: true`{.language-plaintext
.highlighter-rouge}

🤝 If the application on the private network, wants to allow the
request, then it will return the following CORS headers that will *make
the preflight successful*:

💡 Note the special **response** header:
`Access-Control-Allow-Private-Network: true`{.language-plaintext
.highlighter-rouge}

:::: {.language-html .highlighter-rouge}
::: highlight
``` highlight
HTTP/1.1 200 OK
Access-Control-Allow-Origin: https://example.com
Access-Control-Allow-Methods: GET
Access-Control-Allow-Private-Network: true
...
```
:::
::::

📍 To summarize, the application on the private network, uses its
response to the preflight request to allow or not the real request to be
performed:

- ✅ **Preflight succeed**: The browser will send the real request (HTTP
  GET in our example).
- ❌ **Preflight fail**: The browser will NOT send the real request.

#### References {#references}

- <https://developer.chrome.com/blog/private-network-access-update>
- <https://wicg.github.io/private-network-access/>
- <https://github.com/WICG/private-network-access>
- <https://portswigger.net/daily-swig/chrome-to-bolster-csrf-protections-with-cors-preflight-checks-on-private-network-requests>
- <https://developer.mozilla.org/en-US/docs/Glossary/Preflight_request>

### Fetch metadata request header

A fetch metadata request header is an HTTP request header that provides
additional information about the context from which the request
originated. This allows the server to make decisions about whether a
request should be allowed based on where the request came from and how
the resource will be used .

🔒 These headers are prefixed with `Sec-`{.language-plaintext
.highlighter-rouge}, and hence have [forbidden header
names](https://developer.mozilla.org/en-US/docs/Glossary/Forbidden_header_name).
As such, they *cannot be modified from JavaScript*.

📑 Source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Glossary/Fetch_metadata_request_header).

🎯 These headers can be leveraged to add protection measures against
[XS-Leaks](https://xsleaks.dev/docs/defenses/opt-in/fetch-metadata/)
attacks.

#### Sec-Fetch-Dest

The `Sec-Fetch-Dest`{.language-plaintext .highlighter-rouge} fetch
metadata request header indicates the request's destination. That is the
initiator of the original fetch request, which is where (and how) the
fetched data will be used.

📋 Possible values are detailed
[here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Dest#directives).

📑 Source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Dest).

#### Sec-Fetch-Mode

The `Sec-Fetch-Mode`{.language-plaintext .highlighter-rouge} fetch
metadata request header indicates the
[mode](https://developer.mozilla.org/en-US/docs/Web/API/Request/mode) of
the request: **cors**, **no-cors**, **same-origin**, **navigate** or
**websocket**.

Broadly speaking, this allows a server to distinguish between: requests
originating from a user navigating between HTML pages, and requests to
load images and other resources.

📋 Possible values are detailed
[here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Mode#directives).

📑 Source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Mode).

#### Sec-Fetch-User

The `Sec-Fetch-User`{.language-plaintext .highlighter-rouge} fetch
metadata request header *is only sent for requests initiated by user
activation*, and its value will always be `?1`{.language-plaintext
.highlighter-rouge}.

📑 Source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-User).

#### Sec-Fetch-Site

The `Sec-Fetch-Site`{.language-plaintext .highlighter-rouge} fetch
metadata request header indicates the relationship between a request
initiator's origin and the origin of the requested resource.

In other words, this header tells a server whether a request for a
resource is coming from the same origin, the same site, a different
site, or is a "user-initiated" request. The server can then use this
information to decide if the request should be allowed.

📋 Possible values are detailed
[here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Site#directives).

📑 Source [Mozilla
MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Site).

💡 Explanation about **Site** vs **Origin** can be found
[here](https://web.dev/same-site-same-origin/).

#### Example {#example-1}

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
GET /www-project-secure-headers/
Host: owasp.org
User-Agent: Chrome/91.0.4472.124
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
```
:::
::::

#### References {#references-1}

- <https://developer.mozilla.org/en-US/docs/Glossary/Fetch_metadata_request_header>
- <https://caniuse.com/mdn-http_headers_sec-fetch-dest>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Dest>
- <https://caniuse.com/mdn-http_headers_sec-fetch-mode>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Mode>
- <https://caniuse.com/mdn-http_headers_sec-fetch-user>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-User>
- <https://caniuse.com/mdn-http_headers_sec-fetch-site>
- <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-Fetch-Site>
- <https://web.dev/same-site-same-origin/>
- <https://jub0bs.com/posts/2021-01-29-great-samesite-confusion/#are-site-and-origin-interchangeable>
- <https://portswigger.net/daily-swig/firefox-becomes-latest-browser-to-support-fetch-metadata-request-headers>
- <https://xsleaks.dev/docs/defenses/opt-in/fetch-metadata/>
:::::::::::

::: {#sec-statistics .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Statistic about HTTP security response headers usage

📅 Last update: 06/05/2025 at 00:16:43 - Domains analyzed count: 150000.

## Global usage of secure headers

Provide the distribution of usage of secure headers across all domains
analyzed.

![be611e71c615c27471d766612bfb7e8b05d743c7](assets/tab_stats_generated_images/be611e71c615c27471d766612bfb7e8b05d743c7.png)

## Global usage of header 'cache-control'

Provide the distribution of usage of the header 'cache-control' across
all domains analyzed.

![577d76c6092c4da6347e1d2c89523dd13a1925f7](assets/tab_stats_generated_images/577d76c6092c4da6347e1d2c89523dd13a1925f7.png)

## Global usage of header 'clear-site-data'

Provide the distribution of usage of the header 'clear-site-data' across
all domains analyzed.

![49f6a7d15e9a2e3fd4cad94360d37e83ef05fa00](assets/tab_stats_generated_images/49f6a7d15e9a2e3fd4cad94360d37e83ef05fa00.png)

## Global usage of header 'content-security-policy'

Provide the distribution of usage of the header
'content-security-policy' across all domains analyzed.

![2da94599d03c73073ac60b0d8864152f8609cc5b](assets/tab_stats_generated_images/2da94599d03c73073ac60b0d8864152f8609cc5b.png)

## Global usage of header 'content-security-policy-report-only'

Provide the distribution of usage of the header
'content-security-policy-report-only' across all domains analyzed.

![c0b5a705e7e94af3f71ef579bb01b45c2a80ca6b](assets/tab_stats_generated_images/c0b5a705e7e94af3f71ef579bb01b45c2a80ca6b.png)

## Global usage of header 'cross-origin-embedder-policy'

Provide the distribution of usage of the header
'cross-origin-embedder-policy' across all domains analyzed.

![0753b0c4fecc8c56d81e31f36bc8c397cea5032b](assets/tab_stats_generated_images/0753b0c4fecc8c56d81e31f36bc8c397cea5032b.png)

## Global usage of header 'cross-origin-opener-policy'

Provide the distribution of usage of the header
'cross-origin-opener-policy' across all domains analyzed.

![e7e550d9cbff786153f7f13f664361e41efee57c](assets/tab_stats_generated_images/e7e550d9cbff786153f7f13f664361e41efee57c.png)

## Global usage of header 'cross-origin-resource-policy'

Provide the distribution of usage of the header
'cross-origin-resource-policy' across all domains analyzed.

![9cf15b18b743939cbe01342ed5461bc7af6c4d36](assets/tab_stats_generated_images/9cf15b18b743939cbe01342ed5461bc7af6c4d36.png)

## Global usage of header 'expect-ct'

Provide the distribution of usage of the header 'expect-ct' across all
domains analyzed.

![78fc7e8d03077546e27c016ee80b2143dc4ebb08](assets/tab_stats_generated_images/78fc7e8d03077546e27c016ee80b2143dc4ebb08.png)

## Global usage of header 'permissions-policy'

Provide the distribution of usage of the header 'permissions-policy'
across all domains analyzed.

![87eabe1fe075f9034dc4db8f76be07da0d08afe3](assets/tab_stats_generated_images/87eabe1fe075f9034dc4db8f76be07da0d08afe3.png)

## Global usage of header 'public-key-pins'

Provide the distribution of usage of the header 'public-key-pins' across
all domains analyzed.

![e58d592c018472a09777c3fd5440f556bd176dd5](assets/tab_stats_generated_images/e58d592c018472a09777c3fd5440f556bd176dd5.png)

## Global usage of header 'referrer-policy'

Provide the distribution of usage of the header 'referrer-policy' across
all domains analyzed.

![15d82f7cac9021b254fdf8fed98bb870acc436fb](assets/tab_stats_generated_images/15d82f7cac9021b254fdf8fed98bb870acc436fb.png)

## Global usage of header 'strict-transport-security'

Provide the distribution of usage of the header
'strict-transport-security' across all domains analyzed.

![c313c0ceef6eb3116547426b41bdf278df2cc0c6](assets/tab_stats_generated_images/c313c0ceef6eb3116547426b41bdf278df2cc0c6.png)

## Global usage of header 'x-content-type-options'

Provide the distribution of usage of the header 'x-content-type-options'
across all domains analyzed.

![5808d16f90388bd6309eb12d74010d1c4a8518cf](assets/tab_stats_generated_images/5808d16f90388bd6309eb12d74010d1c4a8518cf.png)

## Global usage of header 'x-frame-options'

Provide the distribution of usage of the header 'x-frame-options' across
all domains analyzed.

![cfaf56ab8ec6588aa6ee9297b4f93638640d1048](assets/tab_stats_generated_images/cfaf56ab8ec6588aa6ee9297b4f93638640d1048.png)

## Global usage of header 'x-permitted-cross-domain-policies'

Provide the distribution of usage of the header
'x-permitted-cross-domain-policies' across all domains analyzed.

![2ec5e9a684938a169c757a7a631595c53fccc769](assets/tab_stats_generated_images/2ec5e9a684938a169c757a7a631595c53fccc769.png)

## Global usage of header 'x-xss-protection'

Provide the distribution of usage of the header 'x-xss-protection'
across all domains analyzed.

![7b2906800d5eb94d25d0f5cf18322155e8f2192d](assets/tab_stats_generated_images/7b2906800d5eb94d25d0f5cf18322155e8f2192d.png)

## Global usage of insecure framing configuration via the header 'x-frame-options'

Provide the distribution of usage of the header 'x-frame-options' across
all domains analyzed with a insecure framing configuration: value
different from `DENY`{.language-plaintext .highlighter-rouge} or
`SAMEORIGIN`{.language-plaintext .highlighter-rouge} including
unsupported values.

![ccc438a754b6d9324c9c1ea62662969c6114bfdf](assets/tab_stats_generated_images/ccc438a754b6d9324c9c1ea62662969c6114bfdf.png)

## Global usage of insecure referrer configuration via the header 'referrer-policy'

Provide the distribution of usage of the header 'referrer-policy' across
all domains analyzed with a insecure referrer configuration: value set
to `unsafe-url`{.language-plaintext .highlighter-rouge} or
`no-referrer-when-downgrade`{.language-plaintext .highlighter-rouge}.

`no-referrer-when-downgrade`{.language-plaintext .highlighter-rouge} was
included because it send origin, path, and querystring when the protocol
security level stays the same (HTTPS is very often in place).

![e90a8350bb77972b086599b65efc8fcd02036a11](assets/tab_stats_generated_images/e90a8350bb77972b086599b65efc8fcd02036a11.png)

## Global usage of the Strict Transport Security 'preload' feature

Provide the distribution of usage of the
'[preload](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security#preloading_strict_transport_security)'
feature for the header 'strict-transport-security' across all domains
analyzed.

![8dd898e970a4cc540e0394ace9c9cedd425bc1c5](assets/tab_stats_generated_images/8dd898e970a4cc540e0394ace9c9cedd425bc1c5.png)

## Global common 'max-age' values of the Strict Transport Security header

- Most common value used is 31536000 seconds (525600 minutes) across all
  domains analyzed.
- Maximum value used is 447897600000 seconds (7464960000 minutes) across
  all domains analyzed.
- Minimum value used is -299819655 seconds (-4996994 minutes) across all
  domains analyzed.

## Global usage of content security policy with directives allowing unsafe expressions

Provide the distribution of content security policy allowing unsafe
expressions across all domains analyzed.

Determine if a CSP policy contains
`(default-src|script-src|script-src-elem|script-src-attr|style-src)`{.language-plaintext
.highlighter-rouge} directives using
`(unsafe-inline|unsafe-hashes|unsafe-eval)`{.language-plaintext
.highlighter-rouge} expressions.

Based on [Report-URI CSP](https://report-uri.com/home/generate)
generator allowed instructions for CSP directives.

![c7ef83055cf836a48ed9dd26b3a8d55103645022](assets/tab_stats_generated_images/c7ef83055cf836a48ed9dd26b3a8d55103645022.png)
:::

::::::::: {#sec-casestudies .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Case Studies

📋 This section list the entities referencing the [OWASP Secure Headers
Project](index.html).

📩 Feel free to contact project leaders if your company or software
(open source or not) was using the OSHP project.

🔎 **Google dork** used to identity references was
`allintext:"OWASP Secure Headers Project" -site:owasp.org -site:github.com -site:youtube.com -site:twitter.com -site:linkedin.com`{.language-plaintext
.highlighter-rouge}.

## How to create a link to the OSHP site?

🌎 Use the following absolute URL syntax to create a reference link to a
specific location of the OSHP site. The presence of the
`index.html`{.language-plaintext .highlighter-rouge} file is mandatory
otherwise any anchor specified is not effective:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
https://owasp.org/www-project-secure-headers/index.html#[TAB-ID]_[HEADER-ID-INSIDE-TAB]
```
:::
::::

💡 Where:

- `[TAB-ID]`{.language-plaintext .highlighter-rouge}: ID of the tab that
  can be obtained with the link to it.
- `[HEADER-ID-INSIDE-TAB]`{.language-plaintext .highlighter-rouge}: Href
  value of the link to the section inside the tab.

👀 Example of reference link to the section about the header
**Clear-Site-Data** in the **Response Headers** tab:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
https://owasp.org/www-project-secure-headers/index.html#div-headers_clear-site-data
```
:::
::::

👀 Example of reference link to the section **PHP** in the **Technical
Resources** tab:

:::: {.language-text .highlighter-rouge}
::: highlight
``` highlight
https://owasp.org/www-project-secure-headers/index.html#div-technical_php
```
:::
::::

## Companies and other legal entities

- [Cloud.gov](https://cloud.gov/docs/management/headers/).
- [Salesforce](https://help.salesforce.com/s/articleView?language=en_US&id=cc.b2c_declarative_security_via_http_headers.htm&type=5).
- [Black Hills Information
  Security](https://www.blackhillsinfosec.com/fixing-content-security-policies-with-cloudflare-workers/).
- [Progress](https://www.progress.com/documentation/sitefinity-cms/110/predefined-security-headers-in-http-response).
- [Bloomreach](https://documentation.bloomreach.com/14/library/concepts/security/configure-security-response-headers.html).
- [Tableau](https://help.tableau.com/current/server-linux/en-us/security_http_headers.htm).
- [42Crunch](https://docs.42crunch.com/latest/content/extras/protection_security_headers.htm).
- [SAP](https://help.sap.com/docs/SAP_UPSCALE_COMMERCE/4620dd88ff9047c89ffb7fa897207a46/30af09ca9e394505a85661fa530d1263.html).
- [SecureAuth](https://docs.secureauth.com/2104/en/identity-platform-http-security-header-best-practices.html).
- [Detectify](https://support.detectify.com/support/solutions/articles/48001048949-https-stripping).
- [ImmuniWeb](https://www.immuniweb.com/websec/about).
- [Zoom](https://developers.zoom.us/docs/zoom-apps/security/owasp/).
- [NexusGuard](https://blog.nexusguard.com/hardening-web-applications-using-secure-http-headers).
- [VeraCode](https://docs.veracode.com/r/enable-security-headers).
- [Ivanti](https://forums.ivanti.com/s/article/HTTP-Security-Headers-X-Frame-Options-X-XSS-Protection-X-Content-Type-Options).
- [Government Technology Agency of Singapore
  GovTech](https://info.standards.tech.gov.sg/control-catalog/as/).
- [HCL Volt
  MX](https://opensource.hcltechsw.com/volt-mx-docs/docs/documentation/Foundry/voltmx_Foundry_deployment_guide/Content/Hardening_Guide.html).
- [Missouri State
  Website](https://assets.mo.gov/samples/security/security-headers.html).
- [SAS](https://documentation.sas.com/doc/en/sasadmincdc/v_054/viyaov/p0i3vcgjpciz45n1of1v4vkffwbn.htm).
- [RedHat](https://www.redhat.com/en/blog/creating-web-application-firewall-red-hat-openshift).
- [Sages](https://www.sages.io/blog/headlines-safety-review-actual-recommendations).

## Software

- [Nmap](https://github.com/nmap/nmap/blob/master/scripts/http-security-headers.nse).
- [Spring
  Security](https://docs.spring.io/spring-security/reference/features/exploits/headers.html).
:::::::::

::: {#sec-logo .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Official project logo

🤝 OWASP Secure Headers Project logos are free to use. All files are
licensed under the [Apache 2.0
Licenses](https://www.apache.org/licenses/LICENSE-2.0).

📦 A mirror of all the logo files are also stored into the [OWASP
Swag](https://github.com/OWASP/owasp-swag/tree/master/projects/secure-headers-project)
GitHub repository.

## Mantra

💬 The official project mantra is
`Defense in depth as a credo`{.language-plaintext .highlighter-rouge}.

## Set 1

📐 Designed by
**[weperfectionist](https://www.fiverr.com/weperfectionist)** using
`Adobe Illustrator`{.language-plaintext .highlighter-rouge}.

🧾 Source files are **[logo-source.ai](logo/logo-source.ps)** and
**[logo-source.eps](logo/logo-source-2.ps)**.

📦 Different flavors are available.

🎨 Transparent background ([PNG](https://en.wikipedia.org/wiki/PNG)
format):

- [Black foreground](logo/logo-black-on-transparent.png).
- [Blue foreground](logo/logo-blue-on-transparent.png).
- [White foreground](logo/logo-white-on-transparent.png).

🎨 Non-transparent background
([JPEG](https://en.wikipedia.org/wiki/JPEG) format):

- [Black foreground on white background](logo/logo-black-on-white.jpg).
- [Blue foreground on white background](logo/logo-blue-on-white.jpg).
- [White foreground on black background](logo/logo-white-on-black.jpg).

📝 The file [logo-all.pdf](logo/logo-all.pdf) gathers the three
non-transparent logo.

## Set 2

📦 The folder
[generated-via-ai](https://github.com/OWASP/www-project-secure-headers/tree/master/logo/generated-via-ai)
contains several base images that were generated via the following AI
systems:

- [ChatGPT](https://chatgpt.com/).
- [Microsoft Copilot](https://copilot.microsoft.com/).

🎨 To be transparent about its source, each image include the name of
the AI systems used in its filename. They were all edited with
[Paint.net](https://www.getpaint.net/) and saved into the
[PNG](https://en.wikipedia.org/wiki/PNG) format:

- [logo01-chatgpt](logo/generated-via-ai/logo01-chatgpt.png).
- [logo02-microsoft-copilot](logo/generated-via-ai/logo02-microsoft-copilot.png).
- [logo03-microsoft-copilot](logo/generated-via-ai/logo03-microsoft-copilot.png).
- [logo04-microsoft-copilot](logo/generated-via-ai/logo04-microsoft-copilot.png).
- [logo05-microsoft-copilot](logo/generated-via-ai/logo05-microsoft-copilot.png).
- [logo06-microsoft-copilot](logo/generated-via-ai/logo06-microsoft-copilot.png).
- [logo07-chatgpt](logo/generated-via-ai/logo07-chatgpt.png).
- [logo08-microsoft-copilot](logo/generated-via-ai/logo08-microsoft-copilot.png).
- [logo09-microsoft-copilot](logo/generated-via-ai/logo09-microsoft-copilot.png).
:::
:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-secure-headers/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-secure-headers){.github-button
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

### Project Information

-  [Production project]{style="font-size: 1.3em;"}

#### Classification

-  Documentation

#### Audience

-  Builder
-  Defender

### Project GitHub Organization

- 💻 [OSHP](https://github.com/oshp/)

### Notification

- 🌏 We use the hashtag `owasp_shp`{.language-plaintext
  .highlighter-rouge} in our posts on
  [Bluesky](https://bsky.app/hashtag/owasp_shp) and
  [LinkedIn](https://www.linkedin.com/feed/hashtag/?keywords=owasp_shp),
  to publish an update about the project.
- 📡 This [atom web
  feed](https://github.com/OWASP/www-project-secure-headers/commits/master.atom)
  can be used to be notified when an update is pushed on the OSHP
  website's repository.

### Leaders

- [Ricardo
  Iramar](../cdn-cgi/l/email-protection.html#b5c7dcd6d4c7d1da9bdcc7d4d8d4c7f5dac2d4c6c59bdac7d2)
- [Dominique
  Righetto](../cdn-cgi/l/email-protection.html#90f4fffdf9fef9e1e5f5bee2f9f7f8f5e4e4ffd0ffe7f1e3e0beffe2f7)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
