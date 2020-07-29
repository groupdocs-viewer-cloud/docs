---
id: "groupdocs-viewer-cloud-18-5-release-notes"
url: "viewer/groupdocs-viewer-cloud-18-5-release-notes"
title: "GroupDocs.Viewer Cloud 18.5 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: ""
keywords: ""
---

## Major Features ##

There 18 features and fixes in this release. The most notable are:

* Added next file formats supportAdded option which allows to exclude fonts when rendering as HTML
** PPTM (PowerPoint macro-enabled presentation)
** POTX (PowerPoint template)
** XLTX (Excel template)
** XLTM (Excel macro-enabled template)
* Added support of Quality option when rendering Microsoft Project documents as Image
* Added option to render only Print Area when rendering spreadsheet documents as HTML 
* Added option to enable rendering of hidden content when rendering spreadsheet documents as HTML

## Full List of Issues Covering all Changes in this Release ##

|Key
|---
|Summary
|Category
|VIEWERCLOUD-146|Feature for AutoFitting column width depending on content for rendering into HTML|New Feature
|VIEWERCLOUD-139|Add PPTM file format support|New Feature
|VIEWERCLOUD-138|Add POTX file format support|New Feature
|VIEWERCLOUD-137|Rendering only Print Area in Excel documents|New Feature
|VIEWERCLOUD-136|Settings to include/exclude hidden content in Excel documents|New Feature
|VIEWERCLOUD-130|Exclude fonts when rendering to HTML|New Feature
|VIEWERCLOUD-129|Add XLTX file format support|New Feature
|VIEWERCLOUD-128|Add XLTM file format support|New Feature
|VIEWERCLOUD-127|Specify image quality when rendering PDF documents as HTML|New Feature
|VIEWERCLOUD-144|Support Quality option when rendering Microsoft Project documents|Improvement
|VIEWERCLOUD-143|Improve rendering comments from Presentation documents|Improvement
|VIEWERCLOUD-142|Minify CSS content when rendering into HTML with embedded resources|Improvement
|VIEWERCLOUD-141|Add prefix for CSS classes when rendering Email messages|Improvement
|VIEWERCLOUD-134|Improve rendering metafile images into HTML|Improvement
|VIEWERCLOUD-133|Extend support for ShowHiddenSlides option to Open Document Presentation|Improvement
|VIEWERCLOUD-132|Exporting contained images when rendering SVG to HTML|Improvement
|VIEWERCLOUD-131|Improve rendering MS OneNote documents into HTML by providing pure HTML and SVG|Improvement
|VIEWERCLOUD-155|Error when installing PHP SDK with Composer|Bug


## Public API and Backward Incompatible Changes ##

### Prevent adding fonts  ###

 Embedded fonts increase the size of the rendering result, in order to prevent adding fonts into HTML, set **ExcludeFonts** option to **true** as shown in example below: 

Set **ExcludeFonts ****# true** to prevent adding fonts to HTML document.

**cURL**



 

|
|---

 # Retrieve authorization token




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/oauth2/token \




  ~-~-header 'content-type: application/x-www-form-urlencoded' \




  ~-~-data 'grant_type#client_credentials&client_id#[Your AppSid]&client_secret#[Your AppKey]'




 




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages \




  ~-~-header 'authorization: [Access Token]' \




  ~-~-header 'content-type: application/json' \




  ~-~-data '{"excludeFonts": true }'




 


API will return list of created pages and page resources, note that there are no fonts in resources.


Also, created html document does not contain references to external font-resources or embedded fonts.


**JSON**



 

|
|---

{




  "fileName": "one-page.docx",




  "folder": null,




  "pages": [




    {




      "number": 1,




      "resources": [




        {




          "name": "image.png",




          "url": "[http:~~/~~/api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/image.png >}}>url:http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/image.png)




        },




        {




          "name": "styles.css",




          "url": "[http:~~/~~/api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles.css >}}>url:http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles.css)




        }




      ],




      "url": "[http:~~/~~/api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1 >}}>url:http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1)




    }




  ]




}



\\





### AutoFitting column width depending on content for rendering into HTML ###

When rendering worksheets which contains overlapping text GroupDocs.Viewer adds new value **AutoFitColumn** to **TextOverflowMode** of **CellsOptions **which expands cells width to fit overflowed text.

 

**cURL**



 

|
|---

~#~## Retrieve access token




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/oauth2/token \




  ~-~-header 'content-type: application/x-www-form-urlencoded' \




  ~-~-data 'grant_type#client_credentials&client_id#[Your AppSid]&client_secret#[Your AppKey]'




 




~#~## Render worksheet and expand cells width to fit overflowed text




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages \




  ~-~-header 'authorization: [Access Token]' \




  ~-~-header 'content-type: application/json' \




  ~-~-data '{"cellsOptions": {"textOverflowMode": "AutoFitColumn"}}'




 




~#~## Retrieve created page




curl ~-~-request GET \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages/1 \




  ~-~-header 'authorization: [Access Token]'




 


Rendered worksheet cells will be expanded to fit overflowed text


### Image quality when rendering PDF documents as HTML ###

When rendering PDF documents as HTML Viewer creates single image resource which contains all the images from the PDF document page and uses created image as background for HTML document. Starting from v18.5 new option added to **PdfOptions** class called **ImageQuality **which allows you to control image resource quality. Supported values are **Low**, **Medium** and **High**. When selecting value please note that with **Low** value you'll have satisfying image quality and small image size with **High **value you'll have best quality but image will be larger in size. 

 

**cURL**



 

|
|---

# Retrieve access token




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/oauth2/token \




  ~-~-header 'content-type: application/x-www-form-urlencoded' \




  ~-~-data 'grant_type#client_credentials&client_id#[Your AppSid]&client_secret#[Your AppKey]'




 




# Create pages with High image quality




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-image.pdf/html/pages \




  ~-~-header 'authorization: [Access Token]' \




  ~-~-header 'content-type: application/json' \




  ~-~-data '{"pdfOptions": {"imageQuality": "High"}}'



\\





### Rendering only Print Area in Excel documents ###

To render sections of the workshet(s) defined as [print area](https://support.office.com/en-us/article/set-or-clear-a-print-area-on-a-worksheet-27048af8-a321-416d-ba1b-e99ae2182a7e GroupDocs.Viewer provides new option **RenderPrintAreaOnly **in **CellsOptions**. GroupDocs.Viewer renders each print area in a worksheet as a separate page.
|---|---

 

**cURL**



 

|
|---

~#~## Retrieve access token




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/oauth2/token \




  ~-~-header 'content-type: application/x-www-form-urlencoded' \




  ~-~-data 'grant_type#client_credentials&client_id#[Your AppSid]&client_secret#[Your AppKey]'




 




~#~## Enable rendering of print area(s)




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-four-print-areas.xlsx/html/pages \




  ~-~-header 'authorization: [Access Token]' \




  ~-~-header 'content-type: application/json' \




  ~-~-data '{"cellsOptions": {"renderPrintAreaOnly": true, "renderHiddenColumns": true}}'




 




~#~## Retrieve created page




curl ~-~-request GET \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-four-print-areas.xlsx/html/pages/1 \




  ~-~-header 'authorization: [Access Token]'




 


The page created by Viewer will contain hidden rows and columns


### Settings to include/exclude hidden content in Excel documents ###


 

Starting from 18.5 GroupDocs.Viewer provides new two new options **RenderHiddenRows **and **RenderHiddenColumns **in **CellsOptions **which enables rendering [hidden rows and coumns](https://support.office.com/en-us/article/hide-or-show-rows-or-columns-659c2cad-802e-44ee-a614-dde8443579f8. By default GroupDocs.Viewer doesn't render hidden rows and columns so this options should be enabled in case you would like to render hidden content.
|---|---

 

 

**cURL**



 

|
|---

~#~## Retrieve access token




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/oauth2/token \




  ~-~-header 'content-type: application/x-www-form-urlencoded' \




  ~-~-data 'grant_type#client_credentials&client_id#[Your AppSid]&client_secret#[Your AppKey]'




 




~#~## Render hidden rows and columns when creating pages




curl ~-~-request POST \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-hidden-rows-and-columns.xlsx/html/pages \




  ~-~-header 'authorization: [Access Token]' \




  ~-~-header 'content-type: application/json' \




  ~-~-data '{"cellsOptions": {"renderHiddenRows": true, "renderHiddenColumns": true}}'




 




~#~## Retrieve created page




curl ~-~-request GET \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/with-hidden-rows-and-columns.xlsx/html/pages/1 \




  ~-~-header 'authorization: [Access Token]'




 


 

The page created by Viewer will contain hidden rows and columns




