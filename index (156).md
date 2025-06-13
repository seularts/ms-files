::::::::::::::::::::::::::::::::::::::::::::::::::::::: main-wrapper
# OWASP dep-scan {#owasp-dep-scan .page-title}

:::::::::::::::::::::::::::::::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::::::::::::::::::::::::::::::::::::::::::: {#sec-main .section .page-body}
# Introduction

OWASP dep-scan is a next-generation security and risk audit tool based
on known vulnerabilities, advisories, and license limitations for
project dependencies. Both local repositories and container images are
supported as the input, and the tool is ideal for integration with
ASPM/VM platforms and in CI environments.

![Depscan logo](dep-scan.png)

## Features

- Scan most application code - local repos, Linux container images,
  Kubernetes manifests, and OS - to identify known CVEs with
  prioritization
- Perform advanced reachability analysis for multiple languages (See
  reachability analysis)
- Package vulnerability scanning is performed locally and is quite fast.
  No server is used!
- Generate Software Bill-of-Materials (SBOM) with Vulnerability
  Disclosure Report (VDR) information
- Generate a Common Security Advisory Framework (CSAF) 2.0 VEX document
  (check out the [CSAF
  Readme](https://github.com/owasp-dep-scan/dep-scan/blob/master/contrib/CSAF_README.md))
- Perform deep packages risk audit for dependency confusion attacks and
  maintenance risks (See risk audit)

![Reachable Flows](assets/images/depscan-flows.png)

![CVE Insights](assets/images/depscan-blog/6.jpg)

### Vulnerability Data sources

- OSV
- NVD
- GitHub
- NPM
- Linux [vuln-list](https://github.com/appthreat/vuln-list) (Use
  `--cache-os`{.language-plaintext .highlighter-rouge})

### Linux distros

- AlmaLinux
- Debian
- Alpine
- Amazon Linux
- Arch Linux
- RHEL/CentOS
- Rocky Linux
- Ubuntu
- OpenSUSE/SLES
- Photon
- Chainguard
- Wolfi OS

Application vulnerabilities would be reported for all Linux distros and
Windows. To download the full vulnerability database suitable for
scanning OS, invoke dep-scan with `--cache-os`{.language-plaintext
.highlighter-rouge} for the first time. dep-scan would also download the
appropriate database based on project type automatically.

## Usage

dep-scan is ideal for use during continuous integration (CI) and as a
local development tool.

### OCI Artifacts via ORAS cli

Use [ORAS cli](https://oras.land/docs/installation/) to download the
dep-scan binary and the vulnerability database for effortless
integration. Example workflow is
[here](https://github.com/appthreat/images-info/blob/main/.github/workflows/build.yml#L13).

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
export VDB_HOME=depscan
mkdir -p $VDB_HOME
oras pull ghcr.io/appthreat/vdb:v5 -o $VDB_HOME
oras pull ghcr.io/appthreat/depscan:v4 -o $VDB_HOME
```
:::
::::

### Server mode

dep-scan and cdxgen could be run in server mode. Use the included docker
compose file to get started.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
git clone https://github.com/owasp-dep-scan/dep-scan
docker compose up
```
:::
::::

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
depscan --server --server-host 0.0.0.0 --server-port 7070
```
:::
::::

In server mode, use `/cache`{.language-plaintext .highlighter-rouge}
endpoint to cache the vulnerability database.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
# This would take over 5 minutes
curl http://0.0.0.0:7070/cache
```
:::
::::

Use the `/scan`{.language-plaintext .highlighter-rouge} endpoint to
perform scans.

> \[!NOTE\] The `type`{.language-plaintext .highlighter-rouge} parameter
> is mandatory in server mode.

- Scanning a local directory.

  :::: {.language-bash .highlighter-rouge}
  ::: highlight
  ``` highlight
  curl --json '{"path": "/tmp/vulnerable-aws-koa-app", "type": "js"}' http://0.0.0.0:7070/scan
  ```
  :::
  ::::
- Scanning an SBOM file (present locally).

  :::: {.language-bash .highlighter-rouge}
  ::: highlight
  ``` highlight
  curl --json '{"path": "/tmp/vulnerable-aws-koa-app/sbom_file.json", "type": "js"}' http://0.0.0.0:7070/scan
  ```
  :::
  ::::
- Scanning a GitHub repo.

  :::: {.language-bash .highlighter-rouge}
  ::: highlight
  ``` highlight
  curl --json '{"url": "https://github.com/HooliCorp/vulnerable-aws-koa-app", "type": "js"}' http://0.0.0.0:7070/scan -o app.vdr.json
  ```
  :::
  ::::
- Uploading an SBOM file and generating results based on it.

  :::: {.language-bash .highlighter-rouge}
  ::: highlight
  ``` highlight
  curl -X POST -H 'Content-Type: multipart/form-data' -F 'file=@/tmp/app/sbom_file.json' http://0.0.0.0:7070/scan?type=js
  ```
  :::
  ::::

### Scanning projects locally (Python version)

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
sudo npm install -g @cyclonedx/cdxgen
pip install owasp-depscan
```
:::
::::

This would install two commands called `cdxgen`{.language-plaintext
.highlighter-rouge} and `depscan`{.language-plaintext
.highlighter-rouge}.

You can invoke the scan command directly with the various options.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
cd <project to scan>
depscan --src $PWD --reports-dir $PWD/reports
```
:::
::::

The full list of options is below:

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
usage: cli.py [-h] [--no-banner] [--cache] [--csaf] [--sync] [--profile {appsec,research,operational,threat-modeling,license-compliance,generic}] [--no-suggest] [--risk-audit] [--private-ns PRIVATE_NS] [-t PROJECT_TYPE] [--bom BOM] [-i SRC_DIR_IMAGE] [-o REPORT_FILE]
              [--reports-dir REPORTS_DIR] [--deep] [--no-universal] [--no-vuln-table] [--threatdb-server THREATDB_SERVER] [--threatdb-username THREATDB_USERNAME] [--threatdb-password THREATDB_PASSWORD] [--threatdb-token THREATDB_TOKEN] [--server]
              [--server-host SERVER_HOST] [--server-port SERVER_PORT] [--cdxgen-server CDXGEN_SERVER] [--debug] [--explain] [--reachables-slices-file REACHABLES_SLICES_FILE] [-v]

Fully open-source security and license audit for application dependencies and container images based on known vulnerabilities and advisories.

options:
  -h, --help            show this help message and exit
  --no-banner           Do not display banner
  --cache               Cache vulnerability information in platform specific user_data_dir
  --csaf                Generate a OASIS CSAF VEX document
  --sync                Sync to receive the latest vulnerability data. Should have invoked cache first.
  --profile {appsec,research,operational,threat-modeling,license-compliance,generic}
                        Profile to use while generating the BOM.
  --no-suggest          Disable suggest mode
  --risk-audit          Perform package risk audit (slow operation). Npm only.
  --private-ns PRIVATE_NS
                        Private namespace to use while performing oss risk audit. Private packages should not be available in public registries by default. Comma separated values accepted.
  -t PROJECT_TYPE, --type PROJECT_TYPE
                        Override project type if auto-detection is incorrect
  --bom BOM             Examine using the given Software Bill-of-Materials (SBOM) file in CycloneDX format. Use cdxgen command to produce one.
  -i SRC_DIR_IMAGE, --src SRC_DIR_IMAGE
                        Source directory or container image or binary file
  -o REPORT_FILE, --report_file REPORT_FILE
                        DEPRECATED. Use reports directory since multiple files are created. Report filename with directory
  --reports-dir REPORTS_DIR
                        Reports directory
  --deep                Perform deep scan by passing this --deep argument to cdxgen. Useful while scanning docker images and OS packages.
  --no-universal        Depscan would attempt to perform a single universal scan instead of individual scans per language type.
  --no-vuln-table       Do not print the table with the full list of vulnerabilities. This can help reduce console output.
  --threatdb-server THREATDB_SERVER
                        ThreatDB server url. Eg: https://api.sbom.cx
  --threatdb-username THREATDB_USERNAME
                        ThreatDB username
  --threatdb-password THREATDB_PASSWORD
                        ThreatDB password
  --threatdb-token THREATDB_TOKEN
                        ThreatDB token for token based submission
  --server              Run depscan as a server
  --server-host SERVER_HOST
                        depscan server host
  --server-port SERVER_PORT
                        depscan server port
  --cdxgen-server CDXGEN_SERVER
                        cdxgen server url. Eg: http://cdxgen:9090
  --debug               Run depscan in debug mode.
  --explain             Makes depscan to explain the various analysis. Useful for creating detailed reports.
  --reachables-slices-file REACHABLES_SLICES_FILE
                        Path for the reachables slices file created by atom.
  -v, --version         Display the version
```
:::
::::

### Scanning containers locally (Python version)

Scan `latest`{.language-plaintext .highlighter-rouge} tag of the
container `shiftleft/scan-slim`{.language-plaintext .highlighter-rouge}

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
depscan --cache --src shiftleft/scan-slim -o containertests/depscan-scan.json -t docker
```
:::
::::

Include `license`{.language-plaintext .highlighter-rouge} to the type to
perform license audit.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
depscan --cache --src shiftleft/scan-slim -o containertests/depscan-scan.json -t docker,license
```
:::
::::

You can also specify the image using the sha256 digest

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
depscan --src redmine@sha256:a5c5f8a64a0d9a436a0a6941bc3fb156be0c89996add834fe33b66ebeed2439e -o containertests/depscan-redmine.json -t docker
```
:::
::::

You can also save container images using docker or podman save command
and pass the archive to depscan for scanning.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
docker save -o /tmp/scanslim.tar shiftleft/scan-slim:latest
# podman save --format oci-archive -o /tmp/scanslim.tar shiftleft/scan-slim:latest
depscan --src /tmp/scanslim.tar -o reports/depscan-scan.json -t docker
```
:::
::::

Refer to the docker tests under GitHub action workflow for this repo for
more examples.

### Scanning projects locally (Docker container)

`ghcr.io/appthreat/dep-scan`{.language-plaintext .highlighter-rouge} or
`public.ecr.aws/appthreat/dep-scan:latest`{.language-plaintext
.highlighter-rouge} container image can be used to perform the scan.

To scan with default settings

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
docker run --rm -v $PWD:/app ghcr.io/appthreat/dep-scan --src /app --reports-dir /app/reports
```
:::
::::

Using AWS public ECR image

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
docker run --rm -v $PWD:/app public.ecr.aws/appthreat/dep-scan --src /app --reports-dir /app/reports
```
:::
::::

To scan with custom environment variables based configuration

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
docker run --rm \
    -e VDB_HOME=/db \
    -e NVD_START_YEAR=2010 \
    -e GITHUB_PAGE_COUNT=5 \
    -e GITHUB_TOKEN=<token> \
    -v /tmp:/db \
    -v $PWD:/app ghcr.io/appthreat/dep-scan --src /app --reports-dir /app/reports
```
:::
::::

In the above example, `/tmp`{.language-plaintext .highlighter-rouge} is
mounted as `/db`{.language-plaintext .highlighter-rouge} into the
container. This directory is then specified as
`VDB_HOME`{.language-plaintext .highlighter-rouge} for caching the
vulnerability information. This way the database can be cached and
reused to improve performance.

## Supported languages and package format

dep-scan uses [cdxgen](https://github.com/CycloneDX/cdxgen) command
internally to create Software Bill-of-Materials (SBoM) file for the
project. This is then used for performing the scans.

The following projects and package-dependency format is supported by
cdxgen.

  Language                   Package format
  -------------------------- -------------------------------------------------------------------------------------------
  node.js                    package-lock.json, pnpm-lock.yaml, yarn.lock, rush.js, bower.json, .min.js
  java                       maven (pom.xml \[1\]), gradle (build.gradle, .kts), scala (sbt), bazel
  php                        composer.lock
  python                     setup.py, requirements.txt \[2\], Pipfile.lock, poetry.lock, bdist_wheel, .whl, .egg-info
  go                         binary, go.mod, go.sum, Gopkg.lock
  ruby                       Gemfile.lock, gemspec
  rust                       binary, Cargo.toml, Cargo.lock
  .Net                       .csproj, packages.config, project.assets.json \[3\], packages.lock.json, .nupkg
  dart                       pubspec.lock, pubspec.yaml
  haskell                    cabal.project.freeze
  elixir                     mix.lock
  c/c++                      conan.lock, conanfile.txt
  clojure                    Clojure CLI (deps.edn), Leiningen (project.clj)
  docker / oci image         All supported languages and Linux OS packages
  GitHub Actions Workflows   .github/workflows/\*.yml
  Jenkins Plugins            .hpi files
  YAML manifests             docker-compose, kubernetes, kustomization, skaffold, tekton etc

**NOTE**

The docker image for dep-scan currently doesn't bundle suitable java and
maven commands required for bom generation. To workaround this
limitation, you can -

1.  Use python-based execution from a VM containing the correct versions
    for java, maven and gradle.
2.  Generate the bom file by invoking `cdxgen`{.language-plaintext
    .highlighter-rouge} command locally and subsequently passing this to
    `dep-scan`{.language-plaintext .highlighter-rouge} via the
    `--bom`{.language-plaintext .highlighter-rouge} argument.

## Reachability analysis

Depscan can perform reachability analysis for Java, JavaScript,
TypeScript and Python with built-in support for parsing
[atom](https://github.com/AppThreat/atom) reachables slicing. Simply
invoke depscan with the `research`{.language-plaintext
.highlighter-rouge} profile and language type to enable this feature.

To receive a verbose output including the reachable flows, pass the
argument `--explain`{.language-plaintext .highlighter-rouge}

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
--profile research -t language [--explain]
```
:::
::::

### Example analysis for a Java project

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
depscan --profile research -t java -i <source directory> --reports-dir <reports directory> --explain
```
:::
::::

### Example analysis for a JavaScript project

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
depscan --profile research -t js -i <source directory> --reports-dir <reports directory> --explain
```
:::
::::

## Customization through environment variables

The following environment variables can be used to customise the
behaviour.

- VDB_HOME - Directory to use for caching database. For docker based
  execution, this directory should get mounted as a volume from the host
- NVD_START_YEAR - Default: 2018. Supports upto 2002
- GITHUB_PAGE_COUNT - Default: 2. Supports upto 20

## GitHub Security Advisory

To download security advisories from GitHub, a personal access token
with the following scope is necessary.

- read:packages

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
export GITHUB_TOKEN="<PAT token>"
```
:::
::::

## Suggest mode

Fix version for each vulnerability is retrieved from the sources.
Sometimes, there might be known vulnerabilities in the fix version
reported. Eg: in the below screenshot the fix versions suggested for
jackson-databind might contain known vulnerabilities.

![Normal mode](assets/images/depscan-normal.png)

By passing an argument `--suggest`{.language-plaintext
.highlighter-rouge} it is possible to force depscan to recheck the fix
suggestions. This way the suggestion becomes more optimal for a given
package group.

![Suggest mode](assets/images/depscan-suggest.png)

Notice, how the new suggested version is `2.9.10.5`{.language-plaintext
.highlighter-rouge} which is an optimal fix version. Please note that
the optimal fix version may not be the appropriate version for your
application based on compatibility.

## Package Risk audit

`--risk-audit`{.language-plaintext .highlighter-rouge} argument enables
package risk audit. Currently, only npm and pypi packages are supported
in this mode. A number of risk factors are identified and assigned
weights to compute a final risk score. Packages that then exceed a
maximum risk score (`config.pkg_max_risk_score`{.language-plaintext
.highlighter-rouge}) are presented in a table.

Use `--private-ns`{.language-plaintext .highlighter-rouge} to specify
the private package namespace that should be checked for dependency
confusion type issues where a private package is available on public
npm/pypi registry.

For example, to check if private packages with namespaces \@appthreat
and \@shiftleft are not accidentally made public, use the below
argument.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
--private-ns appthreat,shiftleft
```
:::
::::

  Risk category                    Default Weight   Reason
  -------------------------------- ---------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  pkg_private_on_public_registry   4                Private package is available on a public registry
  pkg_min_versions                 2                Packages with less than 3 versions represent an extreme where they could be either super stable or quite recent. Special heuristics are applied to ignore older stable packages
  mod_create_min_seconds           1                Less than 12 hours difference between modified and creation time. This indicates that the upload had a defect that had to be rectified immediately. Sometimes, such a rapid update could also be malicious
  latest_now_min_seconds           0.5              Less than 12 hours difference between the latest version and the current time. Depending on the package such a latest version may or may not be desirable
  latest_now_max_seconds           0.5              Package versions that are over 6 years old are in use. Such packages might have vulnerable dependencies that are known or yet to be found
  pkg_min_maintainers              2                Package has less than 2 maintainers. Many opensource projects have only 1 or 2 maintainers so special heuristics are used to ignore older stable packages
  pkg_min_users                    0.25             Package has less than 2 npm users
  pkg_install_scripts              2                Package runs a custom pre or post installation scripts. This is often malicious and a downside of npm.
  pkg_node_version                 0.5              Package supports outdated version of node such as 0.8, 0.10, 4 or 6.x. Such projects might have prototype pollution or closure related vulnerabilities
  pkg_scope                        4 or 0.5         Packages that are used directly in the application (required scope) gets a score with a weight of 4. Optional packages get a score of 0.25
  deprecated                       1                Latest version is deprecated

Refer to `pkg_query.py::get_category_score`{.language-plaintext
.highlighter-rouge} method for the risk formula.

### Automatic adjustment

A parameter called `created_now_quarantine_seconds`{.language-plaintext
.highlighter-rouge} is used to identify packages that are safely past
the quarantine period (1 year). Certain risks such as
`pkg_min_versions`{.language-plaintext .highlighter-rouge} and
`pkg_min_maintainers`{.language-plaintext .highlighter-rouge} are
suppressed for packages past the quarantine period. This adjustment
helps reduce noise since it is unlikely that a malicious package can
exist in a registry unnoticed for over a year.

### Configuring weights

All parameters can be customized by using environment variables. For eg:

export PKG_MIN_VERSIONS=4 to increase and set the minimum versions
category to 4.

## Live OS scan

By passing `-t os`{.language-plaintext .highlighter-rouge}, depscan can
generate an SBoM for a live operating system or a VM with OS packages
and kernel information. Optionally, pass the argument
`--deep`{.language-plaintext .highlighter-rouge} to generate an SBoM
with both OS and application packages and to check for application
vulnerabilities.

All OS packages.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
depscan -t os -i . -o reports/depscan.json
```
:::
::::

All OS and application packages.

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
depscan -t os --deep -i . -o reports/depscan.json
```
:::
::::

## License scan

dep-scan can scan the dependencies for any license limitations and
report them directly on the console log. To enable license scanning set
the environment variable `FETCH_LICENSE`{.language-plaintext
.highlighter-rouge} to `true`{.language-plaintext .highlighter-rouge}.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
export FETCH_LICENSE=true
```
:::
::::

The license data is sourced from choosealicense.com and is quite
limited. If the license of a given package cannot be reliably matched
against this list it will get silently ignored to reduce any noise. This
behavior could change in the future once the detection logic gets
improved.

![License scan](assets/images/license-scan.png)

## Kubernetes and Cloud apps

dep-scan could auto-detect most cloud applications and Kubernetes
manifest files. Pass the argument `-t yaml-manifest`{.language-plaintext
.highlighter-rouge} to manually specify the type.

## PDF reports

Ensure [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html) is
installed or use the official container image to generate pdf reports.
Use with `--explain`{.language-plaintext .highlighter-rouge} for more
detailed reports.

## Discord support

The developers could be reached via the
[discord](https://discord.gg/DCNxzaeUpd) channel.

## Media

![Prioritized Results](assets/images/depscan-blog/1.jpg)

![Reachable Flows with Explanation](assets/images/depscan-blog/2.jpg)

![Automatic Tagging](assets/images/depscan-blog/3.jpg)

![Semantic Analysis](assets/images/depscan-blog/4.jpg)

![Polyglot tagging](assets/images/depscan-blog/5.jpg)

![CVE Insights](assets/images/depscan-blog/6.jpg)

![Recommendation](assets/images/depscan-blog/7.jpg)
:::::::::::::::::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-dep-scan/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-dep-scan){.github-button
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

![Builders](assets/images/owasp_builders_small.png)
![Breakers](assets/images/owasp_breakers_small.png)

![Tool Project](assets/images/owasp_tool_project.png)

MIT License

## Overview

Welcome to the home of the OWASP dep-scan project! dep-scan is a
next-generation security and risk audit tool based on known
vulnerabilities, advisories, and license limitations for project
dependencies. Both local repositories and container images are supported
as the input, and the tool is ideal for integration with ASPM/VM
platforms and in CI environments.

## External Resources

- [GitHub](https://github.com/owasp-dep-scan/dep-scan)
- [Downloads](https://github.com/owasp-dep-scan/dep-scan/releases)
- [Container
  Image](https://github.com/owasp-dep-scan/dep-scan/pkgs/container/depscan/154272305?tag=latest)
- [Issues](https://github.com/owasp-dep-scan/dep-scan/issues)

### Leaders

- [Prabhu
  Subramanian](../cdn-cgi/l/email-protection.html#f8888a999a908dd68b8d9a8a99959996919996b8978f998b88d6978a9f)
- [Caroline
  Russell](../cdn-cgi/l/email-protection.html#f09391829f9c999e95de82858383959c9cb09f87918380de9f8297)
- [Tim
  Messing](../cdn-cgi/l/email-protection.html#a0d4c9cd8ecdc5d3d3c9cec7e0cfd7c1d3d08ecfd2c7)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::::::::::::::::::::::::::::::::::::::
