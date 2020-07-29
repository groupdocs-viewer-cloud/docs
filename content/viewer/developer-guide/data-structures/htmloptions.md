---
id: "htmloptions"
url: "viewer/htmloptions"
title: "HtmlOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# HtmlOptions #

HtmlOptions data structure inherits [RenderOptions ]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}}))and used as part of [ViewOptions ]({{< ref "viewer/developer-guide/data-structures/viewoptions.md" >}}))data structure. 
|---|---|---|---

 

##### HtmlOptions example #####

```html 

{
	"ExternalResources": false,
	"ResourcePath": "string",
	"IsResponsive": true
}

 ```

##### HtmlOptions fields #####

|Name|Description
|---|---
|<RenderOptions fields>|ImageOptions inherits all properties of [RenderOptions]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}}))
|ExternalResources|Controls output HTML document resources (styles, images and fonts) linking.
By default this option is disabled and all the resources are embedded into HTML document.
|ResourcePath|Path for the HTML resources (styles, images and fonts).
For example when resource path is http:~/~/example.com/api/pages/{page-number}/resources/{resource-name}
the {page-number} and {resource-name} templates will be replaced with page number and resource name accordingly.
This option is ignored when ExternalResources option is disabled.
|IsResponsive|Indicates whether rendering will provide responsive web pages, that look well

on different device types. Default value is false.

