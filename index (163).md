:::::::::::::::::::::::::::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Features](#div-features){#features-link .tab-link role="tab"
  aria-selected="false" aria-controls="features"}
- [Screenshots](#div-screenshots){#screenshots-link .tab-link role="tab"
  aria-selected="false" aria-controls="screenshots"}
- [Our Supporters](#div-supporters){#supporters-link .tab-link
  role="tab" aria-selected="false" aria-controls="supporters"}

# OWASP CSRFGuard {#owasp-csrfguard .page-title}

::::::::::::::::::::::::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::::::::::::::::::::::::::::::::: {#sec-main .section .page-body}
![Tool Project](assets/images/owasp_tool_project.png)

# CSRFGuard 4 Token Injection

## Index

1.  [Overview](#overview)
2.  [JavaScript DOM Manipulation](#javascript-dom-manipulation)\
    2.1 [Declare and Configure
    JavaScriptServlet](#declare-and-configure-javascriptservlet)\
    2.2 [Map JavaScriptServlet](#map-javascriptservlet)\
    2.3 [Inject Dynamic JavaScript](#inject-dynamic-javascript)
3.  [JSP Tag Library](#jsp-tag-library)\
    3.1 [Display Token Name](#display-token-name)\
    3.2 [Display Token Value](#display-token-value)\
    3.3 [Display Token Name Value Pair](#display-token-name-value-pair)\
    3.4 [Generate Form with Prevention
    Token](#generate-form-with-prevention-token)\
    3.5 [Generate Link with Prevention
    Token](#generate-link-with-prevention-token)

## Overview

OWASP CSRFGuard implements a variant of the synchronizer token pattern
to mitigate the risk of CSRF attacks. In order to implement this
pattern, CSRFGuard must offer the capability to place the CSRF
prevention token within the HTML produced by the protected web
application. CSRFGuard provides developers more fine grain control over
the injection of the token. Developers can inject the token in their
HTML using either dynamic JavaScript DOM manipulation or a JSP tag
library. The currently available token injection strategies are designed
to make the integration of CSRFGuard more feasible and scalable within
current enterprise web applications. Developers are encouraged to make
use of both the JavaScript DOM Manipulation and the JSP tag library
strategies for a complete token injection strategy. The JavaScript DOM
Manipulation strategy is ideal as it is automated and requires minimal
effort on behalf of the developer. In the event the JavaScript solution
is insufficient within a particular application context, developers
should leverage the JSP tag library. The purpose of this article is to
describe the token injection strategies offered by OWASP CSRFGuard.

The OWASP CSRFGuard library is integrated through the use of a JavaEE
Filter and exposes various automated and manual ways to integrate
per-session or pseudo-per-request tokens into HTML. When a user
interacts with this HTML, CSRF prevention tokens (i.e. cryptographically
random synchronizer tokens) are submitted with the corresponding HTTP
request.

It is the responsibility of OWASP CSRFGuard to ensure the token is
present and is valid for the current HTTP request.

Any attempt to submit a request to a protected resource without the
correct corresponding token is viewed as a CSRF attack in progress and
is discarded. Prior to discarding the request, CSRFGuard can be
configured to take one or more actions such as logging aspects of the
request and redirecting the user to a landing page. The latest release
enhances this strategy to support the optional verification of HTTP
requests submitted using Ajax as well as the optional verification of
referrer headers.

As OWASP project we follow the OWASP Code Of Conduct available here:
https://owasp.org/www-policy/operational/code-of-conduct

## JavaScript DOM Manipulation

OWASP CSRFGuard supports the ability to dynamically inject CSRF
prevention tokens throughout the DOM currently loaded in the user's
browser. This strategy is extremely valuable with regards to server-side
performance as it simply requires the serving of a dynamic JavaScript
file. There is little to no performance hit when the fetched dynamic
JavaScript updates the browser's DOM. Making use of the JavaScript token
injection solution requires the developer map a Servlet and place a
JavaScript HTML tag within all pages sending requests to protected
application resources. Developers are strongly encouraged to leverage
the JavaScript token injection strategy by default. This strategy
requires minimal effort on behalf of the developer as most of the token
injection logic is automated. In the event that the JavaScript automated
solution may be insufficient for a specific application context,
developers should leverage the OWASP CSRFGuard JSP tag library. \\

**Note**: Use of JavaScript DOM Manipulation is required for Ajax
support.

### Declare and Configure JavaScriptServlet

The JavaScript file used for token injection is dynamically generated by
the JavaScriptServlet class using a template file. Ensure that the
Owasp.CsrfGuard.jar file is found within the target application's
classpath. Copy the Owasp.CsrfGuard.js template file from the OWASP
CSRFGuard distribution folder to a non-publicly accessible directory
within the target application. For the remainder of this section, we
assume the Owasp.CsrfGuard.js template file was placed in the
application's WEB-INF folder. Edit the deployment descriptor (web.xml)
to declare the JavaScriptServlet class along with any associated
initialization parameters. Consider the following configuration snippet
taken from the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<servlet>
     <servlet-name>JavaScriptServlet</servlet-name>
     <servlet-class>org.owasp.csrfguard.servlet.JavaScriptServlet</servlet-class>
     <init-param>
         <param-name>source-file</param-name>
         <param-value>WEB-INF/Owasp.CsrfGuard.js</param-value>
     </init-param>
     <init-param>
         <param-name>inject-into-forms</param-name>
         <param-value>true</param-value>
     </init-param>
     <init-param>
         <param-name>inject-into-attributes</param-name>
         <param-value>true</param-value>
     </init-param>
    <init-param>
         <param-name>domain-strict</param-name>
         <param-value>false</param-value>
    </init-param>
    <init-param>
         <param-name>referer-pattern</param-name>
         <param-value>.*localhost.*</param-value>
    </init-param>
</servlet>
```
:::
::::

The aforementioned configuration snippet declares the JavaScriptServlet
class using the name "JavaScriptServlet". JavaScriptServlet accepts
various initialization parameters augmenting the behavior of the class
at runtime. The provided configuration snippet instructs
JavaScriptServlet to...

1.  Leverage the template JavaScript file at WEB-INF/Owasp.CsrfGuard.js
2.  Inject the token into all HTML forms
3.  Inject the token into all src and href attributes
4.  Leverage loose same origin matching criteria when placing the token
    in URL resources

Consider the following for a more detailed listing of the initialization
parameters supported by JavaScriptServlet:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
source-file
```
:::
::::

Denotes the location of the JavaScript template file that should be
consumed and dynamically augmented by the JavaScriptServlet class. The
default value is WEB-INF/Owasp.CsrfGuard.js. Use of this property and
the existence of the specified template file is required.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
domain-strict
```
:::
::::

Boolean value that determines whether or not the dynamic JavaScript code
should be strict with regards to what links it should inject the CSRF
prevention token. With a value of true, the JavaScript code will only
place the token in links that point to the same exact domain from which
the HTML originated. With a value of false, the JavaScript code will
place the token in links that not only point to the same exact domain
from which the HTML originated, but sub-domains as well.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
referer-pattern
```
:::
::::

Allows the developer to specify a regular expression describing the
required value of the Referer header. Any attempts to access the servlet
with a Referer header that does not match the captured expression is
discarded. Inclusion of referer header checking is to help minimize the
risk of JavaScript Hijacking attacks that attempt to steal tokens from
the dynamically generated JavaScript. While the primary defenses against
JavaScript Hijacking attacks are implemented within the dynamic
JavaScript itself, referer header checking is implemented to achieve
defense in depth.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
cache-control
```
:::
::::

Allows the developer to specify the value of the Cache-Control header in
the HTTP response when serving the dynamic JavaScript file. The default
value is private, maxage=28800. Caching of the dynamic JavaScript file
is intended to minimize traffic and improve performance. Note that the
Cache-Control header is always set to "no-store" when either the
"Rotate" "TokenPerPage" options is set to true in
Owasp.CsrfGuard.properties.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
inject-into-forms
```
:::
::::

Boolean value that determines whether or not the dynamic JavaScript code
should inject the CSRF prevention token as a hidden field into HTML
forms. The default value is true. Developers are strongly discouraged
from disabling this property as most server-side state changing actions
are triggered via a POST request.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
inject-into-attributes
```
:::
::::

Boolean value that determines whether or not the dynamic JavaScript code
should inject the CSRF prevention token in the query string of src and
href attributes. Injecting the CSRF prevention token in a URL resource
increases its general risk of exposure to unauthorized parties. However,
most JavaEE web applications respond in the exact same manner to HTTP
requests and their associated parameters regardless of the HTTP method.
The risk associated with not protecting GET requests in this situation
is perceived greater than the risk of exposing the token in protected
GET requests. As a result, the default value of this attribute is set to
true. Developers that are confident their server-side state changing
controllers will only respond to POST requests (i.e. discarding GET
requests) are strongly encouraged to disable this property.

### Map JavaScriptServlet

Developers must map the JavaScriptServlet to a URI space such that the
Servlet class can be remotely accessed by the dynamic JavaScript code.
Consider the following configuration snippet taken directly from the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<servlet-mapping>
     <servlet-name>JavaScriptServlet</servlet-name>
     <url-pattern>/JavaScriptServlet</url-pattern>
</servlet-mapping>
```
:::
::::

The aforementioned configuration snippet maps the Servlet referenced by
the name "JavaScriptServlet" to the URI space "/JavaScriptServlet". Any
request sent to the /JavaScriptServlet URI will produce a dynamically
generated CSRFGuard JavaScript file specific to the user's current
session.

### Inject Dynamic JavaScript

Developers are required to place an HTML script tag within all pages
that are known to send requests to CSRF protected resources. All
requests within the current HTML page are augmented to ensure they
submit the correct CSRF token for the user's current session. Note that
inclusion of the dynamic JavaScript does not protect the current page.
Rather, the script ensures the CSRF token is transmitted within all
requests generated by the current page. Consider the following code
snippet taken directly from the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<script src="/Owasp.CsrfGuard.Test/JavaScriptServlet"></script>
```
:::
::::

The script tag retrieves and executes the dynamically generated
JavaScript from the Servlet mapped at
/Owasp.CsrfGuard.Test/JavaScriptServlet. This JavaScript code will
register an event handler with window.onload. Once triggered, the code
will iterate over every HTML element within the DOM looking for either
form tags and or tags containing href or src attributes as configured by
the JavaScriptServlet initialization parameters. Forms are dynamically
updated to include the CSRFGuard token via a hidden field and tags using
src and href attributes are updated to include the CSRFGuard token via a
query string parameter.

## JSP Tag Library

OWASP CSRFGuard exposes a JSP tag library providing developers more fine
grain control over token injection. The library exposes JSP tags that
allow access to the token name, the token value, and the token name
value pair delimited by an equals (=) sign. In order to make use of the
tag library, ensure the Owasp.CsrfGuard.jar file is found within the
target application's classpath. For example, the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application places the OWASP CSRFGuard jar file within the
WebContent/WEB-INF/lib directory. After placing the library in the
classpath, developers can reference the tags in JSP pages using
predefined URI reference. The following JSP code snippet imports the tag
library and makes it available using the prefix "csrf":

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<%@ taglib uri="http://www.owasp.org/index.php/Category:OWASP_CSRFGuard_Project/Owasp.CsrfGuard.tld" prefix="csrf" %>
```
:::
::::

The benefit of using the JSP tag library to inject the CSRF prevention
token is the fine grain level of control. Developers can place the token
in all the correct locations within the context of their applications.
This strategy is useful in application contexts where the JavaScript DOM
Manipulation strategy is insufficient.

### Display Token Name

The OWASP CSRFGuard token name can be obtained through the token-name
tag. The token-name tag is useful when injecting the CSRFGuard token
name in a non-query string context. Consider the following code snippet
taken from the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application. This code makes use of the token-name tag to reference the
token name in the name attribute of a hidden input field:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<form name="test1" action="protect.html">
     <input type="text" name="text" value="text"/>
     <input type="submit" name="submit" value="submit"/>
     <input type="hidden" name="<csrf:tokenname/>" value="<csrf:tokenvalue uri="protect.html"/>"/>
</form>
```
:::
::::

### Display Token Value

The OWASP CSRFGuard token value can be obtained through the token-value
tag. The token-value tag is useful when injecting the CSRFGuard token
value in a non-query string context. Consider the following code snippet
taken from the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application. This code makes use of the token-value tag to reference the
token value in the value attribute of a hidden input field:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<form name="test1" action="protect.html">
     <input type="text" name="text" value="text"/>
     <input type="submit" name="submit" value="submit"/>
     <input type="hidden" name="<csrf:tokenname/>" value="<csrf:tokenvalue/>"/>
</form>
```
:::
::::

The token value tag must be used in conjunction with the URI attribute
when using the unique token per page model
(org.owasp.csrfguard.TokenPerPage). The value of the uri attribute is
the URI for which the token value will be posted. Consider the following
example which sets the URI to the destination of the form,
"protect.html":

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<form id="formTest1" name="formTest1" action="protect.html">
     <input type="text" name="text" value="text"/>
     <input type="submit" name="submit" value="submit"/>
     <input type="hidden" name="<csrf:tokenname/>" value="<csrf:tokenvalue uri="protect.html"/>"/>
</form>
```
:::
::::

### Display Token Name Value Pair

The OWASP CSRFGuard token name value pair, delimited by an equals sign
(=), can be obtained though the token tag. The token tag is useful when
injecting the CSRFGuard token value in a query string context. Consider
the following code snippet taken from the
[Owasp.CsrfGuard.Test](https://github.com/OWASP/www-project-csrfguard/tree/master/csrfguard-test/csrfguard-test-jsp/src/main/webapp/WEB-INF/classes)
application. This code makes use of the token tag to reference the token
name value pair in the href attribute of an anchor tag:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<a href="protect.html?<csrf:token/>">protect.html</a>
```
:::
::::

The token name value pair tag must be used in conjunction with the URI
attribute when using the unique token per page model
(org.owasp.csrfguard.TokenPerPage). The value of the uri attribute is
the URI for which the token value will be posted. Consider the following
example which sets the URI to the destination of the link,
"protect.html":

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<a href="protect.html?<csrf:token uri="protect.html"/>">protect.html</a>
```
:::
::::

### Generate Form with Prevention Token

The OWASP CSRFGuard JSP library implements a tag library designed
specifically to generate HTML forms with the CSRF prevention token
automatically embedded as a hidden field. This strategy simplifies the
integration of the CSRF token, especially when using the unique token
per page model (org.owasp.csrfguard.TokenPerPage). The tag accepts
dynamic attribute name value pairs and simply outputs them to the page.
As a result, you are free to use the same attribute values made
available in a standard HTML form. There is no special output encoding
performed on these dynamic attributes. Take care to perform the
appropriate validation and output encoding for all dynamic attributes
used in conjunction with untrusted data. Consider the following code
snippet which will produce a HTML form with an embedded CSRF token. No
special care must be taken when using this flag in conjunction with the
unique token per uri model:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<csrf:form id="formTest2" name="formTest2" action="protect.html">
     <input type="text" name="text" value="text"/>
     <input type="submit" name="submit" value="submit"/>
</csrf:form>
```
:::
::::

### Generate Link with Prevention Token

The OWASP CSRFGuard JSP library implements a tag library designed
specifically to generate HTML anchor tags with the CSRF prevention token
automatically embedded as a query string parameter. This strategy
simplifies the integration of the CSRF token, especially when using the
unique token per page model (org.owasp.csrfguard.TokenPerPage). The tag
accepts dynamic attribute name value pairs and simply outputs them to
the page. As a result, you are free to use the same attribute values
made available in a standard HTML anchor. There is no special output
encoding performed on these dynamic attributes. Take care to perform the
appropriate validation and output encoding for all dynamic attributes
used in conjunction with untrusted data. Consider the following code
snippet which will produce a HTML anchor tag with an embedded CSRF
token. No special care must be taken when using this flag in conjunction
with the unique token per uri model:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
<csrf:a href="protect.html">protect.html</csrf:a>
```
:::
::::
:::::::::::::::::::::::::::::::::::::

::: {#sec-features .section .page-body .tab-hidden}

------------------------------------------------------------------------

# OWASP CSRFGuard 4.0.0 {#owasp-csrfguard-400}

![OWASP CSRFGuard 4.0.0](assets/images/csrfguard.png)

## What are CSRF (Cross-Site Request Forgery) Attacks?

![How Does CSRF Work](assets/images/what_is_csrf_attacks_1.png) ![How
Does CSRF Work](assets/images/what_is_csrf_attacks_2.png) ![How Does
CSRF Work](assets/images/what_is_csrf_attacks_3.png) ![How Does CSRF
Work](assets/images/what_is_csrf_attacks_4.png) ![How Does CSRF
Work](assets/images/what_is_csrf_attacks_5.png) ![How Does CSRF
Work](assets/images/what_is_csrf_attacks_6.png) ![How Does CSRF
Work](assets/images/what_is_csrf_attacks_7.png)
:::

::: {#sec-screenshots .section .page-body .tab-hidden}

------------------------------------------------------------------------

# CSRFGuard In Action

![CSRFGuard in action](assets/images/csrfguard_in_action.png)
:::

::: {#sec-supporters .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Supporters

CSRFGuard is developed by a worldwide of volunteers in Morocco, France,
India, China, Singapore, Indonesia, Canada and more.

## Special Thanks

Thanks to Trent Schmidt and Joel Orlina (JIRA) for there help.
:::
:::::::::::::::::::::::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-csrfguard/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-csrfguard){.github-button
icon="octicon-star" data-size="large" show-count="true"
aria-label="Star on GitHub"}
:::

:::::::: {.sidebar role="complementary"}
::: owasp-sidebar-top
**The OWASP^®^ Foundation** works to improve the security of software
through its community-led open source software projects, hundreds of
chapters worldwide, tens of thousands of members, and by hosting local
and global conferences.
:::

### Project Classification

![Flagship Project](assets/images/mature_projects.png)

![Builders](assets/images/owasp_builders_small.png)
![Breakers](assets/images/owasp_breakers_small.png)

![Tool Project](assets/images/owasp_tool_project.png)

## CSRFGuard 4.0 released in April 2021 {#csrfguard-40-released-in-april-2021}

[https://owasp.org/www-project-csrfguard/](index.html)

BSD License, All rights reserved.

## Overview {#overview}

Welcome to the home of the OWASP CSRFGuard Project! OWASP CSRFGuard is a
library that implements a variant of the synchronizer token pattern to
mitigate the risk of Cross-Site Request Forgery (CSRF) attacks. The
OWASP CSRFGuard library is integrated through the use of a JavaEE Filter
and exposes various automated and manual ways to integrate per-session
or pseudo-per-request tokens into HTML. When a user interacts with this
HTML, CSRF prevention tokens (i.e. cryptographically random synchronizer
tokens) are submitted with the corresponding HTTP request. It is the
responsibility of OWASP CSRFGuard to ensure the token is present and is
valid for the current HTTP request. Any attempt to submit a request to a
protected resource without the correct corresponding token is viewed as
a CSRF attack in progress and is discarded. Prior to discarding the
request, CSRFGuard can be configured to take one or more actions such as
logging aspects of the request and redirecting the user to a landing
page. The latest release enhances this strategy to support the optional
verification of HTTP requests submitted using Ajax as well as the
optional verification of referrer headers.

## Project Leads

The CSRFGuard project is run by [Azzeddine
RAMRAMI](../cdn-cgi/l/email-protection.html#690813130c0d0d00070c471b08041b08040029061e081a1947061b0e)
and [Istvan
ALBERT-TOTH](../cdn-cgi/l/email-protection.html#9df4eee9ebfcf3b3fcf1fff8efe9e9f2e9f5ddf2eafceeedb3f2effa).

## License

OWASP CSRFGuard 4.x is offered under the [BSD
license](http://www.opensource.org/licenses/bsd-license.php).

## Using with Maven

Add the following dependencies to your Maven POM file to use the
library:\
**Note**: for the
[Jakarta](https://github.com/OWASP/www-project-csrfguard/tree/jakarta)
releases use the `-jakarta`{.language-plaintext .highlighter-rouge}
suffix in the `version`{.language-plaintext .highlighter-rouge}.

:::: {.language-xml .highlighter-rouge}
::: highlight
``` highlight
<dependency>
    <groupId>org.owasp</groupId>
    <artifactId>csrfguard</artifactId>
    <version>4.4.0</version>
</dependency>

<!-- Stateful web application support -->
<dependency>
    <groupId>org.owasp</groupId>
    <artifactId>csrfguard-extension-session</artifactId>
    <version>4.4.0</version>
</dependency>

<!-- JSP TAG support -->
<dependency>
    <groupId>org.owasp</groupId>
    <artifactId>csrfguard-jsp-tags</artifactId>
    <version>4.4.0</version>
</dependency>
```
:::
::::

## Building the code

1.  Make sure you have [Apache Maven](http://maven.apache.org/) 3.6.3+
    and JDK 11+ installed
2.  Clone this repository locally
3.  Build the project by running `mvn clean install`{.language-plaintext
    .highlighter-rouge} in the project root directory
4.  Build and run the test JSP web application by running
    `mvn pre-integration-test -Pdeploy-jsp-webapp -pl csrfguard-test/csrfguard-test-jsp`{.language-plaintext
    .highlighter-rouge} or
    `mvn -Pdeploy-jsp-webapp -pl csrfguard-test/csrfguard-test-jsp tomcat7:run`{.language-plaintext
    .highlighter-rouge}
5.  Optional: you can use `mvnDebug`{.language-plaintext
    .highlighter-rouge} to enable remote debugging, then connect your
    IDE to it (default port is 8000)
6.  Use a web browser to access
    `http://localhost:8080`{.language-plaintext .highlighter-rouge} to
    open the home page of the test project

## Uploading to the Maven Central repository

1.  Follow the [Sonatype Open-Source Project Maven Repository Usage
    Guide](https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide)
    to create a Sonatype user account;
2.  Next, [open a support
    request](https://issues.sonatype.org/browse/OSSRH) to get your newly
    created username added to the Maven groupId
    `org.owasp`{.language-plaintext .highlighter-rouge};
3.  Once the support request has been completed, follow the instructions
    in the Sonatype Maven repository usage guide mentioned above to
    upload new versions to the Maven Central repository.

### Maven Central repository

You can download pre-compiled versions from:

- [Maven Central
  repository](https://search.maven.org/search?q=csrfguard)
- [OSS Sonatype Nexus
  repository](https://oss.sonatype.org/#nexus-search;gav~~csrfguard~~~)

## Discussions and Email list

If you have questions, would like to share or discuss ideas, please use
the official [discussions
page](https://github.com/OWASP/www-project-csrfguard/discussions)
(**preferred**). You can also sign up for the OWASP CSRFGuard email list
[here](https://groups.google.com/a/owasp.org/g/csrfguard-project).

## CSRFGuard 4.0 Release Notes: {#csrfguard-40-release-notes}

- [Support for stateless web
  applications](https://github.com/OWASP/www-project-csrfguard/issues/4)
- [Apply "TokenPerPage" approach to
  AJAX](https://github.com/OWASP/www-project-csrfguard/issues/2)
- [Reduced code
  duplication](https://github.com/aramrami/OWASP-CSRFGuard/issues/127)
- [Proper multi-module maven project
  structure](https://github.com/aramrami/OWASP-CSRFGuard/issues/128)
- [The test JSP web application now relies on the latest development
  JavaScript
  code](https://github.com/aramrami/OWASP-CSRFGuard/issues/133)
- [Improved code
  quality](https://github.com/aramrami/OWASP-CSRFGuard/issues/134)
- [Addressing synchronous XMLHttpRequest
  deprecation](https://github.com/aramrami/OWASP-CSRFGuard/issues/137)
- [Approach changed for master and page token
  retrieval](https://github.com/aramrami/OWASP-CSRFGuard/issues/139)
- [Improved test
  coverage](https://github.com/aramrami/OWASP-CSRFGuard/issues/140)
- [Better solution for looking up page tokens in the
  JS](https://github.com/aramrami/OWASP-CSRFGuard/issues/141)
- [The javascript template is now parsable and
  minifiable](https://github.com/aramrami/OWASP-CSRFGuard/issues/142)
- [Short-circuit the solution logic if CSRFGuard is
  disabled](https://github.com/aramrami/OWASP-CSRFGuard/issues/143)
- [Do not generate page tokens for pages that are not
  protected](https://github.com/aramrami/OWASP-CSRFGuard/issues/144)
- [Page tokens generated on first use are not sent back to the
  client](https://github.com/aramrami/OWASP-CSRFGuard/issues/145)
- [Issue with the token-per-page support for REST endpoint containing
  path
  parameters](https://github.com/aramrami/OWASP-CSRFGuard/issues/146)
- [Possible race condition on first access of endpoints when
  token-per-page and AJAX request options are
  enabled](https://github.com/aramrami/OWASP-CSRFGuard/issues/147)
- [Tokens are not injected into dynamically created DOM
  elements](https://github.com/aramrami/OWASP-CSRFGuard/issues/148)
- [Make the configuration more resilient to
  errors](https://github.com/aramrami/OWASP-CSRFGuard/issues/149)
- [Tokens should not be injected into external links if the domainStrict
  property is set to
  true](https://github.com/aramrami/OWASP-CSRFGuard/issues/150)
- [Tokens not injected in dynamic content returned from
  Ajax](https://github.com/aramrami/OWASP-CSRFGuard/issues/151)
- Heavily refactored, improved and more optimized code-base
- Documentation update and typo fixes.
- Copyright update and unification.

### Leaders

- [Azzeddine
  RAMRAMI](../cdn-cgi/l/email-protection.html#89e8f3f3ecedede0e7eca7fbe8e4fbe8e4e0c9e6fee8faf9a7e6fbee)
- [Istvan
  Albert-Toth](../cdn-cgi/l/email-protection.html#3e574d4a485f50105f525c5b4c4a4a514a567e51495f4d4e10514c59)
- [Sébastien
  Gioria](../cdn-cgi/l/email-protection.html#cebdabacafbdbaa7aba0e0a9a7a1bca7af8ea1b9afbdbee0a1bca9)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::::
::::::::::::::::::::::::::::::::::::::::::::::::::
