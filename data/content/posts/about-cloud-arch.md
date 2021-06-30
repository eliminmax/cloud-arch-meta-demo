+++
title = "About Cloud Architecture"
date = "2021-06-26"
author = "Eli Array Minkoff"
authorTwitter = "" #do not include @
cover = ""
tags = ["cloud", "cloud-arch","meta","this-is-the-only-post-on-this-site"]
keywords = ["cloud", "architecture"]
description = "A self-demonstrating introduction"
showFullContent = false
+++

# Cloud Architecture - what it is, and how to use it

Cloud Architecture

Many similar explanations of cloud architecture and related concepts are out there, but the most succinct comes from a pair of articles from Red Hat.
[What is cloud infrastructure?](https://www.redhat.com/en/topics/cloud-computing/what-is-cloud-infrastructure)
> Cloud infrastructure is a term used to describe the components needed for cloud computing, which includes hardware, abstracted resources, storage, and network resources. **Think of cloud infrastructure as the tools needed to build a cloud.** In order to host services and applications in the cloud, you need cloud infrastructure.
*(emphasis mine)*
[What is cloud architecture?](https://www.redhat.com/en/topics/cloud-computing/what-is-cloud-architecture)
> Imagine you're building a house: Cloud infrastructure incorporates all the materials, while cloud architecture is the blueprint.

Cloud architecture can include any of the following:
* database software
* virtual servers
* hosting services
* web server hardware
* server operating systems
* monitoring tools
* network infrastructure.

## This Web Page

A concrete example is this web page. I will go over the tools used to make it, and the infrastructure used to serve it:

### Making this page:

This web page was made on [Pop!_OS](https://pop.system76.com/) using [hugo](https://gohugo.io), with the [Terminal](https://github.com/panr/hugo-theme-terminal/) theme. I wrote it as a markdown file, and by the time you're reading this, it was exported to HTML+CSS. It is hosted on three different servers, each of which uses a different software stack.

[https://self.cloud-arch.earrayminkoff.tech](https://self.cloud-arch.earrayminkoff.tech) - Raspberry Pi 3b in my home living room, running Ubuntu 20.04 LTS, and the Caddy web server

[https://aws.cloud-arch.earrayminkoff.tech](https://aws.cloud-arch.earrayminkoff.tech) - Amazon Web Services Electronic Compute Cloud instance running Amazon Linux 2, and the Apache web server

[https://azure.cloud-arch.earrayminkoff.tech](https://azure.cloud-arch.earrayminkoff.tech) - Microsoft Azure Virtual Machine running Debian GNU/Linux 10, and the nginx web server

All three use [Cloudflare DNS](https://www.cloudflare.com/dns/) in combination with [DuckDNS](https://duckdns.org) to dynamically update the IP addresses associated with the domain names, and they all use [Certbot](https://www.cloudflare.com/dns/) to obtain SSL certificates from [LetsEncrypt](https://www.cloudflare.com/dns/).
