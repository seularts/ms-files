:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Deployment](#div-deployment){#deployment-link .tab-link role="tab"
  aria-selected="false" aria-controls="deployment"}

# OWASP WinFIM.NET {#owasp-winfim.net .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
# WinFIM.NET {#winfimnet}

WinFIM.NET - File Integrity Monitoring For Windows

**#Introduction** There are plenty of commercial tools to do file
integrity monitoring (FIM). But, for freeware / Open Source, especially
for Windows, it seems not much options.

A small Windows Service named
["WinFIM.NET"](https://github.com/OWASP/www-project-winfim.net) was
developed trying to fill up this gap.

**#characteristics** The characteristics of this small application are:

It will identify add / remove / modify of files and directories

Monitoring scope could be easily customized

Path exclusion (e.g. sub-directory) could be configured

File extension exclusion could be configured (e.g. \*.bak, \*.tmp,
\*.log, \*.mdf, \*.ldf, \*.xel, \*. installlog)

All the events are saved as native Windows Events, which could easily
integrate with users' existing log management mechanism (e.g. Windows
Event Subscription, Winlogbeat , nxlog, etc.)

Deployment friendly

Using SHA256 for hashing

**#Installation (single machine)**

1\) Manual download all files to destination computer

2\) Configure the parameters to fill your own environment

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
a) ‘monlist.txt‘ – put your in-scope monitoring files / directories (Absolute path) line by line under this file<br>
b) ‘exclude_path.txt‘ – put your exclusion (Absolute path) line by line under this file (the exclusion should be overlapped with the paths in ‘monlist.txt’ (e.g. Sub-directory of the in-scope directory)<br>
c) ‘exclude_extension.txt‘ – put all whitelisted file extension (normally, those extensions should be related to some frequent changing files, e.g. *.log, *.tmp)<br>
d) ‘scheduler.txt‘ – This file is to control whether the WinFIM.NET will be run in schedule mode or continuous mode.<br>
  -  Put a number ‘0’ to the file, if you want the WinFIM.NET keep running.
  -  Put a number (in minute) for the time separation of each run. e.g. 30 (that means file checksum will be run every 30 minutes).
```
:::
::::

3\) Unblock the "WinFIM.NET Service.exe"

4\) Install the Windows Service - Bring up an Administrator command
prompt and navigate to the deployed folder, then execute
"install_service.bat"

5\) Verify if the Windows Service is up and running

6\) Please make sure maximum log size is configured according to your
deployment environment. By default, it only reserves around 1MB for
it. - %SystemRoot%\\System32\\Winevt\\Logs\\WinFIM.NET.evtx

**#Uninstallation** Bring up an Administrator command prompt and
navigate to the deployed folder, then execute "uninstall_service.bat"

**#Windows Event ID for file / directory changes**

Event ID 7776 -- File / Directory creation

Event ID 7777 -- File modification

Event ID 7778 -- File / Directory deletion

\
Enjoy!

Cheers\
Henry
:::::

::: {#sec-deployment .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Deployment Illustration

For detail introduction, please visit my [Cyber Security
Corner](https://redblueteam.wordpress.com/2020/03/11/winfim-net-windows-file-integrity-monitoring/)
technical blog.
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-winfim.net/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-winfim.net){.github-button
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

### WinFIM.NET Information {#winfimnet-information}

WinFIM.NET - File Integrity Monitoring For Windows

There are plenty of commercial tools to do file integrity monitoring
(FIM). But, for freeware / Open Source, especially for Windows, it seems
not much options.

A small Windows Service named
["WinFIM.NET"](https://github.com/OWASP/www-project-winfim.net) was
developed trying to fill up this gap.

### Downloads or Social Links

- Developer's blog: <https://redblueteam.wordpress.com/>

### Change Log

#### 2022-10-26 v1.2.0 {#2022-10-26-v120}

- on initial run, do not warn if base paths are not detected

- Bumped assembly to 1.2.0.0, setup project and docker image versions to
  1.2.0

- New switch: is_log_to_windows_eventlog - default value is true

- New switch: is_capture_remote_connection_status - default value is
  false

- check directory owner

- Performance improvement - only checks file ownership once per cycle

- log to file uses JSON formatter by default

- Updated nuget packages

- Cleared issues found by Resharper

- logs a max of 32768 characters to windows event log per reported bug

#### 2020-03-11 [Initial release](https://redblueteam.wordpress.com/2020/03/11/winfim-net-windows-file-integrity-monitoring/). {#2020-03-11-initial-release}

### Leaders

- [Henry
  Hon](../cdn-cgi/l/email-protection.html#3159545f43481f595e5f715e465042411f5e4356)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
