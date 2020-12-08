---
title: ECA Validation Update for Gerrit
author: Christopher Guindon
date: '2020-12-08T12:45:00-05:00'
draft: false
categories:
  - technology
tags:
  - eclipse
---

We are planning to install a new version of our Gerrit ECA validation plugin this week in an effort to reduce errors when a contribution is validated.

With this update, we are moving our validation logic to our new [ECA Validation API](https://github.com/EclipseFdn/git-eca-rest-api) that we created for our new Gitlab instance.

We are planning to push these changes live on **Wednesday, December 9 at 16:00 GMT**, though there is no planned downtime associated with this update other that the time required to restart the server with the new version of our plugin.

Please note that we are also planning to apply these changes to our [GitHub ECA validation app](https://github.com/apps/eclipse-eca-validation) in Q1 of 2021. You can expect more news about this in the new year!

For those interested, the code for the API and the plugin are open-source and can be seen at [git-eca-rest-api](https://github.com/EclipseFdn/git-eca-rest-api) and [gerrit-eca-plugin](https://github.com/EclipseFdn/gerrit-eca-plugin).

Please use our GitHub [issue](https://github.com/EclipseFdn/gerrit-eca-plugin/issues/24) to discuss any concerns you might have with this change.