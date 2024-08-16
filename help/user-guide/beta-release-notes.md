---
title: 面向性能营销人员的Adobe GenStudioBeta发行说明
description: 了解面向Performance Marketers的Adobe GenStudio的最新功能和增强功能。
source-git-commit: cbae3aeb1b8282fb64f2a6405a7ad9e07a48dbbd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# 面向性能营销人员的Adobe GenStudioBeta发行说明

这些说明重点介绍在截至8月16日的一周内进行的重大Adobe GenStudio修复和增强功能。

## 高亮

特征开发是快速和持续的。 重要的新功能包括：

### [!DNL Brands]

已增强[!DNL Brand]验证面板以改善用户体验，包括以下更改：

* **基于百分比的验证分数**：品牌验证现在以百分比的形式显示品牌验证分数，而不是通过/未通过值。

* **已更新品牌提取界面**：品牌提取现在以百分比显示提取流程的完成情况。

* **在提取期间增量加载品牌**：品牌指南现在增量加载到用户界面中。

* **复制准则架构的简化**：已从复制准则架构中删除`unique attributes`和`frequent keywords`字段，从而简化了准则设置过程。

### [!DNL Create]

* **多节电子邮件创建**：用户现在可以创建由单独的标题、图像、正文和CTA元素组成的电子邮件。

* **元广告调整大小**：创建者可以调整元广告长宽比。

### [!DNL Insights]

* **有限的Insights登录帐户**： Insights登录现在仅支持每个客户一个帐户。

## 增强功能和修复的问题

此版本包含以下其他修复。

### [!DNL Insights]

* _体验详细信息_&#x200B;页面馈送放置名称现在指定了Facebook或Instagram馈送。

* 现在，当用户从&#x200B;_资源概述_&#x200B;视图导航到&#x200B;_资源详细信息_&#x200B;视图时，大图像和视频的裁剪是一致的。

* 在用户登录之前，“属性”屏幕搜索结果计数不再显示`0 of`。<!-- GS- 3665 -->

* 单击&#x200B;**[!UICONTROL [!DNL Insights]]** > **[!UICONTROL 资产]**&#x200B;计数字段不再清除搜索和筛选设置。<!-- GS-3476 -->

## 已知问题

GenStudio for Performance Marketers GA版本将解决以下已知问题。

### 分析

* 当前未跟踪由&#x200B;**[!UICONTROL 添加模板]**&#x200B;和&#x200B;**[!UICONTROL 上传]**&#x200B;按钮触发的操作。<!-- GS-3505 -->

### [!DNL Insights]

* 无法从&#x200B;_Assets_&#x200B;播放视频。<!-- GS-3846 -->

* 用户还必须登录两次Facebook。 **解决方法**：在登录到[!DNL Insights]之前注销Facebook。

* 营销活动级别的&#x200B;**支出**&#x200B;值不准确。 目前，Facebook广告管理器与数据湖之间的数据不一致。<!-- GS-3202 -->

### [!DNL Reviews and Approvals]

* 创建者可以在获得批准后在发布之前更改资产。 这些更改不会通知批准者。

