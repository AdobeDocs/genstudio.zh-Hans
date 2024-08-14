---
title: 自定义模板
description: 了解如何为GenStudio构建自定义模板。
level: Intermediate
feature: Templates, Content
source-git-commit: d7d11077d35a4c1924e4be456c00b1fae24e0a1b
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---


# 自定义模板

您可以使用&#x200B;_Handlebars_ HTML语言调整模板以用于GenStudio。 Handlebars语法使用带双大括号的常规文本作为内容占位符。 请参阅&#x200B;_Handlebars语言指南_&#x200B;中的[`What is Handlebars?`](https://handlebarsjs.com/guide/#what-is-handlebars)以了解如何准备模板。

<!-- This is for email. In the future, maybe use tabs to provide guidance for other template types.
-->If you do not have an HTML template ready to use in GenStudio, you can start by defining the structure of your email using HTML tags: `DOCTYPE`, `html`, `head`, and `body`. You can include CSS styles to customize the appearance of your email.

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

请参阅[模板示例](#template-examples)。

>[!TIP]
>
>在接下来的几个部分中，为电子邮件字段添加内容占位符，请参阅示例模板，在预览中隐藏不必要的元素，以及管理指向静态内容的链接。 模板准备就绪后，您可以[将其上传到GenStudio](use-templates.md#upload-a-template)，并开始根据您的自定义模板生成个性化电子邮件。

## 内容占位符

在模板的head或body中，可以使用Handlebars语法插入内容占位符，其中需要GenStudio使用实际内容填充模板。 GenStudio根据字段名称自动识别和解释内容占位符。

例如，您可以使用`{{ headline }}`来指示电子邮件标题的放置位置：

```handlebars
<div>{{ headline }}</div>
```

### 字段名称

自定义模板中允许的最大字段数为20。

#### 可识别的字段名称

下表列出了GenStudio识别用于填充到模板中的字段名称。

| 字段 | 角色 | 渠道模板 |
| -------------- | ---------------------- | -------------------- |
| `pre_header` | 预标题 | 电子邮件（推荐） |
| `headline` | 标题 | 电子邮件（推荐）<br>元广告 |
| `body` | 正文 | 电子邮件（推荐）<br>元广告 |
| `cta` | 行动号召 | 电子邮件（推荐）<br>元广告 |
| `on_image_text` | 在图像文本上 | 元广告（推荐） |
| `image` | 图像 | 电子邮件（推荐）<br>元广告（推荐） |
| `brand_logo` | 所选品牌的徽标 | 元广告 |

GenStudio会自动填充模板中的某些字段，因此没有必要将它们包含在模板设计中：

* `subject`字段（电子邮件模板）
* `headline`、`body`和`CTA`字段（元广告模板）

>[!WARNING]
>
>对于Instagram广告，生成的标题不会显示在最终体验中。

#### 品牌徽标字段名称

要在模板中添加品牌徽标，请使用以下代码呈现默认徽标：

```{{#if brand_logo}}{{brand_logo}}{{else}} encoded inline logo {{/if}}```

#### 手动字段名称

所有其他字段名称均被视为手动填充的字段。 如果希望某个节是可编辑的，请在要编辑的节周围添加双括号。

> 示例： ``{{customVariable}}`` （customVariable是手动可编辑的部分）

## 区域或组

_节_&#x200B;通知GenStudio，此节中的字段需要高度一致性。 建立这种关系有助于AI生成与部分中的创意元素匹配的内容。

在字段名称中使用您选择的前缀来指示字段是部分或组的一部分。

例如，您可能希望突出显示区域中显示的内容：

* `spotlight_headline`
* `spotlight_body`

每个部分只能有一个字段类型。 在上述示例中，`spotlight`前缀只能有一个`spotlight_headline`字段。

一个模板最多可以包含三个部分：

* `headline`
* `body`
* `spotlight_headline`
* `spotlight_body`
* `news_headline`
* `news_body`

GenStudio了解`spotlight_headline`与`spotlight_body`的关系比`news_body`更密切。

## 模板示例

+++示例：带一个部分的电子邮件模板

以下是包含一节的电子邮件的HTML模板的基本示例。 标头包含用于样式设置的简单内联CSS。 正文包含`pre-header`、`headline`和`image` [占位符](#content-placeholders)，供GenStudio在电子邮件生成过程中用于插入内容。

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

+++示例：具有多个部分的电子邮件模板

以下是上述示例中的相同HTML模板，但添加了两个部分。 标头包含用于设置组样式的内联CSS。 正文使用两个组，其中[个内容占位符](#content-placeholders)使用前缀。

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

+++示例：元广告模板

以下是元广告模板的基本示例。 标头包含用于样式化的内联CSS。 正文使用带有前缀的[内容占位符](#content-placeholders)。

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adobe</title>
    <style>
        .ad-container {
            width: 300px;
            border: 1px solid #ddd;
            padding: 16px;
            font-family: Arial, sans-serif;
        }
        .ad-image {
            width: 100%;
            height: auto;
        }
        .ad-headline {
            font-size: 18px;
            font-weight: bold;
            margin: 12px 0;
        }
        .ad-body {
            font-size: 14px;
            margin: 12px 0;
        }
        .ad-cta {
            display: inline-block;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            text-decoration: none;
            border-radius: 4px;
            text-align: center;
        }
    </style>
</head>
<body>
<div class="ad-container">
    <img src="{{ image }}" alt="Ad Image" class="ad-image">
    <div class="ad-headline">"{{ headline }}"</div>
    <div class="ad-body">"{{ body }}"</div>
    <a href="(https://example.com)" class="ad-cta">"{{ CTA }}"</a>
</div>

</body>
</html>
```

+++

## 模板预览

使用内置帮助程序（Handlebars模板语言中可执行特定操作的特殊表达式）控制特殊内容的可见性。 例如，您可以向导出的模板中的链接添加跟踪参数，同时保持预览链接干净。

在呈现模板时设置`_genStudio.browser`值，在导出模板时设置`genStudio.export`值。 例如，当模板用于导出时，您可以决定在电子邮件顶部使用条件包装器包含某些内容：

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

另一个示例可能是为了防止在GenStudio中预览模板时使用跟踪代码。 此示例说明如何在保持预览链接干净的同时向导出的模板中的链接添加跟踪参数：

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
