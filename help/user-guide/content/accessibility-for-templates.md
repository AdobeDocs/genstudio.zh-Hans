---
title: 创建无障碍模板
description: 构建能够联系所有受众的模板，以便用于Adobe GenStudio性能营销人员。
feature: Templates, Content
source-git-commit: 26d1b9c7b392e93e87ffcd9444f391c2980d1c3c
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# 创建无障碍模板

Adobe致力于为所有受众提供最佳体验。 请参阅Adobe](https://www.adobe.com/trust/accessibility/initiatives.html)上的[辅助功能计划以进一步阅读。

在面向性能营销人员的GenStudio中，您可以上传可为各种体验启用内容创建的资源和模板。 遵守辅助功能标准有助于您的内容触及最大目标受众。

使用以下建议，使用最佳辅助功能标准准备模板。

## 替换文本

为非文本内容（如图像）提供替换文本。

```html
<img alt="Collage of ideas, books, man holding giant pencil, computer" src="card-create-assets.png">
```

![创意拼贴、书籍、拿着巨铅笔的男人、计算机](../../assets/card-create-assets.png){width="400"}

## 链接目的（仅限链接）

创建描述链接目的和位置的纯链接文本。

例如，使用“单击此处”或“了解更多”之类的链接文本不会清楚地描述链接的目的：

```html
<a href="product-site.html">Click here</a>
```

作为最佳实践，您应该使用清晰描述链接位置的文本。 更好的示例可能使用链接源的标题和目的：

```html
<a href="product-site.html">Explore Product Site</a>
```

## 语言

许多产品和服务都以富有创意或独一无二的方式使用语言。 避免使用行话、长句和复杂短语。 使用与目标受众兼容的清晰、简洁、易读语言。

- 尽可能使用清晰的描述、内联定义或可关联的示例。 翻译一个独特的白话可能很困难。

- 拼出或链接到首字母缩写或缩写实例的定义。 缩写可能很难翻译。

- 尽可能使用可视化元素来补充文本或复杂想法。