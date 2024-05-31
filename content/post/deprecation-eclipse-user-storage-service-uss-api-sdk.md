---
title: Announcing the Deprecation of the Eclipse User Storage Service (USS) API and SDK
author: Christopher Guindon
date: '2024-05-31T10:54:00-04:00'
draft: false
categories:
  - technology
tags:
  - eclipse
---

Today, we are announcing the deprecation of the [Eclipse User Storage Service SDK](https://projects.eclipse.org/projects/technology.usssdk) (the Eclipse project) and the [Eclipse User Storage Service API](https://webdev.eclipse.org/docs/api/additional-api-docs/#tag/Eclipse-USS) (hosted and maintained by the Eclipse Foundation).

The Eclipse User Storage Service (USS) API was created in 2015 to enable Eclipse projects to store and retrieve user data and preferences from our servers. Complementing this is the [Eclipse User Storage Service SDK](https://projects.eclipse.org/projects/technology.usssdk) which offers a user-friendly Java library tailored for Eclipse RCP-based applications to simplify the integration with Eclipse USS API by managing the authentication and login processes.

Despite their past utility, the usage of this service has been steadily declining, and the costs associated with maintaining it are increasing.

Our current plan is to remove the Eclipse USS SDK from SimRel before the release of Eclipse IDE 2025-03 and to shut down the API service by **July 2nd, 2025**.

We appreciate your understanding and cooperation as we navigate these changes. If you have any questions or require further assistance, please don't hesitate to reach out via our [helpdesk issue #4696](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/4696).


### References

* [Deprecate the Eclipse User Storage Service (USS) by July 2, 2025](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/4696).
* [Eclipse User Storage Service SDK project](https://projects.eclipse.org/projects/technology.usssdk)
* [Eclipse USS OpenAPI Docs](https://webdev.eclipse.org/docs/api/additional-api-docs/#tag/Eclipse-USS)
* [Eclipsepedia: Eclipse USS](https://wiki.eclipse.org/Eclipse_USS)
* [Eclipse Oomph](https://projects.eclipse.org/projects/tools.oomph)
* [Eclipse MarketPlace Client](https://projects.eclipse.org/projects/technology.packaging.mpc)