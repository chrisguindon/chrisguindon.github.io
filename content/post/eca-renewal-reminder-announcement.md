---
title: "Improving ECA Renewals with Automated Notifications"
author: Christopher Guindon
date: '2025-06-10T09:48:05-04:00'
draft: false
categories:
  - technology
  - community
tags:
  - eclipse
  - jakartaee
  - ECA
  - contribution
  - legal
---

To make it easier for our community to maintain an active contributor status, we're introducing a new notification service for the [Eclipse Contributor Agreement (ECA)](https://www.eclipse.org/legal/eca/).

Starting June 11, 2025, we will begin sending email reminders before a standalone ECA is set to expire. For those who need to take action, the email will have a subject line of "Action Required: Your Eclipse Contributor Agreement (ECA) is Expiring Soon" and will contain a link to renew the agreement.

While these notifications apply to anyone who has signed a standalone ECA, it's important to know that Eclipse committers are already covered by a different agreement that includes the ECA, such as the Individual Committer Agreement (ICA) or the Member Company Committer Agreement (MCCA). **If you are covered by one of these agreements, your ability to contribute will not be affected by an expiring standalone ECA.** In this case, you will receive a separate, informational email with the subject "No Action Required" to confirm your status.

For those covered only by a standalone ECA, if it expires, you won't be allowed to contribute to open source projects at Eclipse until you sign it again. Specifically:

* You will no longer be able to **push changes** to an Eclipse project repositories hosted on [Eclipse Foundation GitLab](https://gitlab.eclipse.org/eclipse).
* Any commits included in a GitHub Pull Request will **fail our automated ECA validation check**.

If this happens, you can always restore your ability to contribute by visiting [https://accounts.eclipse.org/user/eca](https://accounts.eclipse.org/user/eca) and signing the ECA. Your contributor status will be restored once the new agreement is processed, which may take 5 to 15 minutes for our system caches to update.

For any questions or feedback, please join the discussion on our [HelpDesk issue](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/6222).