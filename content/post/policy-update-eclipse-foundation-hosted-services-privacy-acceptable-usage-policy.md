---
title: 'Policy Update: Eclipse Foundation Hosted Services Privacy and Acceptable Usage Policy'
author: Christopher Guindon
date: '2024-12-02T15:55:00-05:00'
draft: false
categories:
  - technology
tags:
  - eclipse
  - jakartaee
keywords:
  - Policy Update
  - Privacy Policy
  - Acceptable Usage
  - Service Operators
  - Data Protection
  - Personal Information
  - Eclipse Foundation
  - OpenID Connect
  - Website Analytics
  - Content Embedding
description: 'This update to the Eclipse Foundation Hosted Services Privacy and Acceptable Usage Policy introduces clearer guidelines for Service Operators, enhanced privacy and security measures, new analytics platform support, and reporting requirements to ensure compliance with global privacy standards.'
---

We are pleased to announce the release of Version 1.1 of the [Eclipse Foundation Hosted Services Privacy and Acceptable Usage Policy](https://www.eclipse.org/org/documents/eclipse-foundation-hosted-services-privacy-and-acceptable-usage-policy.pdf?v=1.1), effective December 2, 2024. This policy sets out the rules and responsibilities for Services Operators — individuals other than Eclipse Foundation staff managing services hosted or supported by the Eclipse Foundation — to ensure compliance  with the [Eclipse Foundation Website Privacy Policy](https://www.eclipse.org/legal/privacy/) and global privacy standards.

A service refers to any system or service hosted, funded, or supported by the Eclipse Foundation, including domains, subdomains, servers, Project and Industry Collaboration websites, sandboxes, website analytics, and third-party tools (e.g., Survey Monkey, Google Analytics, Netlify).

If you are Service Operator, we ask that you review this new policy and ensure your service is in adherence to it.


## What’s New?

1. **Clearer Privacy and Security Guidelines** \
The updated policy clarifies the responsibilities of service operators in managing personal information (PI) and ensuring compliance with global privacy regulations. This includes but not limited to:

    * Ensuring proper anonymisation of PI (e.g., IP anonymisation in Google Analytics) and deleting it when no longer needed.
    * Completing a Data Protection Impact Assessment (DPIA) to document how PI is collected, retained, and deleted.
    * Promptly reporting security breaches to the Eclipse Foundation’s Security Team at [security@eclipse-foundation.org](mailto:security@eclipse-foundation.org), with details on the nature and scope of the breach.

2. **Dedicated GitLab Project for Reporting** \
To simplify the reporting and approval processes, we’ve created a [GitLab project](https://gitlab.eclipse.org/eclipsefdn/hosted-services-privacy-and-acceptable-usage-policy) that service operators must use to:
    * Submit a [Usage Report](https://gitlab.eclipse.org/eclipsefdn/hosted-services-privacy-and-acceptable-usage-policy/-/issues/new?issuable_template=usage_report) notifying and seeking approval from the Eclipse Foundation regarding their PI collection activities.
    * Request a Client ID and Secret for those who wish to implement the [Eclipse Foundation OpenID Connect](https://gitlab.eclipse.org/eclipsefdn/hosted-services-privacy-and-acceptable-usage-policy/-/issues/new?issuable_template=eclipsefdn_openid_connect) service to enable secure logins with Eclipse accounts.

3. **New Analytics Platforms and Content Embedding Restrictions** \
The policy now includes two new supported website analytics platforms and a list of approved domains for embedding external content. The use of any other services or domains requires explicit consent from the Eclipse Foundation, which can be requested by contacting [privacy@eclipse.org](mailto:privacy@eclipse.org).

## Action Required

If you operate a service that collects Personal Information (e.g., usernames, email addresses, or other user-identifiable data), you must:

* Submit a [Usage Report](https://gitlab.eclipse.org/eclipsefdn/hosted-services-privacy-and-acceptable-usage-policy/-/issues/new?issuable_template=usage_report) to inform us of your activities.
* For new services, you must now obtain formal approval via an [issue](https://gitlab.eclipse.org/eclipsefdn/hosted-services-privacy-and-acceptable-usage-policy/-/issues/new?issuable_template=usage_report) before starting any data collection.

**Note**: This step is not required for service operators maintaining project websites that do not collect Personal Information or use any website analytics platform.

We are committed to supporting our community in meeting the highest standards for privacy, security, and transparency. For more details, please review the [updated policy](https://www.eclipse.org/org/documents/eclipse-foundation-hosted-services-privacy-and-acceptable-usage-policy.pdf?v=1.1) and don’t hesitate to contact us at [privacy@eclipse.org](mailto:privacy@eclipse.org) if you have any questions!