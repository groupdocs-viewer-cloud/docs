---
id: "inforesult"
url: "viewer/inforesult"
title: "InfoResult"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# InfoResult #

InfoResult data structure returned by [Document Info API]({{< ref "viewer/developer-guide/basic-usage/get-document-information.md" >}}) as output result


##### InfoResult example #####

```html 

{
  "FormatExtension": "string",
  "Format": "string",
  "Pages": [
    {
      "Number": 0,
      "Width": 0,
      "Height": 0,
      "Visible": true,
      "Lines": [
        {
          "X": 0,
          "Y": 0,
          "Width": 0,
          "Height": 0,
          "Value": "string",
          "Words": [
            {
              "X": 0,
              "Y": 0,
              "Width": 0,
              "Height": 0,
              "Value": "string",
              "Characters": [
                {
                  "X": 0,
                  "Y": 0,
                  "Width": 0,
                  "Height": 0,
                  "Value": "string"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "Attachments": [
    {
      "Name": "string"
    }
  ],
  "ArchiveViewInfo": {
    "Folders": [
      "string"
    ]
  },
  "CadViewInfo": {
    "Layers": [
      {
        "Name": "string",
        "Visible": true
      }
    ],
    "Layouts": [
      {
        "Name": "string",
        "Width": 0,
        "Height": 0
      }
    ]
  },
  "ProjectManagementViewInfo": {
    "StartDate": "2020-04-02T05:56:17.389Z",
    "EndDate": "2020-04-02T05:56:17.389Z"
  },
  "OutlookViewInfo": {
    "Folders": [
      "string"
    ]
  },
  "PdfViewInfo": {
    "PrintingAllowed": true
  }
}

 ```

##### InfoResult fields #####

|#Name|#Description
|FormatExtension|File format extension
|Format|File format
|Pages|List of document pages
|Attachments|List of document attachments
|ArchiveViewInfo|Represents view information for archive file
|CadViewInfo|Represents view information for CAD drawing
|ProjectManagementViewInfo|Represents view information for MS Project document
|OutlookViewInfo|Represents view information for Outlook Data file
|PdfViewInfo|Represents view information for PDF document