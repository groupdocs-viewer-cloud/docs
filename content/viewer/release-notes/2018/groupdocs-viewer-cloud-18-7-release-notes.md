---
id: "groupdocs-viewer-cloud-18-7-release-notes"
url: "viewer/groupdocs-viewer-cloud-18-7-release-notes"
title: "GroupDocs.Viewer Cloud 18.7 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 2
description: ""
keywords: ""
---

## Major Features ##

There 13 features and fixes in this release. The most notable are:

* Added next file formats support:
** DGN (V7) (MicroStation design file)
** DWF (AutoCAD Design Web Format)
*  Extended support of DefaultFontName setting on
** Rendering PDF documents into PDF and HTML

* \\
** Rendering MS Project documents into PDF
** Rendering ODG, SVG and MetaFile Images
* Added feature to set page size when rendering Email messages as PDF and image
* Added feature which allows changing labels when rendering Email messages

## Full List of Issues Covering all Changes in this Release ##

|Key
|---
|Summary
|Category
|VIEWERCLOUD-175|Add ISFF-based DGN (V7) file format support|New Feature
|VIEWERCLOUD-171|Extend support for DefaultFontName setting to PDF documents when rendering into PDF|New Feature
|VIEWERCLOUD-170|Render CAD documents by specifying coordinates|New Feature
|VIEWERCLOUD-169|Add DWF file format support|New Feature
|VIEWERCLOUD-167|Extend support for DefaultFontName option for MS Project documents when rendering into PDF|New Feature
|VIEWERCLOUD-165|Add support for rendering password protected ODT and OTT formats|New Feature
|VIEWERCLOUD-164|Changing language for header of emails|New Feature
|VIEWERCLOUD-163|Setting page size when rendering Email documents as PDF and image|New Feature
|VIEWERCLOUD-177|Improve compression for rendering into HTML with EnableMinification setting|Improvement
|VIEWERCLOUD-176|Extend DefaultFontName setting support for ODG, SVG and MetaFile Images|Improvement
|VIEWERCLOUD-173|Extend support for DefaultFontName option for CAD documents|Improvement
|VIEWERCLOUD-172|Eliminate the gap between list of tasks and footer when rendering MS Project documents|Improvement
|VIEWERCLOUD-145|Extend support for DefaultFontName setting to PDF documents when rendering into HTML|Improvement


## Public API and Backward Incompatible Changes ##


### Changing language for header of emails ###

![](viewer/images/EmailHeader.png)

When rendering email messages by default Viewer uses English languge to render field labels such as (From, To, Subject etc.). To change field labels you can set **FieldLabels** on **EmailOptions** [options-objects]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})class.



```html 
 ### Retrieve access token
curl --request POST \
  --url https://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#appSid&#x26;client_secret#appKey'

### Set field labels when rendering pages
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/sample.msg/html/pages \
  --header 'authorization: [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"emailOptions": {"fieldLabels": [{"Field":"From", "Label":"Sender"}, {"Field":"To", "Label":"Receiver"}]}}'

### Retrieve created page
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1 \
  --header 'authorization: [Access Token]'

 ```
  Viewer supports following field labels:

|Field|Label
|---|---
|Anniversary |Anniversary
|Bcc |Bcc
|Birthday|Birthday
|Business|Business
|Business Address |Business Address
|Business Fax |Business Fax
|BusinessHomepage|BusinessHomepage
|Company|Company
|Department|Department
|Email|Email
|Email Display As|Email Display As
|Email2|Email2
|Email2 Display As|Email2 Display As
|Email3 |Email3
|Email3 Display As|Email3 Display As
|End|End
|First Name|First Name
|From|From
|Full Name|Full Name
|Gender|Gender
|Hobbies|Hobbies
|Home Address|Home Address
|Importance|Importance
|Job Title|Job Title
|Last Name|Last Name
|Location|Location
|Middle Name|Middle Name
|Mobile|Mobile
|Organizer|Organizer
|Other Address|Other Address
|PersonalHomepage|PersonalHomepage
|Profession|Profession
|Recurrence|Recurrence
|Recurrence Pattern|Recurrence Pattern
|Required Attendees|Required Attendees
|Sent|Sent
|Show Time As|Show Time As
|Spouse/Partner|Spouse/Partner
|Start|Start
|Subject|Subject
|To|To
|User Field 1|User Field 1
|User Field 2|User Field 2
|User Field 3|User Field 3
|User Field 4|User Field 4


### Rendering by coordinates or Tiled rendering ###

![](viewer/images/RendCoordinate.jpg) 

#### Introduction ####

 

Tiled rendering or (rendering by coordinates) is the process of rendering CAD documents (into an image, HTML or PDF) by dividing into square parts and rendering each part (or tile), separately. Since the version 18.7 tiled rendering is available for rendering into an image and HTML for DWG file format. Generally DWG documents are divided into pages by Model and Layouts, but when the tiled rendering is enabled, only the Model is rendered, and every tile composes a separate page. 

 

#### How to render by coordinates ####

 

Before you start rendering by coordinates, it is recommended to obtain the overall width and height of the document with help of [document info methods]({{< ref "viewer/developer-guide/v1/document-information.md" >}}) as shown in example below. After you know the width and height, determine the starting point X and Y coordinates and the width with the height of the tile (region you want to render). Then add tiles to [CadOptions.Tiles]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) as shown in example below. Coordinates start from bottom left corner of the drawing and have only positive values as shown in sample picture below. 

 


,,Overall width of the document is 650px height and 750px width. The selected tile starts at coordinate X: 250 and Y: 100 and has a width 150px, height: 200px,, 

 

![](viewer/images/coordinates.jpg) 

You can add as many tiles as you need, the following example demonstrates how to render DWG drawing into an image by dividing into four equal parts. 

 





```html 
### Retrieve access token
curl --request POST \
  --url https://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#appSid&#x26;client_secret#appKey'

### Retrive document width and height
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/three-layouts.dwg/html/info \
  --header 'authorization: [Access Token]'

### Render document by coordinates into 4 pages (tiles)
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/three-layouts.dwg/html/pages \
  --header 'authorization: [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"cadOptions": {"tiles": [{"width":1300, "height":800, "startPointX":0, "startPointY":0 },{"width":1300, "height":800, "startPointX":1300, "startPointY":0 },{"width":1300, "height":800, "startPointX":0, "startPointY":800 },{"width":1300, "height":800, "startPointX":1300, "startPointY":800 }]}}'

### Retrieve first page (tile)
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/three-layouts.dwg/html/pages/1 \
  --header 'authorization: [Access Token]'

 ```



### Setting default font when rendering PDF documents into HTML ###

Since the version 18.7, it is possible to set default font when rendering PDF document into HTML. This setting may be useful when you would like to specify which font should be used in case PDF document missing some font(s).



```html 
### Retrieve access token
curl --request POST \
  --url http://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'
 
### Set default font name when rendering PDF document as HTML
curl --request POST \
  --url http://api.groupdocs.cloud/v1/viewer/missing-font.pdf/html/pages \
  --header 'authorization: [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"defaultFontName": "Arial"}'
 
### Retrieve created page
curl --request GET \
  --url http://api.groupdocs.cloud/v1/viewer/missing-font.pdf/html/pages/1 \
  --header 'authorization: [Access Token]'
 ```
 


### Setting page size when rendering Email documents as PDF and image ###







 

 

 

![](viewer/images/pagesize.jpg)

 

 

 

Since the version 18.7, it is possible to set output page size for rendering Email documents into PDF and images. To enable this feature, please set the **PageSize **property of the **[EmailOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** class as shown in example below. Please note, that for rendering into HTML the whole email message is rendered into one responsive HTML page and this new option will not influence the rendering. 

 





```html 

### Retrieve access token
curl --request POST \
  --url http://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'
 
### Set page size when rendering pages
curl --request POST \
  --url http://api.groupdocs.cloud/v1/viewer/message.msg/image/pages \
  --header 'authorization: [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"emailOptions": {"pageSize": "A0"}}'
 
### Retrieve created page
curl --request GET \
  --url http://api.groupdocs.cloud/v1/viewer/message.msg/image/pages/1 \
  --header 'authorization: [Access Token]'

 ```

```html 
### Retrieve access token
curl --request POST \
  --url http://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'
 
### Set page size when rendering into PDF
curl --request POST \
  --url http://api.groupdocs.cloud/v1/viewer/message.msg/image/pdf \
  --header 'authorization: [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"emailOptions": {"pageSize": "A0"}}'
 
### Retrieve created PDF document
curl --request GET \
  --url http://api.groupdocs.cloud/v1/viewer/message.msg/image/pdf \
  --header 'authorization: [Access Token]'
 ```
