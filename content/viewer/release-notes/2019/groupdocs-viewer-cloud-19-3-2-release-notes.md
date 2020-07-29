---
id: "groupdocs-viewer-cloud-19-3-2-release-notes"
url: "viewer/groupdocs-viewer-cloud-19-3-2-release-notes"
title: "GroupDocs.Viewer Cloud 19.3.2 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: ""
keywords: ""
---

{{< alert style="info" >}}
This page contains release notes for GroupDocs.Viewer Cloud 19.3.2
{{< /alert >}}

# Major Features #

This is hot-fix release which includes 3 bug-fixes and 2 improvements.

## Full List of Issues Covering all Changes in this Release ##

|Key|Summary|Category
|---|---|---
|VIEWERCLOUD-302|Update methods description|Improvement
|VIEWERCLOUD-285|Support of responsive HTML in V2 API version|Improvement
|VIEWERCLOUD-284|Download HTML pages in V2 API version|Bug
|VIEWERCLOUD-282|GroupDocs.Viewer Cloud PHP SDK V2 is not proper on GitHub|Bug
|VIEWERCLOUD-278|Serialize complex types to log message|Bug


## Public API and Backward Incompatible Changes ##

IsResponsive option added to  [HtmlOptions]({{< ref "viewer/developer-guide/data-structures/htmloptions.md" >}})) 
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
            "RenderOptions": {
                "IsResponsive": true
            }
          }'
    ### Result:
    {
    "pages": [
        {
        "number": 1,
        "resources": [],
        "path": "viewer/one-page_docx/p1.html",
        "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/one-page_docx/p1.html" 
        }
    ],
    "attachments": [],
    "file": null
    }

### Download Result
    curl --request GET \
    'https://api.groupdocs.cloud/v2/viewer/storage/file/viewer/one-page_docx/p1.html' \
    --header 'authorization: Bearer [ACCESS_TOKEN]' \
    ### Result:
    
<Contents of viewer/one-page_docx/p1.html>
 ```

