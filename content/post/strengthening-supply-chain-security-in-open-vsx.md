
---
title: 'Strengthening supply-chain security in Open VSX'
description: 'Open VSX Registry is introducing pre-publish security checks to strengthen extension supply chain security and protect publishers and users.'
author: Christopher Guindon
date: '2026-01-27T10:00:00-04:00'
draft: false
categories:
  - technology
  - community
tags:
  - eclipse
  - jakartaee
  - supply chain security
  - developer security
  - extension registry
  - package registries
---

The [Open VSX Registry](https://open-vsx.org/) is core infrastructure in the developer supply chain, delivering extensions developers download, install, and rely on every day. As the ecosystem grows, maintaining that trust matters more than ever.

***A quick note on terminology: Eclipse Open VSX is an open source project, and the Open VSX Registry is the hosted instance of that project, operated by the Eclipse Foundation. This post focuses primarily on security improvements being rolled out in the Open VSX Registry, while much of the underlying work is happening in the Open VSX project***.

Up to now, the Open VSX Registry has relied primarily on post-publication response and investigation. When a bad extension is reported, we investigate and remove it. While this approach remains relevant and necessary, it does not scale as publication volume increases and threat models evolve.

To address this, we are taking a more proactive approach by adding security checks **before extensions are published**, rather than relying only on reports after the fact.

## Why pre-publish security checks matter

Developer tooling ecosystems, including package registries and extension marketplaces, are a popular target, and we see the same types of issues repeatedly:

* Namespace impersonation designed to mislead users
* Secrets or credentials accidentally committed and published
* Malicious or misleading extensions
* Supply-chain attacks that spread quietly over time

Relying only on after-the-fact detection leaves a growing window of exposure. Pre-publish checks help narrow that window by catching the most obvious issues earlier. Similar pre-publication and monitoring approaches are increasingly standard across large extension marketplaces as developer tooling ecosystems mature.

## How we’re approaching this work

To move faster and add specialized expertise, we are working alongside security consultants from [Yeeth Security](https://yeeth.xyz/). These experts are helping us design and implement a new verification framework, while keeping overall direction, decision-making, and long-term stewardship firmly within the Open VSX project and the Eclipse Foundation as operators of the Open VSX Registry.

Most of this work is happening in the open. We are keeping a small set of security-sensitive details private to reduce the risk of abuse or circumvention.

## What we’re building

Together, we’re introducing a new, extensible verification framework. Over time, it will enable Open VSX Registry to:

* Detect clear cases of extension name or namespace impersonation
* Flag accidentally published credentials or secrets
* Scan for known malicious patterns
* Quarantine suspicious uploads for review instead of publishing them immediately, with clear feedback provided to the publisher

If you want to follow along, the work is tracked here: \
[https://github.com/eclipse/openvsx/issues/1331](https://github.com/eclipse/openvsx/issues/1331)

This framework is designed to grow with the ecosystem, so we can add new checks as threat models evolve.

## A measured rollout

We’re approaching this effort with a focus on ecosystem health. The goal and intent is to raise the security floor, help publishers catch issues early, and keep the experience predictable and fair for good-faith publishers. Our current plan is to:

* **Begin monitoring newly published extensions in February**, without blocking publication
* Use this monitoring period to tune checks, reduce false positives, and improve feedback
* **Move toward enforcement in March**, once we’re confident the system behaves predictably and fairly

This staged rollout gives us room to get it right before it impacts publication flows.

## What publishers and users should expect

Publishers may start seeing new messages when potential issues are detected. In most cases, these are meant to be helpful nudges, not roadblocks. We also want to thank the thousands of extension publishers who already act responsibly and help make the Open VSX Registry a trusted resource for the broader developer community. The goal is to:

* Catch accidental mistakes early
* Make expectations clearer
* Reduce the likelihood that risky content reaches users

Human review will remain part of the process, especially for edge cases. We will also continue to provide clear remediation guidance in our wikis and project documentation.

For users, the outcome is straightforward. Pre-publish checks reduce the likelihood that obviously malicious or unsafe extensions make it into the ecosystem, which increases confidence in the Open VSX Registry as shared infrastructure.

## Security is ongoing work

Security isn’t a one-and-done project. It evolves alongside the ecosystem it protects. We see this work as ongoing, and we’ll continue to share what we’re doing, why we’re doing it, and what we learn along the way.

## Looking ahead

Strengthening supply-chain security is a shared responsibility. As the Open VSX Registry continues to grow, investing in proactive safeguards is essential to protecting both publishers and users.

These changes are an important step forward, and part of a longer journey. We’ll keep iterating, learning from real-world use, and adapting as the ecosystem evolves. Community feedback plays a critical role in that process, and we encourage publishers and users to share their experiences as this work rolls out.

Our goal is simple: to keep the Open VSX Registry a resource developers can depend on with confidence.

## Growing with the ecosystem

The security work outlined above is part of a broader effort to scale the Open VSX Registry responsibly as adoption continues to grow. That includes investing not just in tooling and processes, but in the people doing the work.

We’re actively expanding the Open VSX team, including roles focused on security, platform engineering, and ecosystem stewardship. If you’re interested in helping build and protect critical open source infrastructure, you can find our current openings on the [Eclipse Foundation careers](https://www.eclipse.org/careers/) page!
