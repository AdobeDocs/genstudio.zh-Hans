---
title: 自定义模板
description: 了解如何为GenStudio构建自定义模板。
level: Intermediate
feature: Templates, Content
source-git-commit: 423956d6fdbf5b31041d44eb434f90d55a87d7c0
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---


# 自定义模板

您可以使用&#x200B;_Handlebars_ HTML语言调整模板以用于GenStudio。 Handlebars语法使用带双大括号的常规文本作为内容占位符。 请参阅&#x200B;_Handlebars语言指南_&#x200B;中的[`What is Handlebars?`](https://handlebarsjs.com/guide/#what-is-handlebars)以了解如何准备模板。

## 模板结构

<!-- This is for email. In the future, maybe use tabs to provide guidance for other template types.
-->

如果您没有可在GenStudio中使用的HTML模板，则可以使用HTML标签定义电子邮件的结构：`DOCTYPE`、`html`、`head`和`body`。 您可以包含CSS样式以自定义电子邮件的外观。

```html
<!DOCTYPE html>
<html>
<head>
    <title>Title</title>
    <style>
    </style>
</head>
<body>
</body>
</html>
```

>[!TIP]
>
>在接下来的几个部分中，为电子邮件字段添加内容占位符，在预览中隐藏不必要的元素，并管理指向静态内容的链接。 模板准备就绪后，您可以[将其上传到GenStudio](use-templates.md#upload-a-template)，并开始根据您的自定义模板生成个性化电子邮件。

## 内容占位符

在模板的head或正文中，可以使用Handlebars语法插入内容占位符，其中要求GenStudio使用实际内容填充电子邮件。 GenStudio根据字段名称自动识别和解释内容占位符。

例如，您可以使用`{{ headline }}`来指示电子邮件标题的放置位置：

```handlebars
<div>{{ headline }}</div>
```

自定义模板中允许的最大字段数为20。

**可识别的字段名称**：

| 字段 | 角色 | 渠道模板 |
| -------------- | ---------------------- | -------------------- |
| `pre_header` | 预标题 | 电子邮件 |
| `headline` | 标题 | 电子邮件<br>社交广告 |
| `body` | 正文 | 电子邮件<br>社交广告 |
| `cta` | 行动号召 | 电子邮件<br>社交广告 |
| `on_image_text` | 在图像文本上 | 社交广告 |
| `image` | 图像 | 电子邮件<br>社交广告 |
| `brand_logo` | 所选品牌的徽标 | 社交广告 |

>[!IMPORTANT]
>
>在[!DNL Create]过程中，GenStudio会自动提供包含`subject`字段的电子邮件模板，因此无需在电子邮件模板中包含主题字段。

+++示例：基本模板

以下是电子邮件的HTML模板的基本示例。 标头包含用于样式设置的简单内联CSS。 正文包含`pre-header`、`headline`和`image`占位符，供GenStudio在电子邮件生成过程中用于插入内容。

```handlebars {line-numbers="true" highlight="13"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
    </div>
</body>
</html>
```

+++

### 背景图像

在为Meta设计广告时，必须使用由文本和品牌徽标叠加补充的背景图像，这一点很重要。 为确保图像正确缩放，元广告模板需要指定`aspect ratio`。 在此上下文中，您只能提供一个图像字段。

## 区域或组

_节_&#x200B;提供了一种通知GenStudio属于节的字段需要高度一致性的方法。 建立这种关系有助于AI生成与部分中的创意元素匹配的内容。 一个模板最多可包含三个部分。

在字段名称中使用您选择的前缀来指示此字段是节或组的一部分。 例如，您可能希望突出显示区域中显示的内容。 您可以选择使用公共前缀标识此区域的内容：

- `spotlight_headline`
- `spotlight_body`

每个部分只能有一个字段类型。 例如，上述前缀为`spotlight`的示例组只能有一个`spotlight_headline`字段。

当您有多个部分（最多三个）时：

- `headline`
- `body`
- `spotlight_headline`
- `spotlight_body`
- `news_headline`
- `news_body`

GenStudio了解`spotlight_headline`与`spotlight_body`的关系比`news_body`更密切。

+++示例：具有多个部分的模板

以下是上述示例中的相同HTML模板，但添加了两个部分。 标题包含用于样式化面板的内联CSS。 正文使用两个pod，内容占位符使用前缀。

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
        .pod {
            background-color: #f8f8f8;
            margin: 10px;
            padding: 20px;
            border-radius: 5px;
        }
        .pod h2 {
            color: #333;
        }
        .pod p {
            color: #666;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
        <div class="pod">
            <h2>{{ pod1_headline }}</h2>
            <p>This is Pod 1 content.</p>
        </div>
        <div class="pod">
            <h2>{{ pod2_headline }}</h2>
            <p>This is Pod 2 content.</p>
        </div>
    </div>
</body>
</html>
```

+++

## 模板预览

电子邮件模板有时包含不需要在GenStudio中预览的特殊内容。 您可以使用内置帮助程序控制此内容的可见性，这些帮助程序是Handlebars模板语言中的特殊表达式，可帮助执行某些操作。

在呈现模板时设置`_genStudio.browser`值，在导出模板时设置`genStudio.export`值。 例如，当模板用于导出时，您可以决定在电子邮件顶部使用条件包装器包含某些内容：

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

另一个示例可能是为了防止在GenStudio中预览电子邮件模板时使用跟踪代码。 此示例说明如何在保持预览链接干净的同时向导出的模板中的链接添加跟踪参数：

```handlebars
<a class="button" {{#if _genStudio.browser }}
   href="{{ link }}"{{/if}}{{#if _genStudio.export }}
   href="{{ link }}?trackingid=<%=getTrackingId()%>&mv=email"{{/if}}
   target="_blank">{{ cta }}</a>
```

## 静态内容

电子邮件和元模板通常链接到托管在GenStudio外部的图像和CSS文件。 当GenStudio为这些模板或从中派生的体验生成缩略图时，如果外部资源没有正确的跨源资源共享(CORS)标头，则可能会忽略这些外部资源。

要确保这些资源在缩略图生成过程中可用，请考虑两个选项：

1. **使用CORS标头**：主机服务器必须发送响应，其中生产环境的`Access-Control-Allow-Origin`标头设置为`https://experience.adobe.com`值。 此方法允许GenStudio访问并包含资源。
1. **使用数据URL**：使用数据URL将外部资源直接嵌入模板。 此方法绕过CORS限制，并确保资源在生成缩略图期间可用。
