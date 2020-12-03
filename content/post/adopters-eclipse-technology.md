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

In November 2019, The Eclipse IoT working group launched a campaign to promote [adopters of Eclipse IoT technologies](https://iot.eclipse.org/adopters/). For those who don't know, Adopters are organizations that voluntarily show their support for an Eclipse project.

Since the launch, more than 60 organizations have shown their support to various Eclipse technologies.

With that success in mind, we decided to build a new [API service](https://github.com/EclipseFdn/eclipsefdn-project-adopters) responsible for managing adopters for all our projects.

We plan on using this service to create an Adopters page for any Eclipse Working Group that wishes to have one. On top of that, our projects will be able to leverage our JavaScript plugin to display logos of adopters without committing the files' in their website git repository.

As an example, you can check out the [Eclipse Ditto](https://www.eclipse.org/ditto/) website.

## What Is Changing? 

We are migrating logos and related metadata to a new repository which means that adopters of Eclipse IoT technologies will be asked to submit their request to this new repository. This change is expected to occur on December 10, 2020. 

We also plan on updating the IoT Documentation on that day to point new users to this new repository. It won’t be a problem, if an issue is created in the wrong repository, we will simply move the issue to the right location.

It’s important to understand that the process is very similar with this new repository but we did make some improvements. 

The path for our logos is different and more importantly, the adopters metadata file was re-defined. We decided to use .json instead of .yml to avoid user errors. The structure of the file is changing to make it easier for an organization to acquire more than one Eclipse technology.

However, we expect this change will be seamless for our projects and users of our sites. The content of the adopters page is not changing, we are simply updating the way that we store and fetch this information and the JavaScript widget hosted on iot.eclipse.org will continue to work as is. An Eclipse project website that is already using our JavaScript widget won’t be required to make any changes for this migration.

## How Can My Organization Become an Adaptor of Eclipse Technology?

The preferred way to become an adapter is with a [pull-request](https://github.com/EclipseFdn/eclipsefdn-project-adopters):

1. Add a **colored** and a **white** organization logo to [static/assets/images/adoptors](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json). We expect logos to be submitted as .svg and they must be transparent. The file size should be less than 20kb since we are planning to use them for the web!
2. Update the adopter JSON file: [config/adopters.json](https://github.com/EclipseFdn/eclipsefdn-project-adopters/blob/master/config/adopters.json). Organizations can be easily marked as having multiple adopted projects across different working groups, no need to create separate entries for different projects or working groups!

The alternative way to become an adopter is to submit an issue with the logo and the project name that your organization has adopted. 


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