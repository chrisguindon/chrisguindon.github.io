---
title: "Security Incident Review: API Endpoint Exposure on accounts.eclipse.org"
linktitle: "Security Incident Review: API Endpoint Exposure on accounts.eclipse.org"
author: Christopher Guindon
date: 2025-04-09T18:31:37.245Z
categories:
  - technology
tags:
  - eclipse
keywords:
  - security incident
  - API exposure
  - JSON:API
  - Drupal 10
  - user data
  - field permissions
  - vulnerability disclosure
  - accounts.eclipse.org
  - security
---

In late March 2025, a security researcher in our community reported a security concern about a publicly accessible API endpoint containing user information on accounts.eclipse.org. After reviewing the issue, we determined this API endpoint was unnecessary and have since disabled it.

We looked through our access logs for the past few months and confirmed that the only requests were from the security researcher and the Eclipse Foundation staff who verified the report.

## Background

The incident was introduced by the Drupal core [JSON:API](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module) module being enabled in production without [recommended field access restrictions](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/security-considerations). This module exposes data such as user entities and fields based on Drupal’s default permissions. While email addresses were not visible, other custom fields were publicly accessible for some users and staff:

* City
* Province/State
* Country
* Matrix ID

We did not intend for this information to be publicly accessible by this module. While we do ask our committers to provide their full postal address, that additional information is not stored in Drupal and was not exposed.

## Timeline of Events

* **January 19, 2025**: Endpoint became accessible after going live with our Drupal 10 migration of accounts.eclipse.org
* **March 26, 2025 (08:16 AM EDT)**: Received initial security report from ethical security researcher in the [security@eclipse.org](mailto:security@eclipse.org) inbox.
* **April 3, 2025 (11:08 AM EDT)**: Security Team confirmed the issue, and notified the WebDev team.
* **April 3, 2025 (12:39 PM EDT):** Endpoint was disabled.

## Resolution and Next Steps

To resolve the issue and prevent similar incidents in the future, we have:

* Disabled Drupal's [JSON:API](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module) module from accounts.eclipse.org
* Installed and configured the [Field Permissions](https://www.drupal.org/project/field_permissions) module to enforce field-level access control.
* Initiated a full audit of all our Drupal-based sites to ensure the [JSON:API](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module) module is disabled and the [Field Permissions](https://www.drupal.org/project/field_permissions) module is enabled and properly configured.

We remain committed to continuously strengthening our security practices and protecting user data. We would like to thank security researcher [Gaurang Maheta](https://www.linkedin.com/in/gaurang883/) for promptly reporting this issue. If you have any questions or concerns, please contact us at [privacy@eclipse.org](mailto:privacy@eclipse.org) or [security@eclipse.org](mailto:security@eclipse.org).