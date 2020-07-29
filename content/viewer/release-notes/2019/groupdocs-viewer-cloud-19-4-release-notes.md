---
id: "groupdocs-viewer-cloud-19-4-release-notes"
url: "viewer/groupdocs-viewer-cloud-19-4-release-notes"
title: "GroupDocs.Viewer Cloud 19.4 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: ""
keywords: ""
---

{{< alert style="info" >}}
This page contains release notes for GroupDocs.Viewer Cloud 19.4
{{< /alert >}}

# Major Features #

* Added PS (PostScript) EPS (Encapsulated PostScript) file formats support
* Added OutputPath parameter which enables users to take control over output location for the results

## Full List of Issues Covering all Changes in this Release ##

|Key|Summary|Category
|---|---|---
|VIEWERCLOUD-47|Feature|Add EPS (Encapsulated PostScript) file format support
|VIEWERCLOUD-19|Feature|Add PS (PostScript) file format support
|VIEWERCLOUD-306|Improvement|Output Path Parameter in CreateView API
|VIEWERCLOUD-305|Bug|Width and Height ImageOptions parameters not working in Image View
|VIEWERCLOUD-303|Bug|Failed to install SDK for Java with Java 12


## Public API and Backward Incompatible Changes ##

OutputPath option added to [ViewOptions]({{< ref "viewer/developer-guide/data-structures/viewoptions.md" >}}))
|---|---





```bash 
### Retrieve access token
    curl --request POST https://api.groupdocs.cloud/connect/token \
        --header 'Content-Type: application/x-www-form-urlencoded' \
        --data 'grant_type#client_credentials&#x26;client_id#[APP_SID]&#x26;client_secret#[APP_KEY]&#x26;undefined'
    ### Result:
    {
    "access_token": "[ACCESS_TOKEN]",
    "expires_in": 86400,
    "token_type": "Bearer" 
    }    

### Upload file into the storage
    curl --request POST \
    'https://api.groupdocs.cloud/v2/viewer/storage/file/one-page.docx' \
    --header 'authorization: Bearer [ACCESS_TOKEN]' \
    --data-binary @"c:\temp\one-page.docx" 
    ### Result:
    {
    "uploaded": [
        "one-page.docx" 
    ],
    "errors": []
    }

### Create view
curl --request POST \
  'https://api.groupdocs.cloud/v2/viewer/view' \
  --header 'authorization: Bearer [ACCESS_TOKEN]' \
  --header 'Content-Type: application/json' \
  --data '{ 
            "FileInfo": {
                "FilePath": "one-page.docx" 
            },
            "OutputPath": "Output"
          }'
    ### Result:
    {
    "pages": [
        {
        "number": 1,
        "resources": [],
        "path": "Output/one-page_docx/p1.html",
        "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/Output/one-page_docx/p1.html" 
        }
    ],
    "attachments": [],
    "file": null
    }

### Download Result
    curl --request GET \
    'https://api.groupdocs.cloud/v2/viewer/storage/file/Output/one-page_docx/p1.html' \
    --header 'authorization: Bearer [ACCESS_TOKEN]' \
    ### Result:
    
<Contents of Output/one-page_docx/p1.html>
 ```

