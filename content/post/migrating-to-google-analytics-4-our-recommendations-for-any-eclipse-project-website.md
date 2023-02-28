---
title: "Migrating to Google Analytics 4: Our Recommendations for Any Eclipse
  Project Website"
linktitle: "Migrating to Google Analytics 4: Our Recommendations for Any Eclipse
  Project Website"
author: Christopher Guindon
date: 2023-02-28T18:43:40.731Z
draft: true
tags:
  - eclipse
keywords:
  - GoogleAnalytics4
  - GA4migration
---
As part of our commitment to providing the best possible service to our community, we would like to take a moment to share some recommendations regarding the use of Google Analytics (GA) for Eclipse project websites.

As you may be aware, [Google Analytics 4 is being rolled out as a replacement for Universal Analytics](https://support.google.com/analytics/answer/11583528?hl=en). While Universal Analytics is still supported at this time, Google has announced that they will stop processing new hits for all standard Universal Analytics properties on July 1, 2023.

Therefore, we strongly recommend that all projects currently using GA take some time to re-evaluate whether it is still necessary for their needs. If the data provided by GA is no longer useful or necessary, we recommend that projects remove GA from their website.

If it is determined that the data is still relevant and useful for the project, we recommend that it be migrated to Google Analytics 4 manually. Google has provided a [migration guide](https://support.google.com/analytics/answer/10759417?hl=en) for those who are looking to upgrade.

We believe this is the safest way for projects to confirm that all is well, as we cannot assume that the automatic GA migration will work as expected for everyone. Also, it’s the only way for projects to ensure that explicit consent has been given by the user via our cookie consent banner before enabling GA.

As a reminder, it’s possible to add our cookie consent banner to any website by adding the following code snippet in the <head></head> section of each page:

> <link rel="stylesheet" type="text/css" href="//www.eclipse.org/eclipse.org-common/themes/solstice/public/stylesheets/vendor/cookieconsent/cookieconsent.min.css" />
>
> <script src="//www.eclipse.org/eclipse.org-common/themes/solstice/public/javascript/vendor/cookieconsent/default.min.js"></script> 

A project website with GA must then ensure that the value of the **eclipse_cookieconsent_status** cookie is set to **“allow”** before loading GA on a webpage.

Additionally, we recommend that projects [opt-out](https://support.google.com/analytics/answer/12938611) from letting GA make any changes to their account. This will ensure that projects have full control over their upgrade and can manage it in a way that best suits their needs.

Upgrading to GA 4 will not only provide access to new features and benefits but will also ensure that project websites are prepared for the future of Google Analytics before the end of support for Universal Analytics.

As always, we are here to support you with any questions or concerns you may have. Please do not hesitate to reach out to us via issue #2630 in our [Helpdesk](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/2630).

You can also find additional information and requirements around the acceptable usage of GA for Eclipse projects in our [Eclipse Foundation Hosted Services Privacy and Acceptable Usage Policy](https://www.eclipse.org/org/documents/eclipse-foundation-hosted-services-privacy-and-acceptable-usage-policy.pdf).