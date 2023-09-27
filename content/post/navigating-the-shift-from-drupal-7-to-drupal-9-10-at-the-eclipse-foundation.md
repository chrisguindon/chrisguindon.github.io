---
title: Navigating the Shift From Drupal 7 to Drupal 9/10 at the Eclipse Foundation
linktitle: Navigating the Shift From Drupal 7 to Drupal 9/10 at the Eclipse Foundation
author: Christopher Guindon
date: 2023-09-27T13:00:43.065Z
draft: false
categories: []
tags:
  - eclipse
  - jakartaee
keywords:
  - Drupal
  - Drupal Migration
  - Drupal 7 to Drupal 10
  - Website Migration
  - Eclipse Community
  - Eclipse Foundation
  - API
  - Eclipse Marketplace
  - Digital Transformation
  - Eclipse Project Management Infrastructure
  - CMS Migration
  - Content Management
  - API Integration
  - Team Collaboration
  - Future-Proofing
  - Web Development
  - Digital Transition
---
We're currently in the middle of a substantial transition as we are migrating mission-critical websites from Drupal 7 to Drupal 9, with our sights set on Drupal 10. This shift has been motivated by several factors, including the announcement of [Drupal 7 end-of-life](https://www.drupal.org/psa-2023-06-07) which is now scheduled for January 5, 2025, and our goal to reduce technical debt that we accrued over the last decade.

To provide some context, we're migrating a total of six key websites:

* **[projects.eclipse.org](https://projects.eclipse.org/):** The Eclipse Project Management Infrastructure (PMI) consolidates project management activities into a single consistent location and experience.
* **[accounts.eclipse.org](https://accounts.eclipse.org/):** The Eclipse Account website is where our users go to manage their profiles and sign essential agreements, like the Eclipse Contributor Agreement (ECA) and the Eclipse Individual Committer Agreement (ICA).
* **[blogs.eclipse.org](https://blogs.eclipse.org/):** Our official blogging platform for Foundation staff.
* **[newsroom.eclipse.org](https://newsroom.eclipse.org/):** The Eclipse Newsroom is our content management system for news, events, newsletters, and valuable resources like case studies, market reports, and whitepapers.
* **[marketplace.eclipse.org](https://marketplace.eclipse.org/):** The Eclipse Marketplace empowers users to discover solutions that enhance their Eclipse IDE. 
* **[eclipse.org/downloads/packages](https://www.eclipse.org/downloads/packages/)**: The Eclipse Packaging website is our platform for managing the publication of download links for the Eclipse Installer and Eclipse IDE Packages on our websites.

## The Progress So Far

We’ve made substantial progress this year with our migration efforts. The team successfully completed the migration of [Eclipse Blogs](https://blogs.eclipse.org/) and [Eclipse Newsroom](https://newsroom.eclipse.org/). We are also in the final stages of development with the [Eclipse Marketplace](https://marketplace.eclipse.org/), which is currently scheduled for a production release on October 25, 2023. Next year, we'll focus our attention on completing the migration of our more substantial sites, such as [Eclipse PMI](https://projects.eclipse.org/), [Eclipse Accounts](https://accounts.eclipse.org/), and [Eclipse Packaging](https://www.eclipse.org/downloads/packages/).

## More Than a Simple Migration: Decoupling Drupal APIs With Quarkus

This initiative isn't just about moving from one version of Drupal to another. Simultaneously, we're undertaking the task of decoupling essential APIs from Drupal in the hope that future migration or upgrade won’t impact as many core services at the same time. For this purpose, we've chosen [Quarkus](https://quarkus.io/about/) as our preferred platform. In Q3 2023, the team successfully migrated the GitHub ECA Validation Service and the Open-VSX Publisher Agreement Service from Drupal to Quarkus. In Q4 2023, we're planning to continue down that path and deploy a Quarkus implementation of several critical APIs such as:

* Account Profile API: This API offers user information, covering ECA status and profile details like bios.
* User Deletion API: This API monitors user deletion requests ensuring the right to be forgotten.
* Committer Paperwork API: This API keeps tabs on the status of ongoing committer paperwork records.
* Eclipse USS: The Eclipse User Storage Service (USS) allows Eclipse projects to store user-specific project information on our servers.

## Conclusion: A Forward-Looking Transition

Our migration journey from Drupal 7 to Drupal 9, with plans for Drupal 10, represents our commitment to providing a secure, efficient, and user-friendly online experience for our community. We are excited about the possibilities this migration will unlock for us, advancing us toward a more modern web stack. 

Finally, I'd like to take this moment to highlight that this project is a monumental team effort, thanks to the exceptional contributions of Eric Poirier and Théodore Biadala, our Drupal developers; Martin Lowe and Zachary Sabourin, our Java developers implementing the API decoupling objective; and Frederic Gurr, whose support has been instrumental in deploying our new apps on the Eclipse Infrastructure.