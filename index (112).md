::::::::::::::::: main-wrapper
# OWASP Maryam {#owasp-maryam .page-title}

:::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::::: {#sec-main .section .page-body}
[![Build
Status](https://app.travis-ci.com/saeeddhqan/Maryam.svg?branch=master)](https://app.travis-ci.com/github/saeeddhqan/Maryam)
![Version 2.5.3](https://img.shields.io/badge/Version-2.5.3-green.svg)
![GPLv3 License](https://img.shields.io/badge/License-GPLv3-green.svg)
![Python 3.12.x](https://img.shields.io/badge/Python-3.12.x-green.svg)
[![CII Best
Practices](https://bestpractices.coreinfrastructure.org/projects/4577/badge)](https://bestpractices.coreinfrastructure.org/projects/4577)

# OWASP Maryam {#owasp-maryam}

OWASP Maryam is a modular open-source framework based on OSINT and data
gathering. It is designed to provide a robust environment to harvest
data from open sources and search engines quickly and thoroughly.

# Installation

### Supported OS

- Linux
- FreeBSD
- Darwin
- OSX

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
$ pip install maryam
```
:::
::::

Alternatively, you can install the latest version with the following
command (Recommended):

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
pip install git+https://github.com/saeeddhqan/maryam.git
```
:::
::::

# Usage

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
# Using dns_search. --max means all of resources. --api shows the results as json.
# .. -t means use multi-threading.
maryam -e dns_search -d ibm.com -t 5 --max --api --form 
# Using youtube. -q means query
maryam -e youtube -q "<QUERY>"
maryam -e google -q "<QUERY>"
maryam -e dnsbrute -d domain.tld
# Show framework modules
maryam -e show modules
# Set framework options.
maryam -e set proxy ..
maryam -e set agent ..
maryam -e set timeout ..
# Run web API
maryam -e web api 127.0.0.1 1313
```
:::
::::

# Contribution

Here is a start guide: [Development
Guide](https://github.com/saeeddhqan/maryam/wiki/Development-Guide) You
can add a new search engine to the util classes or use the current
search engines to write a new module. The best help to write a new
module is checking the current modules.

# Roadmap

- Write a language model based search

# Links

### [OWASP](index.html)

### [Wiki](https://github.com/saeeddhqan/maryam/wiki)

### [Install](https://github.com/saeeddhqan/maryam/wiki#install)

### [Modules Guide](https://github.com/saeeddhqan/maryam/wiki/modules)

### [Development Guide](https://github.com/saeeddhqan/maryam/wiki/Development-Guide)

To report bugs, requests, or any other issues please [create an
issue](https://github.com/saeeddhqan/maryam/issues).
:::::::::
::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/saeeddhqan/maryam/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/saeeddhqan/maryam){.github-button
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

### Project Classification

![Incubator Project](../assets/images/common/owasp_level_incubator.svg)

-  Breaker
-  Builder
-  Tool

### Downloads

- [Github page](https://github.com/saeeddhqan/Maryam)
- [zip file](https://github.com/saeeddhqan/Maryam/zipball/master)
- [tar.gz file](https://github.com/saeeddhqan/Maryam/tarball/master)

### Development

- Please help us to make Maryam even better [Development
  Guide](https://github.com/saeeddhqan/maryam/wiki/Development-Guide)

### Licensing

[GNU GENERAL PUBLIC LICENSE , Version
3](https://github.com/saeeddhqan/Maryam/blob/master/LICENSE)

### Leaders

- [Saeed
  Dehghan](../cdn-cgi/l/email-protection.html#f38092969697dd97969b949b929db39c84928083dd9c8194)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::
