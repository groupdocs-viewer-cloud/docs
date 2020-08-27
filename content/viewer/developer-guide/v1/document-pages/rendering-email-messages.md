---
id: "rendering-email-messages"
url: "viewer/rendering-email-messages"
title: "Rendering Email Messages"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

# Changing Language for Header of Emails #

When rendering email messages by GroupDocs.Viewer uses English language to render field labels such as (From, To, Subject etc.). To change field labels you can set **FieldLabels** on [**EmailOptions** ](https://docs.dynabic.com/display/viewercloud/Options+Objects)class.
|---|---

**Viewer supports following field labels:**

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

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Render Email as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCacheFromContent).
|---|---

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
# Set field labels when rendering pages
curl --request POST \
url https://api.groupdocs.cloud/v1/viewer/sample.msg/html/pages \
header 'authorization: [Access Token]' \
header 'content-type: application/json' \
data '{"emailOptions": {"fieldLabels": [{"Field":"From", "Label":"Sender"}, {"Field":"To", "Label":"Receiver"}]}}'

# Retrieve created page
curl request GET \
 url https://api.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1 \
 header 'authorization: [Access Token]'

```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "sample.msg",
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "font.ttf",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/font.ttf"
        },
        {
          "name": "font1.ttf",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/font1.ttf"
        },
        {
          "name": "font2.ttf",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/font2.ttf"
        },
        {
          "name": "styles.css",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/styles.css"
        }
      ],
      "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1"
    }
  ]
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).
|---|---

### Changing Language for Header of Emails ###

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_Email_Header.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_Email_Header.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_Email_Header.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_Email_Header.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Render_Email_Header.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Render_Email_Header.py >}}

{{< /tab >}} {{< /tabs >}}

# Render Email documents as Image with Setting to set  Page Size #

Since the version 18.7, it is possible to set output page size for rendering Email documents into PDF. To enable this feature, please set the **PageSize **property of the **[EmailOptions](https://docs.dynabic.com/display/viewercloud/Options+Objects)** class as shown in example below. Please note, that for rendering into HTML the whole email message is rendered into one responsive HTML page and this new option will not influence the rendering.
|---|---

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Render Email as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCacheFromContent).
|---|---

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
# Set page size when rendering pages  curl request POST \ 
url http://api.groupdocs.cloud/v1/viewer/message.msg/image/pages \ 
header 'authorization: [Access Token]' \  header 'content-type: application/json' \
data '{"emailOptions": {"pageSize": "A0"}}' 

# Retrieve created page  curl request GET \ 
url http://api.groupdocs.cloud/v1/viewer/message.msg/image/pages/1 \ 
header 'authorization: [Access Token]'
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "sample.msg",
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "font.ttf",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/font.ttf"
        },
        {
          "name": "font1.ttf",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/font1.ttf"
        },
        {
          "name": "font2.ttf",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/font2.ttf"
        },
        {
          "name": "styles.css",
          "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1/resources/styles.css"
        }
      ],
      "url": "https://api-dev.groupdocs.cloud/v1/viewer/sample.msg/html/pages/1"
    }
  ]
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).
|---|---

### Render Email documents as Image with Setting to set  Page Size ###

{{< tabs tabTotal="6" tabID="11" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_Email_Image_PageSize.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_Email_Image_PageSize.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_Email_Image_PageSize.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_Email_Image_PageSize.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Render_Email_Image_PageSize.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Render_Email_Image_PageSize.py >}}

{{< /tab >}} {{< /tabs >}}

