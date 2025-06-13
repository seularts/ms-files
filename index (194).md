::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Concepts](#div-concepts){#concepts-link .tab-link role="tab"
  aria-selected="false" aria-controls="concepts"}
- [Detection_Points](#div-detection_points){#detection_points-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="detection_points"}
- [Response_Actions](#div-response_actions){#response_actions-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="response_actions"}

# OWASP AppSensor {#owasp-appsensor .page-title}

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# AppSensor

The AppSensor project defines a conceptual framework and methodology
that offers prescriptive guidance to implement application layer
intrusion detection and automated response. In addition, there is a
reference implementation that provides a toolkit for building
self-defending applications through real-time event detection and
response [appsensor github](https://github.com/jtmelton/appsensor).

The book describing the framework and methodology are available via
[PDF](https://ubiquitous-adventure-gnwnz4m.pages.github.io/Owasp-appsensor-guide-v2.pdf)
or as a physical book on
[Lulu](https://www.lulu.com/en/us/shop/owasp-foundation/appsensor-guide/paperback/product-1v92q7d8.html?page=1&pageSize=4)

There is more detailed information about the concepts as well as a
getting started set of docs for developers at
[appsensor.org](http://www.appsensor.org/)
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::

::: {#sec-concepts .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Concepts

# Application Layer Intrusion Detection

Today's applications are responsible for securely performing critical
operations for individuals and businesses around the world. From
transferring money, to managing health records, web enabled applications
handle immense amounts of sensitive data each day. Despite the critical
role they play, the security defenses within these applications are
seriously lacking. The attackers are organized, motivated, and backed by
a network of resources and talent. If our applications have any hope of
standing up to such formidable opponents, then we need to move beyond
just attempting to design our applications securely. We need to
implement robust attack detection within the application to identify
malicious users before they are successful in their attack. Just like in
the real world, we would prefer to detect and prevent an attack instead
of just responding after a compromise has occurred.

How do we bridge the technology gap to implement appropriate security
controls in our critical applications? The first step is to realize that
in order to detect and respond to malicious activity at the application
layer we need to be able to monitor and understand a user's actions
within the application. Security approaches of previous years are not
sufficient. A firewall provides no protection; its purpose is to allow
users to access the application. Nor does a network based IDS system
since it will have no insight to our application specific traffic.
Antivirus is also out of the question since this is a signature based
approach that knows nothing of custom web application vulnerabilities.

We need to move into the application layer to understand our attackers.
One potential solution is a web application firewall (WAF). A WAF is
able to detect generic application attacks such as basic SQL injection
attacks or common actions of a known attack sequence. While some
detection is better than none, a generic product could never fully
understand the intricacies of each custom web application. This approach
is just not sufficient to properly protect critical applications that
process sensitive financial data or personal user information. Imagine
trying to design an effective building alarm system without any
knowledge of how the building is designed or even where the doors and
windows are located.

The solution is to design and integrate a detection and response system
into the application itself. Within the application we have a full
understanding of the user initiating an action, the target of that
action and whether that action should be allowed for that user. Inside
the application our protection system can identify advanced attacks that
are attempting to exploit specific features of our application. Within
the application we can easily identify attempts to circumvent security
controls or use the application in an unintended manner. After we have
determined that a particular user has malicious intent and is attempting
to identify weaknesses in our system, we can immediately respond and
block the user from future access to the application, or take whatever
other action is appropriate. Once locked out, such users can no longer
login and are limited to attacking the perimeter of an application,
which often contains limited functionality and is typically well
secured. Alternatively, some organizations may wish to forego an
automated lockout response and instead generate an attack alert and
allow their security-monitoring center to perform an immediate
investigation and decide upon the appropriate response.

The rigor of response is a decision for each organization in relation to
their tolerance for risk and specific needs for an application. However,
it is clear that this level of detection capability is a must for any
organization wishing to prevent skilled and persistent attackers from
compromising their critical applications.

OWASP AppSensor

OWASP is committed to the protection of applications through application
attack detection and automated response. The OWASP AppSensor project has
been established in response to the clear need for guidance and
knowledge in this area.

AppSensor provides the following:

- Recommendations for what application actions should be detected as
  malicious along with suggested responses
- Guidance on designing and implementing an attack detection and
  response system within an application
- A Java reference implementation that you can integrate into your
  application as the basis for your Application Layer Intrusion
  Detection and Response mechanism
:::

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: {#sec-detection_points .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Detection Points

# About This Document

These detection points are part of the [OWASP
AppSensor](http://www.owasp.org/index.php/Category:OWASP_AppSensor_Project)
project which advocates bringing intelligent intrusion detection inside
the application. These detection points can be used to identify a
malicious user that is probing for vulnerabilities or weaknesses within
your application.

[Read
more](http://www.owasp.org/index.php/ApplicationLayerIntrustionDetection)
about why application logging is the way to go.

**TOC**

# Detection Points

::: {#re}
:::

## RequestException

::: {#RE1}
:::

### RE1: Unexpected HTTP Command

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE1
  Title            Unexpected HTTP Command
  Category         RequestException
  Description      An HTTP request is received which contains unexpected/disallowed commands.
  Considerations   A list of accepted commands should be generated (i.e. GET and POST) and all other HTTP commands should generate an event. See \[HTTP/1.1: Method Definitions\](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html).
  Tuning           Browsers and proxies using the HEAD method to check whether the content of a file has changed.
  Examples         Instead of a GET or POST request, the user sends a TRACE request to the application. Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (30b) HTTP Policy Enforcement: Method Is Not Allowed by Policy (960032) - (40e) AppSensor Detection Points: Invalid Request Method for Resource (981088)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE1#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE2}
:::

### RE2: Attempt to Invoke Unsupported HTTP Method

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE2
  Title            Attempt to Invoke Unsupported HTTP Method
  Category         RequestException
  Description      An HTTP request is received which contains a non-existent HTTP command (does not match anything in this list: HEAD, GET, POST, PUT, DELETE, TRACE, OPTIONS, CONNECT).
  Considerations   \\-
  Tuning           \\-
  Examples         Instead of a GET or POST request, the user sends a TEST request to the application (TEST is not a valid HTTP request method). Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (40e) AppSensor Detection Points: Attempt to Invoke Unsupported HTTP Method (981087)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE2#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE3}
:::

### RE3: GET When Expecting POST

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE3
  Title            GET When Expecting POST
  Category         RequestException
  Description      A page which is expecting only POST requests, is requested by HTTP method GET.
  Considerations   Some pages may be designed to receive both GET and POST requests.
  Tuning           Some resources may allow both GET and POST methods e.g. an edit form may be hyperlinked using a parameter value defining the record to be edited, but the form is submitted by POST to itself. Users may bookmark a page that is the result of a POST and return to it at a later date.
  Examples         The user sends a GET request to a page which has only been used for POSTs.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE3#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE4}
:::

### RE4: POST When Expecting GET

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE4
  Title            POST When Expecting GET
  Category         RequestException
  Description      A page which is expecting only GET requests, receives a POST.
  Considerations   \\-
  Tuning           (same as RE3)
  Examples         The user utilizes a proxy tool to build a custom POST request and sends it to a page which has been accessed by GET requests.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE4#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE5}
:::

### RE5: Additional/Duplicated Data in Request

  ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE5
  Title            Additional/Duplicated Data in Request
  Category         RequestException
  Description      Additional unexpected parameters or HTTP headers, or duplicates, are received with the request.
  Considerations   Additional parameters may be an attempt to override values or to exploit unexposed functionality. Duplicated parameters may be an indication of attempted HTTP parameter pollution. Beware of firing this detector when additional cookies, not used by the application, are found (as opposed to duplicated cookies) since these may relate to third-party code (e.g. advertisements, analytics) or some other application. Note that extra HTTP headers may be added by intermediate proxies, and unless the network configuration is fixed (an internal network perhaps), additional headers cannot be controlled and thus cannot be used to infer existence of a potential attacker.
  Tuning           Links from third party sites/services may included additional parameters (e.g. from search engines, from advertisements). Additional cookies headers may be added by other applications or by third parties such as advertisers, and there may be very little control over these. Additional HTTP headers may be added by intermediate network devices (e.g. for traffic management).
  Examples         Example 1: Additional form or URL parameters submitted with request (e.g. debug=1, servervariable=2000). Example 2: A parameter is defined more than once in the URL Query String. Example 3: An HTTP header is duplicated. Example 4: An additional HTTP header is found. Example 5: A URL path parameter with the same name as a form parameter is sent with the request. Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (40e) AppSensor Detection Points: Invalid Number of Parameters - Missing Parameter(s) (981089) - (40e) AppSensor Detection Points: Invalid Number of Parameters - Additional Parameter(s) (981090) - (40e) AppSensor Detection Points: Invalid Parameter Name(s) (981091)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE5#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE5#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE5#php)
  ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE6}
:::

### RE6: Data Missing from Request

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE6
  Title            Data Missing from Request
  Category         RequestException
  Description      Expected parameters or HTTP headers are missing from the request.
  Considerations   Bookmarking and use of a browser\'s \"back button\" can lead to requests without the expected parameters.
  Tuning           A bookmarked page may be missing the required POST parameters (see also RE3). Users may choose to send a blank or different User Agent header value.
  Examples         Example 1: A page is requested without any of the required form parameters. Example 2: The HTTP-Accept header is not present in a request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE6#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE6#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE6#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE7}
:::

### RE7: Unexpected Quantity of Characters in Parameter

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE7
  Title            Unexpected Quantity of Characters in Parameter
  Category         RequestException
  Description      The user provides a parameter value with a large number of characters.
  Considerations   \\-
  Tuning           If the input field does not have client-side validation and/or MAXLENGTH attributes, a user might inadvertently copy in some text that is longer than expected.
  Examples         Example 1: The user submits a form field with more characters than the form\'s maxlength attribute and client-side validation would allow. Example 2: The user submits data in a form\'s hidden field which is longer than expected. Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (40e) AppSensor Detection Points: Invalid Parameter Length - Value Is Below Normal Range (981092) - (40e) AppSensor Detection Points: Invalid Parameter Length - Value Is Above Normal Range (981093)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE7#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE7#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE7#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RE8}
:::

### RE8: Unexpected Type of Characters in Parameter

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RE8
  Title            Unexpected Type of Characters in Parameter
  Category         RequestException
  Description      The user provides a parameter value containing characters outwith the expected range.
  Considerations   \\-
  Tuning           Text fields may include text from copy and paste operations that contain illegal characters.
  Examples         Example 1: The user sends an HTTP header containing a line break character. Example 2: The user sends a URL parameter value that contains ASCII characters below 20 or above 7E. Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting Digits (981094) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting Letters (981095) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting AlphNumeric (981096) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting Email (981097) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting Path (981103) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting Url (981104) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting Flag (981110) - (40e) AppSensor Detection Points: Invalid Character(s) in Payload - Expecting SafeText (981105)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE8#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE8#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RE8#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE}
:::

## AuthenticationException

::: {#AE1}
:::

### AE1: Use of Multiple Usernames

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE1
  Title            Use of Multiple Usernames
  Category         AuthenticationException
  Description      Multiple usernames are attempted when logging into the application.
  Considerations   The assignment of login attempts to a user can be based on a sessionID given to the user when they first visit the website. Correlating based on IP address is difficult since multiple users could be using the site from the same IP address (e.g. corporate NAT).
  Tuning           \\-
  Examples         User first tries username \'bob\', then username \'sue\', then \'steve\', etc.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE1#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE2}
:::

### AE2: Multiple Failed Passwords

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE2
  Title            Multiple Failed Passwords
  Category         AuthenticationException
  Description      For a single username, multiple bad passwords, or other authentication credentials, are entered.
  Considerations   See \[Popularity is Everything\](http://www.eecs.harvard.edu/\~michaelm/postscripts/hotsec2010.pdf) section 4 - Attack-Detection Scenarios for ideas about tracking use of unsuccessful passwords and looking whether these are used against multiple accounts.
  Tuning           A users providing the same wrong password more than once may be different to different wrong passwords. See \[Account Lockout, Bill Cheswick, Episode 76, OWASP Podcast, September 22, 2010\](http://www.owasp.org/index.php/OWASP_Podcast#tab=Latest_Shows).
  Examples         Example 1: User tries username:password combination of \'user:pass1\', \'user:pass2\', \'user:pass3\', etc. Example 2: Multiple failed PINs are attempted for the same customer account. Example 3: In an online banking application, several invalid mobile authentication codes, transaction verification codes or transaction authentication numbers are submitted. Example 4: A user provides the correct password, but repeatedly fails to provide the required second password correctly.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE2#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE3}
:::

### AE3: High Rate of Login Attempts

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE3
  Title            High Rate of Login Attempts
  Category         AuthenticationException
  Description      The rate of login attempts becomes too high (possibly indicating an automated login attack).
  Considerations   The threshold should relate to a limit and period appropriate to the application (e.g. total number in a second or minute or hour).
  Tuning           \\-
  Examples         User sends the following login attempts within 1 second - \'user1:pass1\', \'user1:pass2\', \'user2:pass3\', \'user2:pass4\'.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE3#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE4}
:::

### AE4: Unexpected Quantity of Characters in Username

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE4
  Title            Unexpected Quantity of Characters in Username
  Category         AuthenticationException
  Description      The user provides a username with a large number of characters.
  Considerations   \\-
  Tuning           (same as RE7)
  Examples         The user sends a username that is 200 characters long when 6-8 are expected.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE4#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE5}
:::

### AE5: Unexpected Quantity of Characters in Password

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE5
  Title            Unexpected Quantity of Characters in Password
  Category         AuthenticationException
  Description      The user provides a password with a large number of characters.
  Considerations   Higher limits may be required for sites which allow users to have pass phrases.
  Tuning           (same as RE7)
  Examples         Example 1: The user sends a password that is 200 characters long, when 5-20 are expected. Example 2: The user sends a PIN of 30 characters.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE5#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE5#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE5#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE6}
:::

### AE6: Unexpected Type of Character in Username

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE6
  Title            Unexpected Type of Character in Username
  Category         AuthenticationException
  Description      The user provides a username which contains characters outwith the expected range.
  Considerations   Any characters below hex value 20 or above 7E are often considered illegal (decimal values of below 32 or above 126).
  Tuning           Users may be confused between a username, customer identification code and their account number, or even between offline and online identifiers. Mis-typing might add a character like \"\\\]\" or \"\\#\" if these are adjacent to the ENTER/CR key. Whitespace may be appended to values when copied from a spreadsheet cell (e.g. a line feed character when cell values are copied and pasted from Excel). A password may be put in the username field by accident.
  Examples         The user sends a username that contains ASCII non-printable characters such as the NULL byte.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE6#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE6#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE6#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE7}
:::

### AE7: Unexpected Type of Character in Password

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE7
  Title            Unexpected Type of Character in Password
  Category         AuthenticationException
  Description      The user provides a password containing characters outwith the expected range.
  Considerations   Examples include null byte, and characters which need the ALT key to be used.
  Tuning           (same as AE6)
  Examples         The user sends a password that contains ASCII characters below 20 or above 7E.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE7#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE7#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE7#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE8}
:::

### AE8: Providing Only the Username

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE8
  Title            Providing Only the Username
  Category         AuthenticationException
  Description      The user submits a POST request which only contains the username variable. The password variable has been removed.
  Considerations   This is different from only providing the username in the login form since in that case the password variable would be present and empty.
  Tuning           \\-
  Examples         The user utilizes a proxy tool to remove the password variable from the submitted POST request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE8#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE8#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE8#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE9}
:::

### AE9: Providing Only the Password

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE9
  Title            Providing Only the Password
  Category         AuthenticationException
  Description      The user submits a POST request which only contains the password variable. The username variable has been removed.
  Considerations   This is different from only providing the password in the login form since in that case the username variable would be present and empty.
  Tuning           \\-
  Examples         The user utilizes a proxy tool to remove the username variable from the submitted POST request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE9#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE9#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE9#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE10}
:::

### AE10: Additional POST Variable

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE10
  Title            Additional POST Variable
  Category         AuthenticationException
  Description      Additional, unexpected POST variables are received during an authentication request.
  Considerations   \\-
  Tuning           (same as RE5)
  Examples         The user utilizes a proxy tool to add the POST variable of \'admin=true\' to the request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE10#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE10#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE10#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE11}
:::

### AE11: Missing POST Variable

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE11
  Title            Missing POST Variables
  Category         AuthenticationException
  Description      Expected POST variables are not present within the submitted authentication request.
  Considerations   \\-
  Tuning           (same as RE6)
  Examples         The user utilizes a proxy tool to remove an additional POST variable, such as \'guest=true\', from the POST request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE11#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE11#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE11#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE12}
:::

### AE12: Utilization of Common Usernames

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE12
  Title            Utilization of Common Usernames
  Category         AuthenticationException
  Description      Common dictionary usernames are used to attempt to log into the application.
  Considerations   \\-
  Tuning           Common usernames might be allowed during self-registration or when editing account details.
  Examples         Log in attempted with usernames \"administrator\", then \"admin\", then \"test\"
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE12#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE12#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE12#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#AE13}
:::

### AE13: Deviation from Normal GEO Location

  ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               AE13
  Title            Deviation from Normal GEO Location
  Category         AuthenticationException
  Description      In some applications, most users log in from one or a just a few geographic locations. If the application learns these GeoIP locations, it can then detect when a user is logging into the application from a different location. This would help to identify possible account hijacking attacks (from phishing, banking trojans).
  Considerations   Use of applications while mobile.
  Tuning           \\-
  Examples         Example 1: A banking customer\'s IP address has never been seen before when they log in. Example 2: A system attempts to authenticate to web services from a different country.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE13#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE13#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_AE13#php)
  ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#SE}
:::

## SessionException

::: {#SE1}
:::

### SE1: Modifying Existing Cookie

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               SE1
  Title            Modifying Existing Cookie
  Category         SessionException
  Description      A request is received containing a cookie with a modified value.
  Considerations   This could be determined if the cookie is modified to an illegal value.
  Tuning           In a poorly designed application, the length of the cookie value, or the combined size of all the cookies, might possibly exceed that which is supported.
  Examples         Example 1: The user utilizes a proxy tool to change the encrypted cookie to an alternative value which does not properly decode within the application. Example 2: The user modifies an unencrypted cookie and sets an illegal value for a particular variable.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE1#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#SE2}
:::

### SE2: Adding New Cookie

  ---------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               SE2
  Title            Adding New Cookie
  Category         SessionException
  Description      A request is received which contains additional cookies that are not expected by the application.
  Considerations   A session cookie existing when it should not (e.g. prior to authentication) is probably indicative of an attack. But cookies may also be set by third party sites which get send with the request - these may be harmless. Also consider what other applications exist on sub-domains (e.g. www.example.com, extranet.example.com and sales.example.com) which may also be setting cookies.
  Tuning           \\-
  Examples         The user utilizes a proxy tool to add cookies to the request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE2#php)
  ---------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#SE3}
:::

### SE3: Deleting Existing Cookie

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               SE3
  Title            Deleting Existing Cookie
  Category         SessionException
  Description      A request is received which does not contain the expected cookies.
  Considerations   The user may have bookmarked a page they had visited during a previous authenticated session.
  Tuning           In a poorly designed application, the number of cookies might exceed the allowed number supported by the user\'s browser.
  Examples         The user utilizes a proxy tool to remove cookies or portions of cookies from a request.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE3#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#SE4}
:::

### SE4: Substituting Another User's Valid Session ID or Cookie

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               SE4
  Title            Substituting Another User\'s Valid Session ID or Cookie
  Category         SessionException
  Description      A request is received which contains cookie data that is clearly from another user or another session.
  Considerations   \\-
  Tuning           A mis-configured proxy might send the same session ID or cookie for all users.
  Examples         The user utilizes a proxy tool to substitute valid data from another user or session into the cookie. An example would be changing some sort of identification number within the cookie.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE4#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#SE5}
:::

### SE5: Source Location Changes During Session

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               SE5
  Title            Source Location Changes During Session
  Category         SessionException
  Description      Valid requests, containing valid session credentials, are received from multiple source locations indicating a possible session hijacking attack.
  Considerations   A full IP address may not be constant for some users during normal use due to clustered proxies or while mobile. Enforcing single fixed IP addresses for each session in an intranet application may be valid. However, if the application is accessible over public networks, changing IP address cannot be excluded and it may be more useful to consider fixing just part of the IP address, or looking for more significant changes such as when the user\'s IP address geo-location region or country changes (see \[Autonomous System Number\](http://www.apnic.net/services/services-apnic-provides/helpdesk/faqs/asn-faqs) (ASN) and \[Detecting Malice with ModSecurity: GeoLocation Data\](http://blog.modsecurity.org/2010/10/detecting-malice-with-modsecurity-geolocation-data.html)). Note: source port number should not be used in checks since this usually changes very frequently.
  Tuning           If the full IP address is used for this, it may change slightly from request to request by the same user.
  Examples         Example 1: User A\'s session is compromised and User B begins using the account. The requests originating from User B will possibly contain a different source IP address the User A. The source IP addresses could be the same if both users where behind the same NAT. Example 2: An application at a fixed server location, which calls web services, changes IP address unexpectedly.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE5#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE5#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE5#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#SE6}
:::

### SE6: Change of User Agent Mid Session

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               SE6
  Title            Change of User Agent Mid Session
  Category         SessionException
  Description      The User-Agent value of the header changes during a session. This may indicate a different browser is now being used. Although this value is under the control of the sender, a change in this may indicates that the session has been compromised and is being used another individual. This will likely not be the case that the user has simply copied and pasted the URL from one browser to another on the same system because this action would not copy over the appropriate session identifiers.
  Considerations   The User Agent string may change in some browsers when the content type changes (e.g. from HTML to PDF). This detection point may only be useful in environments where a single browser is deployed. Optionally also include other HTTP headers in this check. For example, the Accept-Encoding and Accept-Language headers do not normally change and could be concatenated with the User-Agent and hashed to created an identifier. The \[ideas\](http://panopticlick.eff.org/about.php) described in \[Panopticlick\](http://panopticlick.eff.org/), \[client identification mechanisms\](https://sites.google.com/a/chromium.org/dev/Home/chromium-security/client-identification-mechanisms), \[canvas fingerprinting\](http://www.darknet.org.uk/2014/07/clear-cookies-cant-escape-canvas-fingerprinting/) and \[JavaScript browser fingerprinting\](http://www.businessinfo.co.uk/labs/probe/probe.php) can also be used to fingerprint a particular client system but require the use of client-side code. Application owners should check the legality of collecting data, and whether it is considered \"personal data\" which may have additional constraints in some jurisdictions.
  Tuning           \\-
  Examples         Mid session, the User Agent changes from Firefox to Internet Explorer.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE6#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE6#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_SE6#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#ACE}
:::

## AccessControlException

::: {#ACE1}
:::

### ACE1: Modifying URL Argument Within a GET for Direct Object Access Attempt

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               ACE1
  Title            Modifying URL Argument Within a GET for Direct Object Access Attempt
  Category         AccessControlException
  Description      The application is designed to use an identifier for a particular object, such as using categoryID=4 or user=guest within the URL. A user modifies this value in an attempt to access unauthorized information. This exception should be thrown anytime the identifier received from the user is not authorized due to the identifier being non-existent or the identifier not authorized for that user.
  Considerations   \\-
  Tuning           Bookmarking , truncation, and mistyping issues could lead to some access control exceptions.
  Examples         The user modifies the following URL from example.com/viewpage?page=1\\&user=guest to example.com/viewpage?page=22\\&user=admin
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE1#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#ACE2}
:::

### ACE2: Modifying Parameter Within A POST for Direct Object Access Attempt

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               ACE2
  Title            Modifying Parameter Within A POST for Direct Object Access Attempt
  Category         AccessControlException
  Description      The value of a non-free text html form element (i.e. drop down box, radio button) is modified to an illegal value. The value either does not exist or is not authorized for the user.
  Considerations   \\-
  Tuning           (same as ACE1 for bookmarking)
  Examples         The user utilizes a proxy tool to intercept a POST request and changes the submitted value to a value that was not available through the normal display. For example, the user encounters a dropdown box containing the numbers 1 through 10. The user selects 5 and then intercepts the request to change the submitted value to 100.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE2#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#ACE3}
:::

### ACE3: Force Browsing Attempt

  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               ACE3
  Title            Force Browsing Attempt
  Category         AccessControlException
  Description      An authenticated or unauthenticated user sends a request for a non-existent resource (e.g. page, directory listing, image, file, etc), or a resource that is not authorized for that user.
  Considerations   \\-
  Tuning           Requests for non-existent resources may occur for many reasons such as \[Benign Unexpected URLs - Part 1 - Missing (404 Not Found Error) Files\](http://www.clerkendweller.com/2010/10/26/Benign-Unexpected-URLs-Part-1-Missing-Files)
  Examples         Example 1: The user is authenticated and requests site.com/PageThatDoesNotExist. Example 2: The user is authenticated and requests a video they are not authorized to download/view. Example 3: An unauthenticated user (perhaps with a session ID) requests a listing of a directory detailed in the site\'s robots.txt file.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE3#php)
  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#ACE4}
:::

### ACE4: Evading Presentation Access Control Through Custom POST

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               ACE4
  Title            Evading Presentation Access Control Through Custom POST
  Category         AccessControlException
  Description      A POST request is received which is not authorized for the current user and the user could not have performed this action without crafting a custom POST request.
  Considerations   This situation is most likely to occur when presentation layer access controls are in place and have removed the user\'s ability to initiate the action through the presentation of the application. An attacker may be aware of the functionality and attempt to bypass this presentation layer access control by crafting their own custom message and sending this in an attempt to execute the functionality.
  Tuning           \\-
  Examples         The application contains the ability for an administrator to delete a user. This method is normally invoked by entering the username and submitting to \<https://oursite/deleteuser\> Presentation layer access controls ensure the delete user form is not displayed to non-administrator users. A malicious user has access to a non-administrator account and is aware of the delete user functionality. The malicious user sends a custom crafted POST message to \<https://oursite/deleteuser\> in an attempt to execute the delete user method.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_ACE4#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#IE}
:::

## InputException

::: {#IE1}
:::

### IE1: Cross Site Scripting Attempt

  ----------------------------------- ----------------------------------------------------------------------------
  ID                                  IE1

  Title                               Cross Site Scripting Attempt

  Category                            InputException

  Description                         The HTTP request contains common XSS attacks which are often used by
                                      attackers probing for XSS vulnerabilities.

  Considerations                      Detection should be configured to test all GET and POST values as well as
                                      all header names and values for the following values.

  Tuning                              There are many patterns which could be XSS but may also be normal user input
                                      to a free text field e.g. \"Press the \'drop\' button\" if a pattern were
                                      looking for a single quotation mark followed by SQL commands like DROP,
                                      INSERT, UPDATE and DELETE. Applications that are used to discuss or share
                                      information about programming, software development and security may want to
                                      allow such free text input, provided it is encoded/escaped correctly.

  Examples                            The user utilizes a proxy tool to add an XSS attack to the header value and
                                      the \'displayname\' POST variable. The header value could be displayed to an
                                      admin viewing log files and the \'displayname\' POST variable may be stored
                                      in the application and displayed to other users. Note, the following XSS
                                      attacks would only be used by an attacker to probe for vulnerability. An
                                      actual XSS attack would be customized by the attacker. \`\`\`javascript
                                      
                                      alert(String.fromCharCode(88,83,83)) ![](javascript:alert('XSS');) \<IMG
                                      SRC=javascript:alert(\'XSS\')\> \<IMG SRC=javascript:alert(\"XSS\")\> \<BODY
                                      ONLOAD=alert(\'XSS\')\> \`\`\` Cross references: - \[OWASP ModSecurity Core
                                      Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project
                                      \"wikilink\") v2.2.7 - (41c) XSS Attacks: Cross-site Scripting (XSS) Attack
                                      (106 Rules)

  Code                                \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE1#java)
                                      \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE1#net)
                                      \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE1#php)
  ----------------------------------- ----------------------------------------------------------------------------

::: {#IE2}
:::

### IE2: Violation Of Implemented White Lists

  ---------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               IE2
  Title            Violation Of Implemented White Lists
  Category         InputException
  Description      The application receives user-supplied data that violates an established white list validation.
  Considerations   See AC3 (Force Browsing Attempts) about requests for non-existent/unauthorised (i.e. not white listed) URLs.
  Tuning           (same as IE1)
  Examples         The user submits data that is not correct for the particular field. This may not be attack data necessarily, but repeated violations could be an attempt by the attacker to determine how an application works or to discover a flaw.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE2#php)
  ---------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#IE3}
:::

### IE3: Violation Of Implemented Black Lists

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               IE3
  Title            Violation Of Implemented Black Lists
  Category         InputException
  Description      The application receives user-supplied data that violates an established black list validation.
  Considerations   This may not be attack data necessarily, but repeated violations could be an attempt by the attacker to determine how an application works or to discover a flaw or to exploit a flaw. This black list approach suffers from the potential for greater false positives than IE2 above, and cannot be used to identify all potential malicious data.
  Tuning           (same as IE1)
  Examples         Example 1: URL in comment field identified as suspected phishing and malware pages using \[Google Safe Browsing API\](http://code.google.com/apis/safebrowsing/)). Example 2: Parameter value matches a known SQL injection pattern. Example 3: Parameter value matches a known XSS pattern.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE3#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#IE4}
:::

### IE4: Violation of Input Data Integrity

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               IE4
  Title            Violation of Input Data Integrity
  Category         InputException
  Description      The application receives HTTP header or body parameter values which have been tampered with when no change should have occurred.
  Considerations   \\-
  Tuning           This detection point should only be used with parameters that cannot be altered by accident. Input types text and textarea would not normally be suitable, even if the elements are disabled in the browser. Be wary of assuming JavaScript will prevent modification of form elements in all conditions.
  Examples         Example 1: Hidden form field modified by client. Example 2: Select list value submitted in response, not sent by server as an available option value. Example 3: Cookie set by server has been manipulated by the client. Example 4: Cookie created by client instead of by the server.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE4#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#IE5}
:::

### IE5: Violation of Stored Business Data Integrity

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               IE5
  Title            Violation of Stored Business Data Integrity
  Category         InputException
  Description      User\'s input leads to violation of data integrity.
  Considerations   \\-
  Tuning           \\-
  Examples         Example 1: A user\'s action leads to a system integrity error when writing to, or updating, a database. Example 2: Business rule checks detect that a user\'s action is not compatible. Example 3: Data accuracy checking detects duplicate records for a user. Example 4: User input leads to an unexpected file change (e.g. .htaccess file overwritten, page template changed). Example 5: User\'s request leads to a new, unexpected, outbound network connection being made (e.g. mail sent to an SMTP server, files downloaded from a FTP server).
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE5#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE5#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE5#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#IE6}
:::

### IE6: Violation of Security Log Integrity

  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               IE6
  Title            Violation of Security Log Integrity
  Category         InputException
  Description      Security or audit log tampering detected.
  Considerations   AppSensor may rely on the accuracy of \"log\" data to make decisions when thresholds are reached. This detector aims to detect the insertion of forged entries, corruption of logs, unauthorised deletion of and changes to records. See also: - \[NIST SP 800-92 Guide to Security Log Management\](http://csrc.nist.gov/publications/nistpubs/800-92/SP800-92.pdf) - \[Tamper Detection in Audit Logs\](http://www.cs.toronto.edu/vldb04/protected/eProceedings/contents/pdf/RS13P1.PDF) - \[Forensic Tamper Detection in SQL Server\](http://www.sqlsecurity.com/images/tamper/tamperdetection.htm)
  Tuning           \\-
  Examples         Example 1: Special characters embedded in logged data about a user\'s activity cause the data to overwrite a previous log entry. Example 2: Log file integrity is broken by modification to an existing log entry.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE6#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE6#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_IE6#php)
  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#IE7}
:::

### IE7: Detect Abnormal Content Output Structure

  ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               IE7
  Title            Detect Abnormal Content Output Structure
  Category         InputException
  Description      Output data is of an unexpected format, structure or contains unexpected components.
  Considerations   \\-
  Tuning           \\-
  Examples         Example 1: An abnormal number of inline scripts or iframes are returned in an HTML page indicating a successful XSS injection. Example 2: An XML file generated utilizing user input no longer matches the expected structure/schema/document declaration. Example 3: Generated JSON data contains does not match expected format.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE2#php)
  ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#EE}
:::

## EncodingException

::: {#EE1}
:::

### EE1: Double Encoded Character

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               EE1
  Title            Double Encoded Characters
  Category         EncodingException
  Description      An HTTP request is received which contains one or more double encoded values.
  Considerations   \\-
  Tuning           Data supplied by other party systems may have encoding issues.
  Examples         The user sends encodes the % symbol to %25 and appends 3C. The user is sending %253C which may be interpreted by the application as %3C which is actually \\\<.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_EE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_EE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_EE1#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#EE2}
:::

### EE2: Unexpected Encoding Used

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               EE2
  Title            Unexpected Encoding Used
  Category         EncodingException
  Description      An HTTP request is received which contains values that have encoded in an unexpected format.
  Considerations   \\-
  Tuning           (same as EE1)
  Examples         The user encodes an attack such as alert(document.cookie) into the UTF-7 format and sends this data the application. This could bypass validation filters and be rendered to a user in certain situations. Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (30c) HTTP Policy Enforcement: Request Content Type Is Not Allowed by Policy (960010)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_EE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_EE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_EE2#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#CIE}
:::

## CommandInjectionException

::: {#CIE1}
:::

### CIE1: Blacklist Inspection for Common SQL Injection Values

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               CIE1
  Title            Blacklist Inspection for Common SQL Injection Values
  Category         CommandInjectionException
  Description      A request is received which contains common SQL injection attack attempts.
  Considerations   The point of this detection is not to detect all variations of a SQL injection attack, but to detect the common probes which an attacker or tool might use to determine if a SQL injection vulnerability is present. Unless the site contains some sort of message board for discussing SQL injection, there is little reason that the SQL injection examples should ever be received from a user request.
  Tuning           (same as IE1)
  Examples         The user sends a request and modifies a URL parameter from category = 5 to category = 5\' OR \'1\' = \'1 in an attempt to perform an SQL injection attack. The user could perform similar attacks by modifying POST variables or even the request headers to contain SQL injection attacks. \' OR \'1\'=\'1 \' OR \'a\'=\'a \' OR 1=1\-- xp_cmdshell UNION JOIN Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (41c) SQL Injection Attacks (13 Rules) - (48e) Bayesian Analysis Detects Probable Attack: SQL Injection Attack (-)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE1#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#CIE2}
:::

### CIE2: Detect Abnormal Quantity of Returned Records

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               CIE2
  Title            Detect Abnormal Quantity of Returned Records
  Category         CommandInjectionException
  Description      A database query is executed which returns more records than expected.
  Considerations   \\-
  Tuning           \\-
  Examples         Example 1: A query of a non-SQL dataset should only return 1 record but 100 records are returned. Example 2: The application is designed to allow a user to maintain 5 profiles. A user makes a request to view all of their profiles. The database SQL query, which is expected to always return 5 or less results, returns 10,000 records. Something in the application, or user\'s actions, has caused unauthorized data to be returned. Example 3: Extraction of data from an XML file should only return one matching node, but more than one is returned.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE2#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#CIE3}
:::

### CIE3: Null Byte Character in File Request

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               CIE3
  Title            Null Byte Character in File Request
  Category         CommandInjectionException
  Description      A request is received to download a file from the server. The filename requested contains the null byte the file name. This is an attempted OS injection attack.
  Considerations   \\-
  Tuning           \\-
  Examples         The user modifies the filename of the requested file to download to contain the null byte. The null byte can be added by inserting the hex value %00.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE3#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#CIE4}
:::

### CIE4: Carriage Return or Line Feed Character in File Request

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               CIE4
  Title            Carriage Return or Line Feed Character in File Request
  Category         CommandInjectionException
  Description      A request is received which contains the carriage return or line feed characters within the POST data or the URL parameters. This is an attempted HTTP split response attack.
  Considerations   \\-
  Tuning           \\-
  Examples         The user includes the hex value %0D or %0A in the HTTP request POST data or URL parameters. Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (40b) Generic Attacks: PHP Injection (959151,958976)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_CIE4#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#FIO}
:::

## FileIOException

::: {#FIO1}
:::

### FIO1: Detect Large Individual File

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               FIO1
  Title            Detect Large Individual File
  Category         FileIOException
  Description      A file upload feature detects that a large file has been submitted for upload which exceeds the maximum upload size.
  Considerations   \\-
  Tuning           \\-
  Examples         The user attempts to upload a large file to occupy resources or fill up disk space.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_FIO1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_FIO1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_FIO1#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#FIO2}
:::

### FIO2: Detect Large Number of File Uploads

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               FIO2
  Title            Detect Large Number of File Uploads
  Category         FileIOException
  Description      A user uploads an excessively large number of files.
  Considerations   The limit and period used to determine the threshold rate is application dependent, and may also depend on the user\'s role.
  Tuning           \\-
  Examples         A single user attempts to upload multiple small files to occupy resources or fill up disk space.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_FIO2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_FIO2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_FIO2#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#HT}
:::

## Honey Trap

::: {#HT1}
:::

### HT1: Alteration to Honey Trap Data

  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               HT1
  Title            Alteration to Honey Trap Data
  Category         HoneyTrap
  Description      Fake (not otherwise needed by the application) data sent to the user and returned (e.g. as form, URL, cookie values or in the path or HTTP header) is modified. This is usually combined with making the name or value a tempting item for an attacker to try modifying.
  Considerations   Similar techniques can also be used for the creation of accessible CAPTCHA. See also ideas at \<http://blogs.sans.org/appsecstreetfighter/2009/06/04/my-top-6-honeytokens/\>
  Tuning           \\-
  Examples         Example 1: Otherwise useless hidden fields, which look like potential vulnerabilities, added to some forms are sent back to the server modified (e.g. ). Example 2: An additional URL parameter, which is not used by the application, is modified by the user (e.g. www.example.com/account.jsp?debug=0). Example 3: An additional fake cookie is added and is modified by the user. Example 4: URL rewriting is used and a fake directory name is added; this is modified by the user (e.g. www.example.com/orders/normaluser/display.php). Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (40e) AppSensor Detection Points: Tampering of Hidden Parameter Honeytrap Data (981131)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT1#php)
  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#HT2}
:::

### HT2: Honey Trap Resource Requested

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               HT2
  Title            Honey Trap Resource Requested
  Category         HoneyTrap
  Description      A purposely leaked resource that has no use in normal application use is requested by a user.
  Considerations   Ensure the resource is not linked from normal application content such that a spider or robot might find the resource in any case.
  Tuning           \\-
  Examples         Example 1: Page, directory or other resource listed in the application\'s robots.txt robots exclusion file is requested by the user. Example 2: URL identified only in HTML comments is requested by the user. Example 3: Unexposed server function call included in Flash file source code is requested by the user.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT2#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#HT3}
:::

### HT3: Honey Trap Data Used

  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               HT3
  Title            Honey Trap Data Used
  Category         HoneyTrap
  Description      Special data sent or accessed by a user.
  Considerations   For honey trap data that is detected on egress only, use of outbound content monitoring (e.g. a web application firewall or similar technique) may be helpful.
  Tuning           \\-
  Examples         Example 1: Fake user name and password only visible in source HTML code used to attempt to log in to the application (e.g. in HTML comments, in server-side code \'accidentally\' delivered to the user). Example 2: A special code number or account name is left in a discussion forum site; this is then used in the application. Example 3: An attempt is made to authenticate with the user name listed in the first row (e.g. ID=1) of the application\'s database table of Users. Example 4: Data from a fake account record is sent by the server and detected; this record should not normally be accessible by anyone using the application.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_HT3#php)
  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#UT}
:::

## UserTrendException

::: {#UT1}
:::

### UT1: Irregular Use of Application

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               UT1
  Title            Irregular Use of Application
  Category         UserTrendException
  Description      The application receives an unusual pattern of requests for the same page or feature from a user. The user may be sending different data combinations or trying to detect errors in the page.
  Considerations   \\-
  Tuning           Use of bookmarked URLs and the \"back\" button might generate out-of-sequence requests. See also related frequency of feature use in UT4.
  Examples         Example 1: The user requests a particular page, such as the address update page, numerous times. Example 2: The user requests a page out-of-sequence, such as an intermediate step in a multi-stage form, or a series of actions that do not map to a valid business process. Example 3: The user only requests dynamic content, and not the associated static files (e.g. images, styles heets). Example 4: The user sends a slow request/read in an attempt at application denial of service.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT1#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#UT2}
:::

### UT2: Speed of Application Use

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               UT2
  Title            Speed of Application Use
  Category         UserTrendException
  Description      The speed of requests from a user indicates that an automated tool is being used to access the site. The use of a tool undertaking a high number of requests quickly may indicate unapproved content scraping or data gathering, reconnaissance for an attack, or attempts to identify vulnerabilities in the site. Slow usage (e.g. between account creation and use) might indicate automated account creation that are then used subsequently for attacks.
  Considerations   If enforced inappropriately or too rigorously, this detection point could lead to false positives.
  Tuning           Time periods need to be set broadly enough to cater for the normal spread in user behavior. Some users may use automated tools that store passwords securely to populate and submit authentication forms.
  Examples         Example 1: The user utilizes an automated tool to request hundreds of pages per minute. Example 2: The user does not log in to the site until a long time after their account is created. Example 3: New (uncached) static content such as images and style sheets associated with each page are not requested in a similar time period as the page. Example 4: A CAPTCHA challenge is responded to more quickly than a human could possibly do. Example 5: The user\'s clickstream data velocity is too high. Example 6: The time interval between the applications displaying a page/form and the time for the user to complete the page/form and submit it is too fast. Example 7: A web scraping tool is used to obtain content from a website.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT2#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#UT3}
:::

### UT3: Frequency of Site Use

  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               UT3
  Title            Frequency of Site Use
  Category         UserTrendException
  Description      Change in how often the site is used by a user
  Considerations   \\-
  Tuning           Some users may correctly change their behavior in the frequency of accessing the application.
  Examples         The user normally accesses the site once per week, but this changes to many times per day.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT3#php)
  ---------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#UT4}
:::

### UT4: Frequency of Feature Use

  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               UT4
  Title            Frequency of Feature Use
  Category         UserTrendException
  Description      The rate of a user utilizing a particular application feature changes dramatically.
  Considerations   \\-
  Tuning           It may be valid for some functionality may be requested repeatedly. For example a real customer placing many orders, a press officer publishing a backlog of press releases, or an administrator populating a staff directory.
  Examples         Example 1: The user submits many forum messages in a short period of time. Example 2: The user adds many new friends rapidly.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_UT4#php)
  ---------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#STE}
:::

## SystemTrendException

::: {#STE1}
:::

### STE1: High Number of Logouts Across The Site

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               STE1
  Title            High Number of Logouts Across The Site
  Category         SystemTrendException
  Description      A sudden spike in logouts across the application could indicate a XSS and CSRF attack placed within the application which is automatically logging off users.
  Considerations   \\-
  Tuning           \\-
  Examples         The hourly usage of the log-off feature of the application suddenly spikes by 500%.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE1#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#STE2}
:::

### STE2: High Number of Logins Across The Site

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               STE2
  Title            High Number of Logins Across The Site
  Category         SystemTrendException
  Description      A sudden spike in logins across the application could indicate users being redirected to the site from a phishing email looking to exploit a XSS vulnerability in the site.
  Considerations   \\-
  Tuning           \\-
  Examples         The hourly usage of the logon feature of the application suddenly spikes by 1,000%.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE2#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#STE3}
:::

### STE3: Significant Change in Usage of Same Transaction Across The Site

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               STE3
  Title            Significant Change in Usage of Same Transaction Across The Site
  Category         SystemTrendException
  Description      A sudden spike in similar activity across numerous users of the application may indicate a phishing attack or CSRF attack against the users; a rapid reduction in activity may indicate users are being redirected elsewhere; a significant change in average transaction value or other quantitative measure may indicate suspicious activity.
  Considerations   External events (e.g. a news item) may lead to additional unexpected traffic which is not an attack.
  Tuning           A special requirement, situation or event may dramatically change the rate of use of certain transactions. (See also UT4)
  Examples         Example 1: The hourly usage of the update email address feature of the application suddenly spikes by 2,000%. Example 2: A website is compromised and users are redirected to a malicious site part-way through a process; the number of successful fully completed transactions drops to nil. Example 3: A number of slow requests/reads are received in an attempt at application denial of service. Example 4: The find contacts functionality is used excessively to identify related friends.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_STE3#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RP}
:::

## Reputation

These reputation detection points could be treated either as:

- like any other detection point contributing to the count of suspicious
  events, or
- used to alter security logging, or the threshold levels, or associated
  response actions

The former could lead to a much higher false positive rate.

::: {#RP1}
:::

### RP1: Suspicious or Disallowed User Source Location

  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RP1
  Title            Suspicious or Disallowed User Source Location
  Category         Reputation
  Description      The user is identified as using an IP address associated with a blacklist
  Considerations   Suspicious or invalid geo-location, IP addresses or IP address ranges may be identified using a whitelist, internal blacklist, list of Tor nodes (e.g. \<https://torstat.xenobite.eu/\>), HTTP blacklist (e.g. \<http://www.projecthoneypot.org/httpbl.php\> and Dshield \<http://www.dshield.org\>) list of spammers (e.g. Spamhaus \<http://www.spamhaus.org/\>) or known botnets (e.g. \<http://www.shadowserver.org/wiki/\>). \"Suspicious\" may also depend upon the type of user e.g. users in the \"CMS manager\" role should be using an internal network IP address, public users could be from anywhere, customers should only be accessing the application from a particular geographical region, search engine robots should be from a limited range of IP addresses. Take care that \"suspicious\" does not contribute to greater false positives.
  Tuning           The currency and accuracy of needs to be considered when the information is used in AppSensor. The method of challenge and removal of inaccuracies, and the speed of this process, should also be considered.
  Examples         Example 1: A user with an external IP address is accessing an internal application, which should not be occurring. Example 2: An authenticated user is accessing the application using a known Tor node, and attack detection thresholds are made stricter. Example 3: An authenticated user is accessing the application from a known trustworthy IP address, and thresholds for certain activity (e.g. input data validation errors) are relaxed slightly. Example 4: The IP address of the payment authentication server, used by the application for credit card authorisation, changes.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP1#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP1#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP1#php)
  ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RP2}
:::

### RP2: Suspicious External User Behavior

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RP2
  Title            Suspicious External User Behavior
  Category         Reputation
  Description      External (to the application) devices and systems (e.g. host and network IDS, file integrity monitoring, disk usage monitoring, anti-malware service, IPS, network firewall, web application firewall, web server logging, XML gateway, database firewall, SIEM) detect anomalous behavior by the user (e.g. session and/or IP address) or suspicious user properties (e.g. fraud score, previously compromised, unusual current/previous behavior). This information can be used by the application to contribute to its knowledge about a potential attacker. In some cases, the information could be detected by the application itself (e.g. XSS pattern black listing), but may be more effectively identified by the external device, or is not known to the application normally (e.g. requests for missing resources that the web server sees, but does not pass onto the application).
  Considerations   The greater the knowledge a device or system has about the application, the greater confidence can be given to evidence of suspicious behaviour. Therefore, for example, attempted SQL injection detected by a web application firewall (WAF) might be given greater weight than information from a network firewall about the IP address. The power of AppSensor is its accuracy and low false positive rate, and the usage of external data should be carefully assessed to ensure it does not contribute to a higher false positive rate.
  Tuning           The level of trust in information from the external device/system/organization needs to be considered.
  Examples         Example 1: A network IDS has detected suspicious activity by a particular IP address, and this is used to temporarily tighten the attack detection thresholds for requests from all users in the same IP address range. Example 2: An application is using the ModSecurity web application firewall with the \[Core Rule Set\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\"), and utilises the anomaly score data passed forward in the X-WAF-Events and X-WAF-Score HTTP headers (optional rules in modsecurity_crs_49_header_tagging.conf) to adjust the level of application logging for each user. Example 3: Information from an instance of PHPIDS suggests request data may be malicious. Example 4: An adverse score is indicated for the user or IP address by a fraud detection engine, or by an external reputation or fraud rating service (e.g. \[Open Fraud Detection Project\](http://wafsec.com/index.php/api/)) Example 5: The username (email address) is related to an account compromised by a data breach (e.g. \[\';\--have i been pwned?\](http://www.haveibeenpwned.com/))
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP2#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP2#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP2#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RP3}
:::

### RP3: Suspicious Client-Side Behavior

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RP3
  Title            Suspicious Client-Side Behavior
  Category         Reputation
  Description      The application receives a report of client-side security policy exceptions.
  Considerations   Take care this information does not contribute to greater false positives.
  Tuning           \\-
  Examples         Example 1: An internal corporate intranet application detects use of a non-standard workstation configuration (e.g. using JavaScript font or plugin detection see \[SE6\](http://www.owasp.org/index.php/AppSensor_DetectionPoints#SE6:\_Change_Of_User_Agent_Mid_Session)). An alert is raised for further investigation. Example 2: An online banking application receives details of suspicious client-side behaviour that would not be expected in normal application use, via a \[Content Security Policy\](http://www.w3.org/Security/wiki/Content_Security_Policy) violation report. The application increases logging for the user, and decreases the monetary limit at which the user\'s payments require manual authorisation by bank staff. Example 3: The HTTP user agent header value does not agree with other indicators (e.g. using JavaScript detection as in example 1 above). \[Reference\](http://ha.ckers.org/blog/20100904/browser-detection-autopwn-etc/). Example 4: A honey client system monitoring the web application reports unexpected behavior in the generated web pages output. Example 5: A third-party monitoring system detects page content that is unauthorised and/or contrary to policy (e.g. structure, included links, HTML validation, inclusion of certain data such as payment card data). Example 6: Client-side code is injected that creates a hash of the page content in the receiving client web browser to monitor for manipulated HTML code. \[Reference\](http://blog.spiderlabs.com/2013/07/modsecurity-advanced-topic-of-the-week-detecting-banking-trojan-page-modifications.html) Cross references: - \[OWASP ModSecurity Core Rule Set Project\](:Category:OWASP_ModSecurity_Core_Rule_Set_Project \"wikilink\") v2.2.7 - (42e) Content Security Policy Enforcement: Content Security Policy (CSP) Violation (960001)
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP3#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP3#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP3#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

::: {#RP4}
:::

### RP4: Change to Environment Threat Level

  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ID               RP4
  Title            Change to Environment Threat Level
  Category         Reputation
  Description      The general threat level (e.g. general risk of attack from the Internet, or specific targetted attacks against an organisation) is elevated. This could also be used to change response sensitivity due to short-term effects such as application upgrades/patching.
  Considerations   This input could be used to alter thresholds for AppSensor responses.
  Tuning           The detection point could receive specially crafted input from an attacker, and therefore the information should be considered as untrusted.
  Examples         Example 1: A machine-readable threat index is read from a third-party and is used to control security logging levels. Example 2: Business circumstances (e.g. increased attention by activists) raises the suspicion the application may be at increased risk of mis-use, and response thresholds for attack detection are tightened for non-authenticated users. Example 3: The Defense Condition Level (\[DEFCON\](http://www.fas.org/nuke/guide/usa/c3i/defcon.htm)) is raised and response thresholds are changed. Example 4: Sensor signal missing. Example 5: External power source disconnected. Example 6: Firmware or software patch signing check failure.
  Code             \[Java\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP4#java) \[.Net\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP4#net) \[PHP\](http://www.owasp.org/index.php/AppSensor_DetectionPoint_RP4#php)
  ---------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

::: {#sec-response_actions .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Response Actions

# About This Document {#about-this-document}

These response actions are part of the [OWASP
AppSensor](http://www.owasp.org/index.php/Category:OWASP_AppSensor_Project)
project which advocates bringing intelligent intrusion detection inside
the application. These responses can be used to counter a malicious user
that [has been
detected](http://www.owasp.org/index.php/AppSensor_DetectionPoints)
probing for vulnerabilities or weaknesses within your application.

**TOC**

# Overview

The following table lists possible AppSensor Responses (ASRs), other
than no response (ASR-P). The application response actions are
categorized here from the user's perspective (not from the
application/server's perspective):

- Silent: User(s) unaware of any application change
- Passive: Process altered, but user(s) may still continue to process
  completion
- Active: Functionality reduced or disabled
- Intrusive: Non-malicious action on user's system

*To add a response action, just use the next available letter (e.g.
"ASR-Q") - they don't have to be in alphabetical order below, but place
it in the appropriate category (silent, passive, active or intrusive).
The image in the table below can be updated later to keep in step with
the page content.*

\![\](Appsensor_response_actions_table_1.png
\"File:Appsensor_response_actions_table_1.png\")

A text version of the table, with some examples and alternative
classifications, is described in [AppSensor - Response
Actions](http://www.owasp.org/index.php/File:Owasp-appsensor-responses.pdf)
(63 KB PDF). The information on the page below is likely to be more
up-to-date.

# Detailed Listing

Classifications are:

- Purposes: Logging, Notifying, Disrupting and Blocking
- Target: One, Some or All users
- Response duration: Instantaneous (e.g. just for the request), Period
  (e.g. time period or session duration), Permanent

## Silent

### ASR-P: No Response

  ----------------- -----------------------------------------------------------------------------------------------------------------------------------
  id                ASR-P
  title             No Response
  classifications   (not applicable)
  category          Silent
  description       There is no response. This could be used to record in logs that a detection event did not lead to any particular response action.
  consideration     
  examples          Example 1: A detection point fired, but the threshold for response has not been reached
  code              \\-
  ----------------- -----------------------------------------------------------------------------------------------------------------------------------

### ASR-A: Logging Change

  ----------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-A
  title             Logging Change
  classifications   Logging \| One, some or all users \| Instantaneous (request) or for a period
  category          Silent
  description       The granularity of logging is changed (typically more logging).
  consideration     
  examples          Example 1: Capture sanitised request headers and response bodies Example 2: Full stack trace of error messages logged Example 3: Record DNS data on user\'s IP address Example 4: Security logging level changed to include \'informational\' messages
  code              \\-
  ----------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-B: Administrator Notification

  ----------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-B
  title             Administrator Notification
  classifications   Logging and notifying \| One, some or all users \| Instantaneous
  category          Silent
  description       A notification message is sent to the application administrator(s)
  consideration     
  examples          Example 1: Email alert sent to everyone in the administration team Example 2: SMS alert sent to the on-call administrator Example 3: Visual indicator displayed on an application monitoring dashboard Example 4: Audible alarm in the control room
  code              \\-
  ----------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-C: Other Notification

  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-C
  title             Other Notification
  classifications   Logging and notifying \| One user \| Instantaneous
  category          Silent
  description       Notification message sent to something or someone other than Administrators (see ASR-B) or the User (see ASR-E)
  consideration     The message recipient (e.g. firewall) could take some action otherwise unavailable to the application (e.g. disruptive - the application makes a silent response, but the firewall actively intervenes and perhaps blocks the user).
  examples          Example 1: Broadcast event to SIEM Example 2: Signal sent to upstream network firewall, application firewall (e.g. XML, web) or load balancer Example 3: Alert sent to fraud protection department Example 4: Record added to server event log Example 5: Event highlighted in a daily management report Example 6: Email alert to staff member\'s manager Example 7: Proactive entry added to customer support system (e.g. \"Someone had difficulty logging in with this customer\'s username - request extra validation for telephone enquiries\")
  code              \\-
  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-N: Proxy

  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-N
  title             Proxy
  classifications   Logging \| One, some or all users \| For a period or permanent
  category          Silent
  description       Send the request to a different back-end location. For redirection that the user will be aware of, see See ASR-G instead.
  consideration     
  examples          Example 1: Requests from the user invisibly (from the user\'s perspective) passed through to a hardened system Example 2: Request are proxied to a special honeypot system which closely mimics or has identical user functionality
  code              \\-
  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Passive

### ASR-D: User Status Change

  ----------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-D
  title             User Status Change
  classifications   Logging \| One user \| For a period
  category          Passive
  description       A parameter related to the user is modified. This may have an impact on functionality or usability of the application, but only for the one user.
  consideration     
  examples          Example 1: Internal trustworthiness scoring about the user changed Example 2: Reduce payment transfer limit for the customer before additional out-of-band verification is required Example 3: Reduce maximum file size limit for each file upload by the forum user Example 4: Increase data validation strictness for all form submissions by this citizen Example 5: Reduce the number of failed authentication attempts allowed before the user\'s account is locked (ASR-K below)
  code              \\-
  ----------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-E: User Notification

  ----------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-E
  title             User Notification
  classifications   Logging, notifying and disrupting \| One user \| Instantaneous
  category          Passive
  description       A visual, audible and/or mechanical (e.g. vibration) signal or message is activated, displayed, or sent by other means, to the user.
  consideration     
  examples          Example 1: On-screen message about mandatory form fields (e.g. \"The \'occupation\' must be completed\") Example 2: On-screen message about data validation issues (e.g. \'The bank sort code can only contain six digits with optional hyphens\') Example 3: Message sent by email to the registered email address to inform them their password has been changed Example 4: On-screen message warning that they have been detected performing malicious activity (e.g. \[Mr Clippy\](http://www.irongeek.com/i.php?page=security/phpids-install-notes) idea)
  code              \\-
  ----------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-F: Timing Change

  ----------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-F
  title             Timing Change
  classifications   Logging and disrupting \| One, some or all users \| Instantaneous (request) or for a period
  category          Passive
  description       The usual timescales to perform an operation are altered, usually extended, or delays are added.
  consideration     
  examples          Example 1: Extend response time for each failed authentication attempt Example 2: File upload process duration extended artificially Example 3: Add fixed time delay into every response Example 4: Order flagged for manual checking Example 5: Goods despatch put on hold (e.g. despatch status changed)
  code              \\-
  ----------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Active

### ASR-G: Process Terminated

  ----------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-G
  title             Process Terminated
  classifications   Logging, notifying (sometimes) and disrupting \| One user \| Instantaneous
  category          Active
  description       An interruption to the sending, display or process, such that the user has to start again, or start somewhere else. For authenticated users, this would not include termination of their session (see ASR-J). And, they would be free to attempt the process again (e.g. access the resource after logging in, submit a payment transfer, etc).
  consideration     
  examples          Example 1: Discard data, display message and force user to begin business process from start Example 2: Redirection of an unauthenticated user to the log-in page Example 3: Redirection to home page Example 4: Display other content (i.e. terminate process but display the output of some other page without redirect) Example 5: Redirection to a page on another website
  code              \\-
  ----------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-H: Function Amended

  ----------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-H
  title             Function Amended
  classifications   Logging, notifying (sometimes), disrupting and blocking \| One, some or all users \| For a period or permanent
  category          Active
  description       The usual functionality is amended but not disabled (see ASR-I).
  consideration     
  examples          Example 1: Limit on feature usage rate imposed Example 2: Reduce number of times/day the user can submit a review Example 3: Additional registration identity validation steps Example 4: Additional anti-automation measures (e.g. out-of-band verification activated, CAPTCHA introduced) Example 5: Static rather than dynamic content returned Example 6: Additional validation requirements for delivery address Example 7: Watermarks added to pages, images and other content Example 8: Additional human interactive proof challenges added due to the number of incorrect guesses of CAPTCHAs outnumbering the correct guesses by more than a certain factor (e.g. \[Token bucket\](http://research.microsoft.com/pubs/74609/CCS2007.pdf) idea) Example 9: Fuzz responses to mask real functionality or increase attacker efforts to enumerate the application (e.g. random URL generation using \[ADHD Spider Trap\](http://sourceforge.net/p/adhd/wiki/Home/) or \[Weblabyrinth\](https://code.google.com/p/weblabyrinth/), realistic but invalid cipher text data using techniques such as \[honey encryption\](http://www.technologyreview.com/news/523746/honey-encryption-will-bamboozle-attackers-with-fake-secrets/))
  code              \\-
  ----------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-I: Function Disabled

  ----------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-I
  title             Function Disabled
  classifications   Logging, notifying (sometimes), disrupting and blocking \| One, some or all users \| For a period or permanent
  category          Active
  description       A function or functions are disabled for one, some or all users. Other functionality continues to work as normal.
  consideration     For changes that affect multiple users, be careful the response cannot be used too easily for denial of service.
  examples          Example 1: \'Add friend\' feature inactivated Example 2: \'Recommend to a colleague\' feature links removed and disabled Example 3: Document library search disabled Example 4: Prevent new site registrations Example 5: Web service inactivated or cloaked Example 6: Content syndication stopped Example 7: Automated Direct Debit system turned off and manual form offered instead
  code              \\-
  ----------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-J: Account Logout

  ----------------- -------------------------------------------------------------------------------------------------------------------------------
  id                ASR-J
  title             Account Logout
  classifications   Logging, notifying (sometimes), disrupting and blocking \| One user \| Instantaneous
  category          Active
  description       The current session is terminated on the server, and the user is logged out.
  consideration     Often undertaken in conjunction with process termination (ASR-G) and sometimes lockout (ASR-K).
  examples          Example 1: Session terminated and user redirected to logged-out message page Example 2: Session terminated only (no redirect)
  code              \\-
  ----------------- -------------------------------------------------------------------------------------------------------------------------------

### ASR-K: Account Lockout

  ----------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-K
  title             Account Lockout
  classifications   Logging, notifying (sometimes), disrupting and blocking \| One user \| For a period or permanent
  category          Active
  description       An account, session or source address is blocked from access and/or authentication.
  consideration     If IP blocking is implemented, it is recommended this is undertaken at the network layer using the operating system (e.g. iptables, Windows firewall) or by a network device (e.g. firewall).
  examples          Example 1: User account locked for 10 minutes Example 2: User account locked permanently until an Administrator resets it Example 3: One user\'s IP address range blocked Example 4: Unauthenticated user\'s session terminated
  code              \\-
  ----------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ASR-L: Application Disabled

  ----------------- -----------------------------------------------------------------------------------------------------------
  id                ASR-L
  title             Application Disabled
  classifications   Logging, notifying (sometimes), disrupting and blocking \| All users \| Permanent
  category          Active
  description       The whole application is disabled or made unavailable.
  consideration     Be careful the response cannot be used too easily for denial of service.
  examples          Example 1: Website shut down and replaced with temporary static page Example 2: Application taken offline
  code              \\-
  ----------------- -----------------------------------------------------------------------------------------------------------

## Intrusive

### ASR-M: Collect Data from User

  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  id                ASR-M
  title             Collect Data from User
  classifications   Logging \| One user \| For a period
  category          Intrusive
  description       Direct action to collect further information from the user\'s system.
  consideration     This response is meant to be non-malicious in intent - it is simply additional information gathering - and not retaliatory or damaging to the user, their systems or data, nor make any permanent change. An alert user might be aware of the action. Be very wary of data collected and perform appropriate validation and sanitization. Ensure any use of this type of response is legally permissible in the relevant jurisdictions, and complies with corporate policies and the application\'s terms of use, privacy notice and corporate policies. To a certain extent, any additional payload in a response might cause a user\'s browser or computer to crash, and this might have unforeseen circumstances. The information collection could use techniques like these described elsewhere: - \[Panopticlick\](http://panopticlick.eff.org) \[methods\](http://panopticlick.eff.org/about.php) to gather information on the user\'s browser and computer configuration - \[Response content injection\](http://www.modsecurity.org/projects/modsecurity/apache/feature_content_injection.html) using JavaScript to discover the user\'s real IP address - \[Embeddable decloaking engine\](http://decloak.net/) to discover the real IP address of a web user - \[Using ModSecurity and BeEF\](https://speakerdeck.com/rcbarnett/building-a-web-attacker-dashboard-with-modsecurity-and-beef) to monitor an attacker
  examples          Example 1: Deploy additional browser fingerprinting using JavaScript in responses Example 2: Deploy a Java applet to collect remote IP address Example 3: Deploy JavaScript to collect information about the user\'s network Example 4: Record mobile phone fingerprint and IMEI number
  code              \\-
  ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-appsensor/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-appsensor){.github-button
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

-  Flagship Project

#### Classification

-  Documentation
-  Tool

#### Audience

-  Builder
-  Breaker
-  Defender

### Source Code

- [appsensor](https://github.com/jtmelton/appsensor)

### Website

- [appsensor web site](https://appsensor.org/)

### Licensing

[MIT License](https://opensource.org/licenses/MIT)

### Leaders

- [John
  Melton](../cdn-cgi/l/email-protection.html#a4cecbccca8ac9c1c8d0cbcae4cbd3c5d7d48acbd6c3)

# Previous Leaders

- [Colin
  Watson](../cdn-cgi/l/email-protection.html#74171b181d1a5a031500071b1a341b031507045a1b0613)
- [Dennis
  Groves](../cdn-cgi/l/email-protection.html#37535259595e441950455841524477584056444719584550)
- [Michael
  Coates](../cdn-cgi/l/email-protection.html#e4898d878c858188ca878b85908197a48b93859794ca8b9683)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
