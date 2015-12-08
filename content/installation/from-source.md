---
layout: bt_wiki
title: Installing from sources
category: Installation
draft: false
weight: 500

---

Installing Cloudify from sources is possible from two locations: PyPi and GitHub.

{{% gsNote title="Advanced Section" %}}
This way of installation is intended for advanced users or developers.
Installation from source requires an environment with compilers since some of Cloudify's
dependencies are not pure Python modules.
Familiarity with tools such as [Virtualenv](https://virtualenv.readthedocs.org/en/latest/) & [Pip](https://pip.pypa.io/en/stable/) is recommended.
{{% /gsNote %}}

## Installation Prerequisites
For all users the following components are required:
* [Python 2.7.X](https://www.python.org/downloads/)
* [pip](https://pip.pypa.io/en/stable/installing/)
* [virtualenv](https://virtualenv.readthedocs.org/en/latest/installation.html)

### For Windows users
* [Microsoft Visual C++ Compiler for Python 2.7](https://www.microsoft.com/en-us/download/details.aspx?id=44266)

### For Linux users
* Python development headers (`python-dev` in Ubuntu or `python-devel` in CentOS)
* C compiler (`gcc`)

### For OS X users
* [Xcode Command Line Tools](https://developer.apple.com/library/ios/technotes/tn2339/_index.html#//apple_ref/doc/uid/DTS40014588-CH1-DOWNLOADING_COMMAND_LINE_TOOLS_IS_NOT_AVAILABLE_IN_XCODE_FOR_OS_X_10_9__HOW_CAN_I_INSTALL_THEM_ON_MY_MACHINE_)

## Installing from GitHub

Cloudify uses GitHub as it's main online source code repository.

Installing latest stable version from GitHub can be done by running the following
commands in terminal:
{{< gsHighlight bash >}}
$ CFY_VERSION="3.3" \
  pip install "https://github.com/cloudify-cosmo/cloudify-cli/archive/$CFY_VERSION.zip" \
  --requirement "https://raw.githubusercontent.com/cloudify-cosmo/cloudify-cli/$CFY_VERSION/dev-requirements.txt"
{{< /gsHighlight >}}

Installing latest bleeding edge release can be done in the similar manner:
{{< gsHighlight bash >}}
$ CFY_VERSION="master"
$ pip install "https://github.com/cloudify-cosmo/cloudify-cli/archive/$CFY_VERSION.zip" \
  --requirement "https://raw.githubusercontent.com/cloudify-cosmo/cloudify-cli/$CFY_VERSION/dev-requirements.txt"
{{< /gsHighlight >}}

You can set `CFY_VERSION` variable to any desired version from [version list](https://github.com/cloudify-cosmo/cloudify-cli/tags).

## Installing from PyPi

PyPi is the official repository for 3rd party Python modules. Cloudify uploads
its Python artifacts to PyPi.

Installation the latest release from PyPi is done by running the following commands in terminal:
{{< gsHighlight bash >}}
$ pip install cloudify
{{< /gsHighlight >}}

It's also possible to request specific version:
{{< gsHighlight bash >}}
$ pip install cloudify==3.3
{{< /gsHighlight >}}

PyPi contains the same [releases](https://github.com/cloudify-cosmo/cloudify-cli/tags) that you can find on GitHub, however naming convention
is a bit different, for example, to get 3.3m6 from PyPi, you'll need to request
`cloudify==3.3a6`.

Full list of PyPi versions is [available here](https://pypi.python.org/pypi/cloudify/json)
