---
id: "supported-file-formats"
url: "viewer/supported-file-formats"
title: "Supported File Formats"
productName: "GroupDocs.Viewer Cloud"
weight: 13
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this Page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}






# Introduction #

GroupDocs.Viewer Cloud REST APIs support to render over 50 file formats to HTML5 or Image formats for the whole document, page by page or custom range of pages. To get list of supported formats, You can use the below API.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [Supported File Formats](https://apireference.groupdocs.cloud/viewer/#!/Formats/GetSupportedFileFormats) example.

## cURL Example ##



 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/formats" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer olzXlublkkhjir2lLJeQZa6JLmodllVmX7pU7jf5t7iZm8bbbsXtzrV1t_t5FGro0bq36vg5syRH0ZILdIjDQxSNM5EuuoJFDvLrUtL9YO3t4vMRP0o-JDejzco8Ut8qGClOqYu1EIj5bfvL51Zd2YliHFlHX-nInUzyDxWESrfR0kOiODJvW_k-OiIChGMAOQnGByi4NSlIaYtvHEeVXgkRd8yMbK2Gn5-vyDGEgTlx0q_g_9cXnGUHRFVRCozY6tklo-GqLeGe65VNSzo0Zd9X4Y5p-hBOZnHpkyMMc1DHT8WPAeZrpLunemAQo6EIjusN_mtP_v4G_LLcvFAgAf2-mkBoYuNdjl7i8mbh5mrQraU-gJu5BSMY-U-EcHhghKJybWMqD-Gft2mG4Ajv-k1gY4RxHNG85dc_pXOquvQFROaK"


 ```


 Response

```html 
{
  "formats": [
    {
      "fileFormat": "Portable Document Format",
      "extension": ".pdf"
    },
    {
      "fileFormat": "Microsoft Word",
      "extension": ".doc"
    },
    {
      "fileFormat": "Microsoft Word",
      "extension": ".docx"
    },
    {
      "fileFormat": "Microsoft Word",
      "extension": ".docm"
    },
    {
      "fileFormat": "Microsoft Word",
      "extension": ".dot"
    },
    {
      "fileFormat": "Microsoft Word",
      "extension": ".dotx"
    },
    {
      "fileFormat": "Microsoft Word",
      "extension": ".dotm"
    },
    {
      "fileFormat": "Mobipocket",
      "extension": ".mobi"
    },
    {
      "fileFormat": "Microsoft Excel",
      "extension": ".xls"
    },
    {
      "fileFormat": "Microsoft Excel",
      "extension": ".xlsx"
    },
    {
      "fileFormat": "Microsoft Excel",
      "extension": ".xlsm"
    },
    {
      "fileFormat": "Microsoft Excel",
      "extension": ".xlsb"
    },
    {
      "fileFormat": "Microsoft PowerPoint",
      "extension": ".ppt"
    },
    {
      "fileFormat": "Microsoft PowerPoint",
      "extension": ".pptx"
    },
    {
      "fileFormat": "Microsoft PowerPoint",
      "extension": ".pps"
    },
    {
      "fileFormat": "Microsoft PowerPoint",
      "extension": ".ppsx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vsd"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vdx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vss"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vsx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vst"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vtx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vsdx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vdw"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vssx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vstx"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vstm"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vsdm"
    },
    {
      "fileFormat": "Microsoft Visio",
      "extension": ".vssm"
    },
    {
      "fileFormat": "Microsoft Project",
      "extension": ".mpp"
    },
    {
      "fileFormat": "Microsoft Project",
      "extension": ".mpt"
    },
    {
      "fileFormat": "Microsoft Outlook",
      "extension": ".msg"
    },
    {
      "fileFormat": "Microsoft Outlook",
      "extension": ".eml"
    },
    {
      "fileFormat": "Microsoft OneNote",
      "extension": ".one"
    },
    {
      "fileFormat": "Apple Mail",
      "extension": ".emlx"
    },
    {
      "fileFormat": "OpenDocument Formats",
      "extension": ".odt"
    },
    {
      "fileFormat": "OpenDocument Formats",
      "extension": ".ott"
    },
    {
      "fileFormat": "OpenDocument Formats",
      "extension": ".ods"
    },
    {
      "fileFormat": "OpenDocument Formats",
      "extension": ".odp"
    },
    {
      "fileFormat": "OpenDocument Formats",
      "extension": ".otp"
    },
    {
      "fileFormat": "OpenDocument Formats",
      "extension": ".ots"
    },
    {
      "fileFormat": "Rich Text Format",
      "extension": ".rtf"
    },
    {
      "fileFormat": "Plain Text File",
      "extension": ".txt"
    },
    {
      "fileFormat": "LaTeX Scientific document",
      "extension": ".tex"
    },
    {
      "fileFormat": "Comma-Separated Values",
      "extension": ".csv"
    },
    {
      "fileFormat": "HyperText Markup Language",
      "extension": ".html"
    },
    {
      "fileFormat": "HyperText Markup Language",
      "extension": ".mht"
    },
    {
      "fileFormat": "Extensible Markup Language",
      "extension": ".xml"
    },
    {
      "fileFormat": "XML Paper Specification",
      "extension": ".xps"
    },
    {
      "fileFormat": "CAD Drawing File Format",
      "extension": ".dxf"
    },
    {
      "fileFormat": "CAD Drawing File Format",
      "extension": ".dwg"
    },
    {
      "fileFormat": "CAD Drawing File Format",
      "extension": ".dwf"
    },
    {
      "fileFormat": "CAD Drawing File Format",
      "extension": ".ifc"
    },
    {
      "fileFormat": "CAD Drawing File Format",
      "extension": ".stl"
    },
    {
      "fileFormat": "Image files",
      "extension": ".bmp"
    },
    {
      "fileFormat": "Image files",
      "extension": ".gif"
    },
    {
      "fileFormat": "Image files",
      "extension": ".jpg"
    },
    {
      "fileFormat": "Image files",
      "extension": ".jpeg"
    },
    {
      "fileFormat": "Image files",
      "extension": ".png"
    },
    {
      "fileFormat": "Image files",
      "extension": ".tiff"
    },
    {
      "fileFormat": "Image files",
      "extension": ".djvu"
    },
    {
      "fileFormat": "Image files",
      "extension": ".svg"
    },
    {
      "fileFormat": "Image files",
      "extension": ".webp"
    },
    {
      "fileFormat": "Image files",
      "extension": ".dng"
    },
    {
      "fileFormat": "Digital Imaging and Communications in Medicine",
      "extension": ".dcm"
    },
    {
      "fileFormat": "Electronic publication",
      "extension": ".epub"
    },
    {
      "fileFormat": "Windows Icon",
      "extension": ".ico"
    },
    {
      "fileFormat": "Windows Metafile",
      "extension": ".wmf"
    },
    {
      "fileFormat": "Windows Metafile",
      "extension": ".emf"
    }
  ]
}
 ```




## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get List of Supported File Formats ###



 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_All_Supported_Formats.cs >}}





 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_All_File_Formats.php >}}





 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_All_Supported_Formats.java >}}





 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_All_Supported_Formats.rb >}}





 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_All_File_Formats.js >}}





 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_All_File_Formats.py >}}




