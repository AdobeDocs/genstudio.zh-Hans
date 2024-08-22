---
title: 为性能营销人员准备用于Adobe GenStudio的电子邮件模板
description: 了解如何为性能营销人员构建自定义电子邮件模板Adobe GenStudio。
level: Intermediate
feature: Templates, Content
source-git-commit: 5bbc089fa7441ad8ce4cd84dd92889d1a22c0f61
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# 为性能营销人员准备Adobe GenStudio电子邮件模板

通常，设计人员会在设计程序(如Adobe XD)中创建模板的可视化设计。 设计、编码和测试电子邮件模板后，您可以准备将其上传并用于GenStudio中的性能营销人员。

查看[模板剖析](/help/user-guide/content/use-templates.md#anatomy-of-a-template)。

## 添加准则

在准备元广告模板之前，请确保已将[准则](/help/user-guide/guidelines/overview.md)添加到您的面向性能营销人员的GenStudio中，并为其填充了相关品牌的综合信息。 [品牌准则](/help/user-guide/guidelines/brands.md)直接影响生成的内容。

**示例**：如果您希望电子邮件模板正文不超过500个字符，请将该要求添加到“正文”字段的[渠道准则](/help/user-guide/guidelines/brands.md#channel-guidelines)中。

如果没有将准则添加到面向性能营销人员的GenStudio，则使用默认值。

## 对电子邮件模板进行编码

设计模板后，使用HTML和内联CSS对其进行编码。 对于各种设备，代码应该是干净和响应式的。

请参阅[模板示例](/help/user-guide/content/customize-template.md#template-examples)。

## 测试电子邮件模板

使用您的电子邮件投放或验证平台来测试您的电子邮件，并验证它是否在不同电子邮件客户端和设备之间正确呈现。

测试以确保您的电子邮件模板满足以下条件：

* 使用CSS媒体查询调整不同屏幕大小的布局
* 按钮可点击，可导航到目标位置
* 电子邮件模板可在移动设备上读取和使用

## 定义生成的内容区域

在电子邮件模板中定义应使用GenStudio中的内容动态填充的区域，以便进行性能营销。

要定义生成的内容区域，请执行以下操作：

* 确定GenStudio for Performance营销人员应自动生成的模板中的文本元素，例如标题或CTA。
* 通过使用Handlebars语法在HTML模板中插入占位符来调整模板。

请参阅[内容占位符](/help/user-guide/content/customize-template.md#content-placeholders)。

## 预览模板

使用内置帮助程序控制特定内容区域的可见性。 例如，您可以在导出的模板中包含指向链接的跟踪参数，同时保持预览链接干净。

请参阅[模板预览](/help/user-guide/content/customize-template.md#template-preview)。

## 上传和使用模板

设计、编码、测试和预览模板后，您可以将其上传到GenStudio以提高性能营销人员，以用于生成全新的营销内容。

请参阅[使用模板](use-templates.md)。
