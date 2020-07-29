---
id: "groupdocs-viewer-cloud-18-11-release-notes"
url: "viewer/groupdocs-viewer-cloud-18-11-release-notes"
title: "GroupDocs.Viewer Cloud 18.11 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

## Major Features ##

The most notable features in this release are:

* Added next file formats support:
** CGM (Computer Graphics Metafile) 
** PST (MS Outlook data file)
** OST (MS Outlook data file)
** PCL (Printer Command Language)
** TSV (Tab Separated values)

* Temporally removed support for CAD file formats (DXF, DWG, DWF, DGN)
* Added Time interval option for rendering MS Project documents
* Added possibility to get project start and end dates from MS Porject document
* Added support of rendering Microsoft Project documents as HTML with embedded resources
* Added new option which allows setting list of fonts to exclude when rendering into HTML

## Full List of Issues Covering all Changes in this Release ##

|Key
|---
|Summary
|Category
|VIEWERCLOUD-215|Time interval option for rendering MS Project documents|Feature
|VIEWERCLOUD-216|Add CGM (Computer Graphics Metafile) file format support|Feature
|VIEWERCLOUD-217|Add support for rendering PST file format|Feature
|VIEWERCLOUD-218|Add support for rendering OST file format|Feature
|VIEWERCLOUD-219|Obtaining start and end dates from MS Porject document|Feature
|VIEWERCLOUD-224|Option for setting the list of fonts that should be excluded from HTML|Feature
|VIEWERCLOUD-225|Add PCL file format support|Feature
|VIEWERCLOUD-226|Add TSV (Tab-separated values) file format support|Feature
|VIEWERCLOUD-228|Exclude CAD file formats from list of supported formats|Feature
|VIEWERCLOUD-95|Photoshop file format (PSD) is not listed as supported file format|Bug
|VIEWERCLOUD-208|Objects model schema is missing at apireference.groupdocs.cloud|Bug
|VIEWERCLOUD-230|Password required to get attachment page after geting pages|Bug


## Public API and Backward Incompatible Changes ##


### CAD file formats are excluded from supported formats ###

CAD file formats are excluded from list of supported formats in the GroupDocs.Viewer.Cloud 18.11


### Obtaining start and end dates from MS Project document ###

Since the version 18.11 GroupDocs.Viewer Cloud API allows to get start and end dates from MS Project document.





```bash 

### Retrieve access token
curl --request POST \
  --url https://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'

### Upload file into the storage
curl --request PUT \
  'https://api.groupdocs.cloud/v1/storage/file?path#%2Fsample.mpp' \
  --header 'authorization: Bearer [Access Token]' \
  --header 'cache-control: no-cache'
  --data-binary @"c:\storage\sample.mpp"

### Get document info
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/info \
  --header 'authorization: Bearer [Access Token]' \
 

 ```

```html 
{
    "fileName": "sample.mpp",
    "extension": ".mpp",
    "fileFormat": "Microsoft Project",
    "size": 289792,
    "dateModified": "2018-10-19T08:03:09.6274443Z",
    "pages": [
        {
            "number": 1,
            "name": "",
            "width": 2245,
            "height": 1587,
            "angle": 0,
            "visible": true,
            "rows": null
        }
    ],
    "attachments": [],
    "layers": null,
    "startDate": "2008-06-01T00:00:00",
    "endDate": "2008-09-03T00:00:00"
}
 ```




### Option for setting list of fonts that should be excluded from HTML ###

Adding fonts into HTML ensures that the text from the original document will appear similar in HTML, regardless of whether fonts are installed on the viewer's device or not. But at the same time, this improvement comes with the cost of the increased size of the output file. Since the version 18.10 GroupDocs.Viewer API provides a new setting - **[HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).ExcludeFontsList**, that allows finding the compromise, by preventing adding specific fonts (that are commonly available on most of the devices). The example below shows how to prevent adding fonts into output HTML. Currently, it works only for Presentation documents. We are planning to extend support for this feature for all document types where it is applicable in the upcoming releases.




```bash 
### Retrieve access token
curl --request POST \
  --url https://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'

### Upload file into the storage
curl --request PUT \
  'https://api.groupdocs.cloud/v1/storage/file?path#%2Fsample.pptx' \
  --header 'authorization: Bearer [Access Token]' \
  --header 'cache-control: no-cache'
  --data-binary @"c:\storage\sample.pptx"

### Set excludeFontsList when rendering pages
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/sample.pptx/html/pages \
  --header 'authorization: Bearer [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"embedResources": true, "excludeFontsList": ["Arial"]}'
 
### Retrieve created page
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/sample.pptx/html/pages/1 \
  --header 'authorization: Bearer [Access Token]'
 ```
 


### Outlook data files rendering support ###

 

Since the version 18.11 GroupDocs.Viewer Cloud API allows to render MS Outlook data files in .pst and .ost formats. 

 

Additionally, an OutlookOptions can be used for rendering.

 





```bash 
### Retrieve access token
curl --request POST \
  --url https://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'

### Upload file into the storage
curl --request PUT \
  'https://api.groupdocs.cloud/v1/storage/file?path#%2Fdata.pst' \
  --header 'authorization: Bearer [Access Token]' \
  --header 'cache-control: no-cache'
  --data-binary @"c:\storage\data.pst"

### Set start and end date when rendering pages
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/data.pst/html/pages \
  --header 'authorization: Bearer [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"outlookOptions": {"maxItemsInFolder": "10"}}'
 
### Retrieve created page
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/data.pst/html/pages/1 \
  --header 'authorization: Bearer [Access Token]'
 ```



### Rendering MS Project documents by specifying Project Start and End dates ###
|---|---

Since the version 18.11 GroupDocs.Viewer Cloud API allows to render part of MS Project  document according to specified StartDate and EndDate properties of ProjectOptions class as shown in examples below. When only one of this properties is set, rendering starts from project start or to end date correspondingly.





```bash 
### Retrieve access token
curl --request POST \
  --url https://api.groupdocs.cloud/oauth2/token \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type#client_credentials&#x26;client_id#[Your AppSid]&#x26;client_secret#[Your AppKey]'

### Upload file into the storage
curl --request PUT \
  'https://api.groupdocs.cloud/v1/storage/file?path#%2Fsample.mpp' \
  --header 'authorization: Bearer [Access Token]' \
  --header 'cache-control: no-cache'
  --data-binary @"c:\storage\sample.mpp"

### Set start and end date when rendering pages
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages \
  --header 'authorization: Bearer [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"projectOptions": {"startDate": "07/01/2008","endDate": "07/31/2008"}}'
 
### Retrieve created page
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1 \
  --header 'authorization: Bearer [Access Token]'
 ```





