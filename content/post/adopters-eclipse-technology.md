---
title: Become an Eclipse Technology Adopter
author: Christopher Guindon
date: '2020-12-03T14:30:00-05:00'
draft: false
categories:
  - technology
tags:
  - eclipse
---

**Did you know that Organizations — whether they are members of the Eclipse Foundation or not — can be listed as Eclipse technology adopters?**


In November 2019, The Eclipse IoT working group launched a campaign to promote [adopters of Eclipse IoT technologies](https://iot.eclipse.org/adopters/). Adopters are organizations that voluntarily show their support for the Eclipse projects.

Since then, more than 60 organizations have shown their support to various Eclipse technolgies.

With that success in mind, we decided build a new API service that will capture [adopters of every Eclipse project](https://github.com/EclipseFdn/eclipsefdn-project-adopters)!

This new service will allow us to create an Adopters page on each of our Eclipse Working Group website.For projects, this means that they will be able to levrege our javascript widget to display adopters on their website as done by Eclipse Ditto: https://www.eclipse.org/ditto/.

By creating this standardized platform for storing adopters' logos. Your Eclipse project website can now display them without having to keep them in git.

## How do you submit an entry for listing

However, in order to add your organization logo, you must follow our process. 

The preferred way to become an adoptor is by submitting a pull [request](https://github.com/EclipseFdn/eclipsefdn-project-adopters) with the following requirements:

1. Add a **colored** and a **white** organization logo to [static/assets/images/adoptors](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json). We expect all submitted logos to be submitted as .svg and they must be transparent. The file size of each logo should be less than 20kb since we are planing to use them for the web!
2. Update the adopter JSON file: [config/adopters.json](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json). Organizations can be easily marked as having multiple adopted projects across different working groups, no need to create separate entries for different projects or working groups!

The alternative way to become an adopter is to submit an issue with the logo and the project name that your organization has adopted. 

## What is changing? 

We are migrating logos and metadata to a new repo which means that adopter of Eclipse IoT technnolgies will need to submit their request to this new repo.

However, this change will be seemaless for our projects and users of our site. The adopters page is not chanching, we are simply updating the way that we store and fetch this information.

## How can I list adopters on my Eclipse Project website?

We built a JavaScript plugin to make this process easier. 

### Usage

Include our plugin in your page:

```html
<script src="//api.eclipse.org/adopters/assets/js/eclipsefdn.adopters.js"></script>
```

Load the plugin:

```
<script>
  eclipseFdnAdopters.getList({
    project_id: "[project_id]"
  });
</script>
```

Create an HTML element containing the chosen selector:

```
<div class="eclipsefdn-adopters"></div>
```
* By default, the selector's value is ```eclipsefdn-adopters```.

#### Options

```
<script>
  eclipseFdnAdopters.getList({
    project_id: "[project_id]",
    selector: ".eclipsefdn-adopters",
    ul_classes: "list-inline",
    logo_white: false
  });
</script>
```

Attribute     | Type        | Default   | Description
---           | ---         | ---       | ---
`project_id`   | *String*   | ` `    | **Required**: Select adopters from a specific project ID.
`selector`   | *String*   | `.eclipsefdn-adopters`    | Define the selector that the plugin will insert adopters into.
`ul_classes`  | *String*   | ` `   | Define classes that will be assigned to the ul element.
`logo_white`  | *Boolean*   | `false`   | Whether or not we use the white version of the logo.

For more information, please refer our [README.md](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/README.md).

A huge thank you to Martin Lowe for all his contributions to this project! His hard work and dedication made it possible for us to realase this new service to our community! 