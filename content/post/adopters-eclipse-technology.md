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

**Did you know that organizations — whether they are members of the Eclipse Foundation or not — can be listed as Eclipse technology adopters?**

In November 2019, The [Eclipse IoT](https://iot.eclipse.org/) working group launched a campaign to promote [Adopters](https://iot.eclipse.org/adopters/) of Eclipse IoT technologies. Since then, more than 60 organizations have shown their support to various Eclipse IoT projects.

With that success in mind, we decided to build a new [API service](https://github.com/EclipseFdn/eclipsefdn-project-adopters) responsible for managing Adopters for all our projects.

This will allow us to create additionnal Adopters page for our working groups. We plan on creating one for [Eclipse Cloud Development Tools](https://ecdtools.eclipse.org/) before the end of the year. Organzations that wishes to be listed on this new Adopters page can submit their request today by following our [instructions](#how-can-my-organization-become-an-adaptor-of-eclipse-technology).

On top of that, our projects will be able to leverage our JavaScript plugin to display these logos without committing them in their website git repository.

As an example, you can check out the [Eclipse Ditto](https://www.eclipse.org/ditto/) website.

## What Is Changing? 

We are migrating logos and related metadata to a new repository which means that Adopters of Eclipse IoT technologies will be asked to submit their request to this new repository. This change is expected to occur on December 10, 2020. 

We plan on updating  our documentation to point new users to this new repository. If an issue is created in the wrong repository, we will simply move the issue to the right location.

The process is very similar with this new repository but we did make some improvements: 

1. The path where we store logos is changing
2. The file format is changing from [.yml](https://github.com/EclipseFdn/iot.eclipse.org/blob/master/data/adopters.yml) to [.json](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json) to reduce user errors.
3. The structure of the file was modified to make it easier for an organization to adopt multiple projects.

We expect this change will be seamless. The content of the Eclipse IoT [Adopters](https://iot.eclipse.org/adopters/) page won't change with this migration and the JavaScript widget hosted on iot.eclipse.org will continue to work as is.

## How Can My Organization Become an Adaptor of Eclipse Technology?

The preferred way to become an adapter is with a [pull-request](https://github.com/EclipseFdn/eclipsefdn-project-adopters):

1. Add a **colored** and a **white** organization logo to [static/assets/images/adoptors](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json). We expect logos to be submitted as .svg and they must be transparent. The file size should be less than 20kb since we are planning to use them for the web!
2. Update the adopter JSON file: [config/adopters.json](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json). Organizations can be easily marked as having multiple adopted projects across different working groups, no need to create separate entries for different projects or working groups!

The alternative way to become an adopter is to submit an issue with your logo and the project name that your organization has adopted. 

## How Can We List Adopters on Our Project Website?

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

A huge thank you to [Martin Lowe](https://accounts.eclipse.org/users/malowe) for all his contributions to this project! His hard work and dedication was crucial for getting this project done on time!