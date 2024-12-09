---
title: Gravatar Support Ending on accounts.eclipse.org
author: Christopher Guindon
date: '2024-12-09T13:23:00-05:00'
draft: false
categories:
  - technology
tags:
  - eclipse
  - jakartaee
keywords:
  - Gravatar Support
  - Eclipse Profile Picture Upload
  - Drupal 10 Migration
  - Eclipse Foundation
  - Eclipse Accounts
  - Privacy Compliance
  - Profile Picture Update
  - GitLab Profile Picture
  - Eclipse Profile
  - User Data Control
  - Profile Picture System
  - Eclipse Websites
  - Profile Management
  - Eclipse Foundation Privacy
  - Update Eclipse Profile
  - Drupal 10 Migration Eclipse
description: As part of our migration to Drupal 10, we’ve decided to discontinue support for Gravatar on some foundation sites. This change enhances privacy compliance by giving users more control over their data and ensures a more consistent experience across many of our web properties.
---

As part of our [migration to Drupal 10](https://www.chrisguindon.com/post/navigating-the-shift-from-drupal-7-to-drupal-9-10-at-the-eclipse-foundation/), we’ve decided to discontinue support for Gravatar on sites such as [accounts.eclipse.org](https://accounts.eclipse.org), [blogs.eclipse.org](https://blogs.eclipse.org), [marketplace.eclipse.org](https://marketplace.eclipse.org), and [newsroom.eclipse.org](https://newsroom.eclipse.org). This change enhances privacy compliance by giving users more control over their data and ensures a more consistent experience across many of our web properties.


## Why Are We Dropping Gravatar?

* **Improved Privacy**: Moving away from Gravatar reduces reliance on external services, giving users greater control over their profile pictures and personal data.
* **Inconsistent Profile Pictures**: Users have experienced issues in the past with their profile pictures displaying inconsistently across some sites due to syncing problems between Gravatar and our internal systems. This update ensures a more consistent experience.
* **Lack of Support with Drupal 10**: The [Gravatar integration module](https://www.drupal.org/project/gravatar) used with Drupal 7 is not compatible with Drupal 10, and maintaining support would require significant effort.


## What Does This Mean for You?

To address these issues, we’ve introduced a new profile picture endpoint that ensures a consistent solution for displaying profile pictures across supported sites. This endpoint will show either the user's uploaded picture or our default silhouette if no picture is available. This update also aligns with our goal to minimise personal data that we need to sync across our various web properties.

To display a community member's profile picture on your project website, simply replace `[:eclipse_username]` with the user's Eclipse username and use that URL as the `href` value in your image tag:

```
https://accounts.eclipse.org/user/[:eclipse_username]/picture
```

For example, my picture is available here (my Eclipse username is "cguindon"): \
[https://accounts.eclipse.org/user/cguindon/picture](https://accounts.eclipse.org/user/cguindon/picture)

The content of that image URL will automatically change if the user uploads a new picture or removes it in the future. If you display profile pictures on your project website, this new endpoint eliminates the need for you to sync profile pictures as-well!

**Important:** Some of our services, such as GitLab, manage profile pictures independently and do not use this new endpoint. This change will not affect your picture on GitLab. To update your GitLab profile picture, visit your [Eclipse GitLab Edit Profile](https://gitlab.eclipse.org/-/user_settings/profile) page.


## How You Can Take Action Now

If you currently use Gravatar for your profile picture, it will no longer be displayed on sites like [accounts.eclipse.org](https://accounts.eclipse.org), [blogs.eclipse.org](https://blogs.eclipse.org), [marketplace.eclipse.org](https://marketplace.eclipse.org), and [newsroom.eclipse.org](https://newsroom.eclipse.org). To ensure your profile has a picture, please upload an [Eclipse profile picture](https://accounts.eclipse.org/user/edit) now in your account.
