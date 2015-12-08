---
layout: bt_wiki
title: Installing from sources
category: Installation
draft: false
weight: 500

---

Installing Cloudify from sources is possible from two locations: PyPi and GitHub.

{{% gsNote title="Installation Prerequisites" %}}
Installation from sources
{{% /gsNote %}}


## Installing from PyPi

## Installing from GitHub

Install latest stable version from GitHub can be done by running the following commands in the terminal:
{{< gsHighlight bash >}}
$ CFY_VERSION="3.3"
$ pip install "https://github.com/cloudify-cosmo/cloudify-cli/archive/$CFY_VERSION.zip" \
  --requirement "https://raw.githubusercontent.com/cloudify-cosmo/cloudify-cli/$CFY_VERSION/dev-requirements.txt"
{{< /gsHighlight >}}

Installing latest bleeding edge release can be done in the similar manner:
{{< gsHighlight bash >}}
$ CFY_VERSION="master"
$ pip install "https://github.com/cloudify-cosmo/cloudify-cli/archive/$CFY_VERSION.zip" \
  --requirement "https://raw.githubusercontent.com/cloudify-cosmo/cloudify-cli/$CFY_VERSION/dev-requirements.txt"
{{< /gsHighlight >}}

You can set `CFY_VERSION` variable to any desired version from [version list](https://github.com/cloudify-cosmo/cloudify-cli/tags).
