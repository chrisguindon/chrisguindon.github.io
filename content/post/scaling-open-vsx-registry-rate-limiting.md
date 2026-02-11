
---
title: 'Scaling the Open VSX Registry responsibly with rate limiting'
description: 'Learn how responsible rate limiting helps keep the Open VSX Registry reliable, fair, and sustainable as AI-driven and automated usage continues to grow.'
author: Christopher Guindon
date: '2026-02-11T08:30:00-05:00'
draft: false
categories:
  - technology
  - community
tags:
  - eclipse
  - jakartaee
  - open vsx
  - open vsx registry
  - eclipse foundation
  - extension registry
  - open source infrastructure
  - developer tooling
  - rate limiting
  - infrastructure sustainability
  - ai automation
  - package registry
  - supply chain security
  - ci automation
  - cloud tooling
  - ecosystem governance
---

The [Open VSX Registry](https://open-vsx.org/) has become widely used infrastructure for modern developer tools. That growth reflects strong trust from the ecosystem, and it brings a shared responsibility to keep the Registry reliable, predictable, and equitable for everyone who depends on it.

In a [previous post](https://blogs.eclipse.org/post/christopher-guindon/strengthening-supply-chain-security-open-vsx), I shared an update on strengthening supply-chain security in the Open VSX Registry, including the introduction of pre-publish checks for extensions. This post focuses on the operational side of the same goal: ensuring the Registry remains resilient and sustainable as usage continues to grow.

## The Open VSX Registry is free to use, but not free to operate

Operating a global extension registry requires sustained investment in:

* **Compute and storage** to serve and index extensions at scale
* **Bandwidth** to deliver downloads and metadata worldwide
* **Security** to protect users, publishers, and the service itself
* **Staff** to operate, monitor, secure, and support the Registry

These costs scale directly with usage.

## AI-driven usage is scaling faster than ever

Demand on the Open VSX Registry is increasing rapidly, and AI-enabled development is accelerating that trend. A single developer can now orchestrate dozens of agents and automated workflows, generating traffic that previously would have required entire teams. In practical terms, that can mean the equivalent load of twenty or more traditional users, with direct impact on compute, bandwidth, storage, security capacity, and operational oversight.

This is not unique to the Open VSX Registry. It is an industry-wide challenge. Stewards of public package registries such as Maven Central, PyPI, crates.io, and Packagist have recently raised the same sustainability concerns in a [joint statement on sustainable stewardship](https://openssf.org/blog/2025/09/23/open-infrastructure-is-not-free-a-joint-statement-on-sustainable-stewardship/). Mike Milinkovich, Executive Director of the Eclipse Foundation, echoed that message in his [post on aligning responsibility with usage](https://blogs.eclipse.org/post/mike-milinkovich/businesses-built-open-infrastructure-have-responsibility-sustain-it).

As reliance on shared open infrastructure grows, sustaining it becomes a collective responsibility across the ecosystem.

## Open VSX is critical, and often invisible, infrastructure

Many developers and organisations may not realise how often they rely on the Open VSX Registry. It provides the extension infrastructure behind a growing number of modern developer platforms and tools, including **Amazon’s Kiro, Cursor, Google Antigravity, Windsurf, IBM’s Project Bob, Trae, **and others.

If you use one of these tools, you use the Open VSX Registry.

The Open VSX Registry remains a neutral, vendor-independent public service, operated in the open and governed by the Eclipse Foundation for the benefit of the entire ecosystem.

For developers, the expectation is simple: Open VSX should remain fast, stable, and dependable as the ecosystem grows.

As more platforms and automated systems rely on the Registry, continuous machine-driven traffic can place sustained load on shared infrastructure. Without clear operational guardrails, that can affect performance and availability for everyone.

## A practical step for sustainable and reliable operations

Usage has shifted from primarily human-driven access to continuous automation driven by CI systems, cloud-based tooling, and AI-enabled workflows. That shift requires operational controls that scale predictably.

Rate limiting provides a structured way to manage high-volume automated traffic while preserving the performance developers expect. It also ensures that operational decisions are based on real usage patterns and that expectations for large-scale consumption are clear and transparent.

Rate limits aren’t entirely new. Like most public infrastructure services, the Open VSX Registry has long had baseline protections in place to prevent sustained high-volume usage from degrading performance for everyone. What’s changing now is that we’re moving from a one-size-fits-all approach to defined tiers that more accurately reflect different usage patterns. This allows us to keep the Registry stable and responsive for developers and open source projects, while providing a clear, supported path for sustained at-scale consumption.

For individual developers and open source projects, day-to-day workflows remain unchanged. Publishing extensions, searching the registry, and installing tools will continue to work as they always have for typical usage.

## A measured, transparent rollout

Rate limiting will be introduced incrementally, with an emphasis on platform health and operational stability.

The initial phase focuses on visibility and observation before any limits are adjusted. This includes improved insight into traffic patterns for registered consumers, baseline protections for anonymous high-volume usage, and a monitoring period before any limits are adjusted.

This work is being done in the open so the community can follow what is changing and why. Progress and discussion are tracked publicly in the Open VSX deployment issue: \
[https://github.com/EclipseFdn/open-vsx.org/issues/5970](https://github.com/EclipseFdn/open-vsx.org/issues/5970)

## What this means for the community

The goal is to keep the Open VSX Registry reliable and fair as it scales, while minimizing impact on normal use.

For most users, nothing should feel different. Developers should see little to no impact, and publishers should not experience disruption to normal publishing workflows. Sustained, high-volume automated consumers may need to coordinate with the Registry to ensure their usage can be supported reliably over time.

Organisations that depend on the Open VSX Registry for sustained or commercial-scale usage are encouraged to get in touch. Coordinating early helps us plan capacity, maintain reliability, and support the broader ecosystem.  Please contact the Open VSX Registry team at **infrastructure@eclipse-foundation.org**.

The intent is not restriction, but clarity in support of fairness, stability, and long-term sustainability.

## Looking ahead

Automation is reshaping how developer infrastructure is consumed. Responsible rate limiting is one step toward ensuring the Open VSX Registry can continue to serve the ecosystem reliably as those patterns evolve.

We will continue to adapt based on real-world usage and community input, with the goal of keeping the Open VSX Registry a dependable shared resource for the long term.