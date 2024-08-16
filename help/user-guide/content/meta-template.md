---
title: 为性能营销人员准备Adobe GenStudio元广告模板
description: 了解如何为性能营销人员构建自定义Adobe GenStudio元广告模板。
level: Intermediate
feature: Templates, Content
source-git-commit: c9d09801f0bd3732611b01d4a98cc7ebf38884d7
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---


# 为性能营销人员准备Adobe GenStudio元广告模板

创建元广告模板涉及为社交媒体定制的结构化方法。 设计和测试元广告模板后，您可以准备将其上传并用于GenStudio中的性能营销人员。

## 添加准则

在准备元广告模板之前，请确保已将[准则](/help/user-guide/guidelines/overview.md)添加到您的面向性能营销人员的GenStudio中，并为其填充了相关品牌的综合信息。 [品牌准则](/help/user-guide/guidelines/brands.md)直接影响生成的内容。

**示例**：如果您希望元广告模板正文不超过500个字符，请将该要求添加到“正文”字段的[渠道准则](/help/user-guide/guidelines/brands.md#channel-guidelines)中。

如果没有将准则添加到面向性能营销人员的GenStudio，则使用默认值。

## 设计模板

通常，设计人员会在设计程序(如Adobe XD)中创建模板的可视化设计。

查看[模板剖析](/help/user-guide/content/use-templates.md#anatomy-of-a-template)和[模板示例](/help/user-guide/content/customize-template.md#template-examples)。

### 广告规范

GenStudio性能营销人员支持对元广告采用以下宽高比：

* 正方形(1:1)：1080 x 1080像素
* 垂直(4:5)：1080 x 1350像素
* 文章(9:16)：1080 x 1920像素

如果广告不是按这些宽高比之一设计的，则GenStudio for Performance营销人员会自动将图像裁剪为适当的大小。

## 测试元广告模板

使用Meta的Creative Hub测试您的模板，以查看广告在不同投放位置（如信息源或故事）中的外观。

使用您的电子邮件投放或验证平台来测试您的电子邮件，并验证它是否在不同电子邮件客户端和设备之间正确呈现。

## 定义生成的内容区域

在电子邮件模板中定义应使用GenStudio中的内容动态填充的区域，以便进行性能营销。

要定义生成的内容区域，请执行以下操作：

* 确定GenStudio for Performance营销人员应自动生成的模板中的文本元素，例如标题或CTA。
* 通过使用Handblebars语法在HTML模板中插入占位符来调整模板。

请参阅[内容占位符](/help/user-guide/content/customize-template.md#content-placeholders)。

## 预览模板

利用内置帮助程序控制特定内容区域的可见性。 例如，您可以在导出的模板中包含指向链接的跟踪参数，同时保持预览链接干净。

请参阅[模板预览](/help/user-guide/content/customize-template.md#template-preview)。

## 上传和使用模板

设计、编码、测试和预览模板后，您可以将其上传到GenStudio以提高性能营销人员，以用于生成全新的营销内容。

请参阅[使用模板](use-templates.md)。
