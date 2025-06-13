::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [features](#div-features){#features-link .tab-link role="tab"
  aria-selected="false" aria-controls="features"}
- [Supporters](#div-supporters){#supporters-link .tab-link role="tab"
  aria-selected="false" aria-controls="supporters"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}

# OWASP SecureTea Project {#owasp-securetea-project .page-title}

:::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
[![Build
Status](https://travis-ci.com/OWASP/SecureTea-Project.svg?branch=master)](https://travis-ci.com/OWASP/SecureTea-Project)
[![Codacy
Badge](https://api.codacy.com/project/badge/Grade/7e1de11511084c06bbe25ed4d629e7fd)](https://app.codacy.com/app/rejahrehim/SecureTea-Project?utm_source=github.com&utm_medium=referral&utm_content=OWASP/SecureTea-Project&utm_campaign=Badge_Grade_Settings)
[![PyPI](https://img.shields.io/pypi/v/securetea.svg)](https://pypi.org/project/securetea/)
[![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)](../LICENSE)
[![Telegram](https://img.shields.io/badge/chat%20on-telegram-blue.svg)](https://t.me/joinchat/Az5yZxQg7Djs-UZWKKCRVQ)
[![Version](https://img.shields.io/github/release/OWASP/SecureTea-Project.svg)](https://github.com/OWASP/SecureTea-Project/releases)
[![Tag](https://img.shields.io/github/tag/OWASP/SecureTea-Project.svg?color=orange&label=version)](https://github.com/OWASP/SecureTea-Project/tags)
[![GitHub
issues](https://img.shields.io/github/issues/OWASP/SecureTea-Project.svg)](https://github.com/OWASP/SecureTea-Project/issues)
[![GitHub pull
requests](https://img.shields.io/github/issues-pr/OWASP/SecureTea-Project.svg)](https://github.com/OWASP/SecureTea-Project/pulls)
[![GSOC
2019](https://img.shields.io/static/v1.svg?label=GSOC&message=Google%20Summer%20of%20Code%202019&color=blue&logo=%20data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAABLFJREFUSA2tVV1sVFUQ/s45d7ulpT+63VSkQC1IIsHyAugDAWLwQSEQI/EnaGL0QWOQ6AMo+uAzJooJJJiIiQ8qkWDURIxGIlLUqEQTKz9REEpbMFhKt7ss7e49P35zb9jaqKEkTnL33jNn5ps538ycBa5D7MH8etuTX38dLlM3jQ+2rXRf1Q/LI99T9VRTMYy/rF+hUflAIeTEPkANe2Tvz9w1fuha/pMChE/RbDNRd83JWnigwzTO2Gma5+ec6eCWgnEDcMXfhl35j43cH4yiqOYSxbZX3YviVcXEDjVWR4tMRvUEegUXQzfNRtT1PJBbw7WFjocTv5DJwZgoZy7t3+N/34YwdhbKZKA0MO6i5UQ6/K8BYBC8gNsYKr8a6rZdCJePwx97EmH0e+rTxFTUDNW8FHrOs9CLD8OdeBp+6BOoKAPBuAou70knSDaYucrfA73wXbhTW+EHdqX2ypCdlNHgigjDn8Pz0R1PwSx8B+7oBuDi/n9ATgoQW+vqp8+EWrCb4C/B9xPciMnfSuVjLhlMM1sm6/vfSNZmwZvwR5YilAZdmlH6S9YmxFjMVl2bEcon08wTcO4LqEhwMHNfhm65E+BJE2GB/SCpLP8K3bUFgpFupL+1AGNfTF8ZtbbtQNt9zOo17iaV5ltDz3iErzpyTO7bH6KOBZ/xYHoSBmXl4M++ymZYh6g1v0OwaJRIEiBwcOrMlX26cV4+eAU/+l2yqTJtiLr3Qd1EMDsONNzKzMvwpaPUbYC5fS9AG5FQZBMwJ8EQLMEUvbaH2tZ6lD4kbM7pmwl0CagOQzXOh1ncg1D9E66XWTNT1byELXmaNmW4Xx6m3RAi2ohtqNLPjsCZmTyzzwmmPdS+VhvYQmBp0gaRDmNBZSG829GUFtPAAFS33AEUf0i/RUfK6E7bqiRLkWYQQ/kOJYNKQasVhR7nMmt8QJ/xA3S6EUJNGDsD++MqHvsKqXiPgaZBNTDT4hGeO6JuT0KX/elu2vZB1eUTX8EQLEtMwU5qkF1V7rUe6/zlU6eV5hzcsDxJBH4M7tjjaQEbyT8n2JdPEKiOjbAd7vgTDDKWJt26jJPMq6V08rRgCaaco9ZF2VXoDcXCJlzYwwndzP5nnwtVnH8/9JkcGf7cbiAm16TED3Go5G4QG86E7qQPfePiyCbBEnCRWgBZhAxG/JnXSRHvms4XmJ0VbRIsuTL6XuFaCE5Bkz25o27ZklDkz2yHJwYNajJpksmtDvEQaXkUZtFHiZHr28ZALKJmLuQ+AZV+5KWlDGdj7laY2c/B/byOpxvioSIaSmKpTA5AnSY1vvANPB30greg82vg+ncgFA4nbZm4ZdugWpcT+BnWowW+l+CFr9PLzkonTsjkAKSbHTDuFfkf+ZZ3yzLoWRvrzLwXdVDSkqW0EU0T3yX48+97P7CzGqoXmTl9iB2IMQGfElpbh72YhvZsR6VCVZYPP0wFM9X0prdNU+ccpziIpN+E8/zD6TsbLpcec1mcE2Mxl5/BC5XBWQ+ArZWKVOyaUjlQ1x3p+GOtQqcY+6D6rM+wFau1bvkvkCkFEOfKgcbuyMTsTTLlMquv9rms/zepHmheIs/1AP4F9DYB6+AcwCcAAAAASUVORK5CYII=)](https://summerofcode.withgoogle.com/organizations/6362925392986112/)
[![Follow
Us](https://img.shields.io/twitter/url/https/secureteatool.svg?label=SecureTea%20Project&style=social)](https://twitter.com/secureteatool)
[![All
Contributors](https://img.shields.io/badge/all_contributors-8-orange.svg?style=flat-square)](#contributors)
[![Heroku](https://img.shields.io/badge/heroku-deployed-brightgreen)](https://secure-tea.herokuapp.com/)

Welcome to the home of the OWASP SecureTea Project !\
The OWASP SecureTea Project is an application designed to help secure a
person's laptop or computer / server with IoT (Internet Of Things) and
notify users (via various communication mechanisms), whenever someone
accesses their computer / server.

This application uses the touchpad/mouse/wireless mouse to determine
activity and is developed in Python and tested on various machines
(Linux, Mac & Windows). The software have it's own IDS(Intrusion
Detection System) / IPS(Instrusion Prevention System), firewall,
anti-virus, intelligent log monitoring capabilities with web defacement
detection, and support for much more communication medium.

**The OWASP SecureTea Project** provides a one-stop security solution
for various devices (personal computers / servers / IoT devices).

## Installation

Before installing, please make sure to install the
**[pre-requisites](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#pre-requisites)**.

You can install SecureTea from PyPi package manager using the following
command:

`$ sudo python3 -m pip install securetea`{.language-plaintext
.highlighter-rouge}

**or**

You can install SecureTea using the latest repository:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
git clone https://github.com/OWASP/SecureTea-Project.git
cd SecureTea-Project/
sudo python3 -m pip install -r requirements.txt
sudo python3 setup.py install
```
:::
::::

Please make sure all dependencies are installed if anyone of the above
fails.

For more detailed information, refer to the [installation
guide](../doc/en-US/user_guide.html#installation).

## Quick Start

1.  Start SecureTea using one or more
    [**integrations**](../doc/en-US/user_guide.html#usage):

    For example, running Intrusion Detection System only:
    `$ sudo securetea --ids`{.language-plaintext .highlighter-rouge}

2.  Start SecureTea in [**server
    mode**](../doc/en-US/user_guide.html#starting-up-in-server-mode):

    `$ sudo securetea-server`{.language-plaintext .highlighter-rouge}

3.  Start SecureTea in [**system
    mode**](../doc/en-US/user_guide.html#starting-up-in-system-mode):

    `$ sudo securetea-system`{.language-plaintext .highlighter-rouge}

4.  Start SecureTea in [**IoT
    mode**](../doc/en-US/user_guide.html#starting-up-in-iot-mode):

    `$ sudo securetea-iot`{.language-plaintext .highlighter-rouge}

For more detailed information, refer to the [usage
guide](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#usage).
:::::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::

::: {#sec-features .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Features

- [x] [Intrusion Detection
  System](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#intrusion-detection-system)
- [x]
  [Firewall](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#firewall)
- [x]
  [AntiVirus](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#antivirus)
- [x] [Server Log
  Monitor](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#server-log-monitor)
- [x] [System Log
  Monitor](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#system-log-monitor)
- [x] [Local Web Deface Detection & Prevention
  System](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#web-deface-detection)
- [x] [Auto Web Server
  Patcher](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#auto-server-patcher)
- [x] [Insecure Headers
  Detection](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#insecure-headers)
- [x] [IoT Anonymity
  Checker](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#iot-anonymity-checker)
- [x] [Auto Report Generation Using
  OSINT](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md)
- [x] [Notifying Suspicious Activities Using Various Mediums (Twitter,
  Telegram, Slack, Gmail, SMS,
  AWS)](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#setting-up-notifiers)
- [x] [Interactive GUI For Ease Of Setting
  Up](https://github.com/OWASP/SecureTea-Project/blob/master/doc/en-US/user_guide.md#configuring-using-web-ui)
:::

::: {#sec-supporters .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Contributors

Thanks goes to these wonderful people ([emoji
key](https://allcontributors.org/docs/en/emoji-key)):

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   [![Abhishek Sharma](https://avatars0.githubusercontent.com/u/29058921?v=4){width="100px;"}~**Abhishek\ Sharma**~](https://abhisharma404.blogspot.com/)[💻](https://github.com/OWASP/SecureTea-Project/commits?author=abhisharma404 "Code") [📖](https://github.com/OWASP/SecureTea-Project/commits?author=abhisharma404 "Documentation")   [![Rejah Rehim ](https://avatars3.githubusercontent.com/u/4394746?v=4){width="100px;"}~**Rejah\ Rehim**~](https://rejahrehim.com/) [💻](https://github.com/OWASP/SecureTea-Project/commits?author=rejahrehim "Code") [📖](https://github.com/OWASP/SecureTea-Project/commits?author=rejahrehim "Documentation")   [![adeyosemanputra](https://avatars1.githubusercontent.com/u/24958168?v=4){width="100px;"}~**adeyosemanputra**~](https://github.com/adeyosemanputra)[💻](https://github.com/OWASP/SecureTea-Project/commits?author=adeyosemanputra "Code") [📖](https://github.com/OWASP/SecureTea-Project/commits?author=adeyosemanputra "Documentation")   [![Ananthu S](https://avatars0.githubusercontent.com/u/30488894?v=4){width="100px;"}~**Ananthu\ S**~](https://github.com/ananthus)[💻](https://github.com/OWASP/SecureTea-Project/commits?author=ananthus "Code")   [![Sunny Dhoke](https://avatars3.githubusercontent.com/u/30065288?v=4){width="100px;"}~**Sunny\ Dhoke**~](http://sunn-e.github.io/)[🐛](https://github.com/OWASP/SecureTea-Project/issues?q=author%3Asunn-e "Bug reports") [📖](https://github.com/OWASP/SecureTea-Project/commits?author=sunn-e "Documentation")   [![MajAK](https://avatars3.githubusercontent.com/u/29600964?v=4){width="100px;"}~**MajAK**~](https://github.com/kUSHAL0601)[💻](https://github.com/OWASP/SecureTea-Project/commits?author=kUSHAL0601 "Code")   [![Mishal Shah](https://avatars3.githubusercontent.com/u/21958074?v=4){width="100px;"}~**Mishal\ Shah**~](https://mishal23.github.io/)[💻](https://github.com/OWASP/SecureTea-Project/commits?author=mishal23 "Code")
                                                                  [![sam@ukjp](https://avatars1.githubusercontent.com/u/26642976?v=4){width="100px;"}~**sam@ukjp**~](https://sam.ukjp.app/)[💻](https://github.com/OWASP/SecureTea-Project/commits?author=sam-aldis "Code")                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This project follows the
[all-contributors](https://github.com/all-contributors/all-contributors)
specification. Contributions of any kind welcome!
:::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Latest News

\
Securetea Project Graduate as OWASP Lab Status on Thu, Sep 9, 2021. see
more at https://owasp.org/projects/ \</br\>
:::
::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-securetea/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-securetea){.github-button
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

### OWASP SecureTea Project Information

- [Lab Project](#)
- [Tool Project](#)
- [Version 2.1](#)
- [Builder](#)
- [Breaker](#)

### Downloads

- [Download](https://github.com/OWASP/SecureTea-Project/archive/master.zip)

### Code Repository

- [repo](https://github.com/OWASP/SecureTea-Project)

### Change Log

- [changes](#)

### Leaders

- [Ade
  Yoseman](../cdn-cgi/l/email-protection.html#204144450e5055545241604f574153500e4f5247)
- [Rejah
  Rehim](../cdn-cgi/l/email-protection.html#3745525d565f1945525f5e5a77584056444719584550)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::
