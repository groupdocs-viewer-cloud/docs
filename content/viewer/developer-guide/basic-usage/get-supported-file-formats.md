---
id: "get-supported-file-formats"
url: "viewer/get-supported-file-formats"
title: "Get Supported File Formats"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: ""
keywords: ""
---






# Get Supported File Formats #

GroupDocs.Viewer Cloud REST APIs support to render over 50 file formats to HTML5 or Image formats for the whole document, page by page or custom range of pages. To get list of supported formats, You can use the below API.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [Supported File Formats](https://apireference.groupdocs.cloud/viewer/#/Viewer/GetSupportedFileFormats) example.

## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/formats" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"

 ```




 Response

```html 
{
  "formats": [
    {
      "extension": ".pdf",
      "fileFormat": "Portable Document Format"
    },
    {
      "extension": ".pcl",
      "fileFormat": "Printer Command Language Document"
    },
    {
      "extension": ".doc",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".docx",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".docm",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".dot",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".dotx",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".dotm",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".mobi",
      "fileFormat": "Mobipocket"
    },
    {
      "extension": ".xls",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xlsx",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xlsm",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xltx",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xltm",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xlsb",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".ppt",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".pptx",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".pps",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".ppsx",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".potm",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".ppsm",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".potx",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".pptm",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".vsd",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vdx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vss",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vsx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vst",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vtx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vsdx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vdw",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vssx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vstx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vstm",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vsdm",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vssm",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".mpp",
      "fileFormat": "Microsoft Project"
    },
    {
      "extension": ".mpt",
      "fileFormat": "Microsoft Project"
    },
    {
      "extension": ".msg",
      "fileFormat": "Microsoft Outlook Mail Message"
    },
    {
      "extension": ".eml",
      "fileFormat": "Microsoft Outlook Mail Message"
    },
    {
      "extension": ".ost",
      "fileFormat": "Microsoft Outlook Data Files"
    },
    {
      "extension": ".pst",
      "fileFormat": "Microsoft Outlook Data Files"
    },
    {
      "extension": ".one",
      "fileFormat": "Microsoft OneNote"
    },
    {
      "extension": ".emlx",
      "fileFormat": "Apple Mail"
    },
    {
      "extension": ".odt",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".ott",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".ods",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".odp",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".otp",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".ots",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".odg",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".rtf",
      "fileFormat": "Rich Text Format"
    },
    {
      "extension": ".txt",
      "fileFormat": "Plain Text File"
    },
    {
      "extension": ".tex",
      "fileFormat": "LaTeX Scientific document"
    },
    {
      "extension": ".csv",
      "fileFormat": "Comma-Separated Values"
    },
    {
      "extension": ".tsv",
      "fileFormat": "Tab-Separated Values"
    },
    {
      "extension": ".html",
      "fileFormat": "HyperText Markup Language"
    },
    {
      "extension": ".mht",
      "fileFormat": "HyperText Markup Language"
    },
    {
      "extension": ".xml",
      "fileFormat": "Extensible Markup Language"
    },
    {
      "extension": ".xps",
      "fileFormat": "XML Paper Specification"
    },
    {
      "extension": ".bmp",
      "fileFormat": "Image files"
    },
    {
      "extension": ".gif",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpg",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpeg",
      "fileFormat": "Image files"
    },
    {
      "extension": ".png",
      "fileFormat": "Image files"
    },
    {
      "extension": ".tiff",
      "fileFormat": "Image files"
    },
    {
      "extension": ".djvu",
      "fileFormat": "Image files"
    },
    {
      "extension": ".svg",
      "fileFormat": "Image files"
    },
    {
      "extension": ".webp",
      "fileFormat": "Image files"
    },
    {
      "extension": ".dng",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jp2",
      "fileFormat": "Image files"
    },
    {
      "extension": ".j2c",
      "fileFormat": "Image files"
    },
    {
      "extension": ".j2k",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpf",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpx",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpm",
      "fileFormat": "Image files"
    },
    {
      "extension": ".dcm",
      "fileFormat": "Digital Imaging and Communications in Medicine"
    },
    {
      "extension": ".epub",
      "fileFormat": "Electronic publication"
    },
    {
      "extension": ".ico",
      "fileFormat": "Windows Icon"
    },
    {
      "extension": ".wmf",
      "fileFormat": "Windows Metafile"
    },
    {
      "extension": ".emf",
      "fileFormat": "Windows Metafile"
    },
    {
      "extension": ".psd",
      "fileFormat": "Photoshop"
    },
    {
      "extension": ".cgm",
      "fileFormat": "Computer Graphics Metafile"
    }
  ]
}


 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get List of Supported File Formats ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Supported_Formats.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_All_File_Formats.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_All_Supported_Formats.java >}}







 Ruby




{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Get_All_Supported_Formats.rb >}}







 Node.js




{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_All_Supported_Formats.js >}}







 Python




{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Get_All_Supported_Formats.py >}}







