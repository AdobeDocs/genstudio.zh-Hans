---
title: Assets概述
description: 了解如何在Adobe GenStudio for Performance Marketing中评估资源性能。
feature: Insights, Assets
source-git-commit: bd3c5c9ff12c962d4123ac992fb74cd94e184172
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Assets概述

[!DNL Insights] _[!UICONTROL Assets]_&#x200B;视图显示在所选渠道帐户的体验和广告营销活动中使用的资源列表。

_[!UICONTROL Assets]_&#x200B;图库是默认视图，该视图显示资源预览拼合和量度（如点进率）。 单击图库右侧上方的设置(cog)图标可切换以下三个可视量度之一：

- `click-through rate` (CTR)
- `cost per click` (CPC)
- `spend`

_[!UICONTROL Assets]_&#x200B;表是使用[!UICONTROL 资源ID]组织的。 表格左上方的筛选器（漏斗）图标会打开&#x200B;**[!UICONTROL 筛选器]**&#x200B;菜单，您可以从多个列表中进行选择。

![Assets筛选器和表](/help/assets/insights-assets-filter.png){zoomable="yes"}

您可以使用视图列表（表格）图标和图库视图（网格）图标在视图之间切换。

## 资源详细信息

_资源_&#x200B;是已批准用于营销计划的图像、视频、文本或其他创意内容。

在资源详细信息视图中，您可以看到哪些体验使用了所选资源。 详细信息包括总资源性能、用户定义的属性以及与该资源关联的AI检测功能。

![资源详细信息](/help/assets/insights-asset-details.png){zoomable="yes"}

## 资产量度

分析量度可以帮助您评估哪些资产对活动取得成功做出了贡献以及哪些资产属性最有效。

### 量度详细信息

下表提供了[!UICONTROL Assets]视图中关键数字营销指标的定义和见解。 每个量度都包括与资产相关的简短定义、量度的计算方式以及一个或多个见解，以帮助了解其重要性及其对资产的影响。

| 量度 | 定义 | Insight |
| ---------------------- | ----------------------------- | -------------------------------- |
| **[!UICONTROL 资产ID]** | 与此资源关联的名称。 | 单击任何关键量度的列标题可对表进行排序。 |
| **[!UICONTROL 展示次数]** | 每次在渠道中加载资源时的计数，不考虑交互或查看。 | 高展示次数计数可能表示广泛的可见性，但为了获得真正的性能洞察，请考虑其他参与量度。 |
| **[!UICONTROL 次点击]** | 用户与资源上的可单击元素（例如链接）进行交互的次数。 | 高点击数表示对内容非常感兴趣并参与其中，这可能有效并影响合适的受众。 |
| **[!UICONTROL CTR &#x200B;]**<br>_点进率_ | 导致体验内资产点击的展示次数百分比(%)。<br>**计算**：`clicks`除以`impressions` | 高点进率表明，内容在消息传递和设计中与受众高度相关且具有激励性，能够有效地定位受众的兴趣。 |
| **[!UICONTROL CPM &#x200B;]**<br>_每千成本_ | 资产每千次广告展示的成本($)。<br>**计算**：总金额`spent`除以范围，然后乘以1000 | 低值可能表示可视性具有成本效益，尤其是与高点进率配对时。 |
| **[!UICONTROL CPC &#x200B;]**<br>_每次点击成本_ | 与每次单击资产关联的平均成本($)。<br>**计算**：总金额`spent`除以`clicks` | 平均成本降低可能表明广告支出具有成本效益，尤其是与转化率提高相比。 |
| **[!UICONTROL 支出]** | 在指定时间段内从预算中花费的金额($)，因为它与单个资产相关。 | 在短时间内高支出量可能表示使用迅速，这可能导致资源提前耗尽。 根据关键绩效指标跟踪支出金额，以帮助监控总体投资回报。 |
| **[!UICONTROL 属性]** | 已检测到并已应用于此资源的属性列表。 | |
