---
title: 资源详细信息
description: GenStudio使用丰富的元数据存储经批准的内容，以便进行可搜索性和性能跟踪。
feature: Attributes, Assets
source-git-commit: ba7dced9e62f797cd43a0bd8d8263828ec5c3d5e
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---


# 资源详细信息

GenStudio使用丰富的元数据存储经批准的内容，以便进行可发现性和性能跟踪。

每个资源（包括体验和模板）都关联了&#x200B;_详细信息_（元数据），可帮助识别、跟踪、使用和学习内容性能。

资源元数据类型包括[系统元数据](#system-metadata)和[用户定义的元数据](#user-defined-metadata)。

## 系统元数据

上传资源时，会自动收集某些资源元数据。 无法编辑默认的系统元数据。

为资源存储和捕获的默认元数据包括文件名、维度、源等。

### 生成的标记

当资源获得批准并存储在[!DNL Content]中时，GenStudio会使用Adobe的AI和机器学习功能，根据资源功能（如颜色和色调）或标识资源功能的关键字生成标记。 无法编辑标记。

### 生成的内容元数据

用于生成新资源或体验的信息将成为元数据，例如所使用的提示。 内容获得批准后，您无法编辑提示，但可以将其用作生成新内容的起点。

## 用户定义的元数据

用户定义的元数据将营销上下文添加到资产的内容，使营销人员能够更好地了解如何使用及参与资产。

在[上传资源](/help/user-guide/content/manage-assets.md#add-assets)时，您可以将GenStudio中存在的一组可选资源详细信息定义为元数据。

### 元数据详细信息

下表详细列出了在创建资源时可以定义的元数据（资源详细信息）。

| 字段 | 描述 | 可编辑 | 必填 |
| ------------- | ----------- | -------- | -------- |
| 营销活动名称（项目名称） | 使用资源捕获和存储默认元数据 | Y | N |
| 品牌名称 | [[!DNL Brands]](/help/user-guide/guidelines/brands.md)已添加到GenStudio并发布以供使用 | Y | N |
| 产品 | [[!DNL Products]](/help/user-guide/guidelines/products.md)已添加到GenStudio以供使用 | Y | N |
| 角色 | [[!DNL Personas]](/help/user-guide/guidelines/personas.md)已添加到GenStudio以供使用 | Y | N |
| 渠道 | GenStudio中用于资源的内容类型，如电子邮件和元广告 | Y | N |
| 时间范围 | 资产使用的时间范围，如季度、季度、年份等。 示例： `Winter 2023` | Y | N |
| 区域 | 使用资产的区域。 示例： `North America`，`APAC`，`Italy` | Y | N |
| 语言 | 资源使用的语言。 示例： `Spanish` | Y | N |
| 关键字 | 用于标识资源用途的关键字 | Y | N |

## 查看资源详细信息

**要查看资源详细信息**：

1. 在&#x200B;_[!DNL Content]_中，选择一个资产。

1. 在资源视图中，查看右侧的&#x200B;_[!UICONTROL 详细信息]_&#x200B;部分。

   如果&#x200B;_[!UICONTROL 详细信息]_&#x200B;部分不可见，请单击&#x200B;**[!UICONTROL 信息]** (i)图标。

>[!TIP]
>
>您还可以从[!DNL Insights]查看资源详细信息。 分析提供各体验的使用情况统计和性能上下文。 在&#x200B;_[!DNL Insights]_中，选择&#x200B;**[!UICONTROL Assets]**部分。

<!-- ## History

Expand the _[!UICONTROL History]_ section to view a timeline of approvals and activity.

list other activity, show screenshot?
-->
