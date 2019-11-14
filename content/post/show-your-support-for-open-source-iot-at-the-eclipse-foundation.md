---
title: Show Your Support for Open Source IoT at the Eclipse Foundation
linktitle: Show Your Support for Open Source IoT at the Eclipse Foundation
author: Christopher Guindon
date: '2019-11-14T11:35:00-05:00'
draft: false
categories:
  - technology
tags:
  - eclipse
---

The [Eclipse IoT](https://iot.eclipse.org) working group is launching a campaign to identify the adopters of Eclipse IoT open source projects. Companies — whether or not they are working group members — can be listed as [adopters](https://iot.eclipse.org/adopters/).

Adopters are organizations that voluntarily show their support for the Eclipse IoT projects they have adopted (i.e. shipping commercial products based on the projects and/or using the projects for non-commercial or internal reasons). 

You can add your organization logo to our list of adopters by submitting a [pull request](https://github.com/EclipseFdn/iot.eclipse.org/pulls) or by creating an [issue](https://github.com/EclipseFdn/iot.eclipse.org/issues/new?template=adopter_request.md). You can attach files to an issue by dragging and dropping them in the text editor of the form. 

If you plan on submitting a pull request, you will need to make the following changes to the website codebase:

1. Add a colored and a white organization logo to [static/assets/images/adoptors](https://github.com/EclipseFdn/iot.eclipse.org/tree/master/static/assets/images/adopters). We expect that all submitted logos to be transparent svg.
2. Update the adopter data file: [data/adopters.yml](https://github.com/EclipseFdn/iot.eclipse.org/blob/master/data/adopters.yml) If your organization wishes to express support for multiple projects, you will need to add your organization's YAML definition to the adopters list of each of the relevant project nodes.

Your participation in this initiative will publicly show your support for open source innovation.

### List Eclipse IoT adopters on an Eclipse project website

Eclipse projects can showcase the logos of their adopters on their project websites. We built a JavaScript plugin to make this process easier. If you are a project committer, here are quick instructions on how to use the [eclipsefdn-adopters.js](https://iot.eclipse.org/assets/js/eclipsefdn.adopters.js) on your Eclipse project website:

#### Usage

Include the plugin's JS in the <head> section of the page:

```html
<script src="//iot.eclipse.org/assets/js/eclipsefdn.adopters.js"></script>
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
