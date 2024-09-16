---
title: 面向性能营销人员的Adobe GenStudio入门
description: 了解如何为性能营销人员设置GenStudio以生成新的品牌一致营销内容。
level: Beginner
feature: Prompt, Brands Service, Personas Service, Products Service, Generative AI, Guidelines
exl-id: bcb03198-bbcb-45ae-af01-25c1e834b563
source-git-commit: 333d32757a4327d8f8a54b25cb5c08ce2b3e2771
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 1%

---

# 面向性能营销人员的Adobe GenStudio入门

GenStudio for Performance Marketers是一个全面的平台，用于创建、评估和管理可反映并遵守您品牌标识的营销体验。

利益相关者对其多种功能的访问权限由分配的&#x200B;_用户角色_&#x200B;控制。 您分配的用户角色决定了您可以在GenStudio中为性能营销人员执行的任务。 Adobe系统管理员在Adobe Admin Console的GenStudio for Performance Marketers产品配置文件中分配您的权限。 您的欢迎电子邮件将标识您分配的角色。

如果您不熟悉基于创作的人工智能工具，或只是想知道关于GenStudio性能营销人员的核心原则，请参阅[概念](concepts.md)和[编写有效的提示](effective-prompts.md)。

## 用户角色

创建和部署现代营销活动需要具有不同责任和技能的利益相关者之间的协作。

三种类型的GenStudio for Performance Marketers用户角色支持这种多样化的组织角色。 权限针对其中每种用户类型量身定制，并支持每个用户在营销组织中的职责。

**三种用户角色类型为**：

* **编辑者**&#x200B;使用GenStudio for Performance Marketers的创作AI功能创建营销活动资源、请求内容审查和批准以及发布此内容的已批准草稿。 创建者将资源保存到“内容”后，所有GenStudio用户都可以访问和使用资源。

* **协作者**&#x200B;是面向性能营销人员用户的最广泛的GenStudio。 协作者可以查看和批准内容，并且是工作流的重要组成部分，可确保生成的内容符合贵组织的需求和标准。

* **系统管理员**&#x200B;在GenStudio中为性能营销人员拥有最广泛的权限集。 系统管理员执行基本入门任务，为营销活动资产的创建和部署建立基本保障。 系统管理员通过上传品牌和组织特定的信息（如[品牌准则](/help/user-guide/guidelines/overview.md)）来实施这些护栏。 GenStudio系统管理员有权创建和发布品牌，但没有用户管理权限。

>[!NOTE]
>在将任何用户配置到这些角色中之前，必须在Adobe Admin Console中指定Adobe系统管理员以执行一次性设置任务。 此Adobe管理员角色仅在Adobe Admin Console的上下文中运行。 它在GenStudio for Performance Marketers平台界面中没有角色。

### GenStudio编辑器

**编辑者**&#x200B;具有为Performance Marketers [!DNL Brands]、[!DNL Campaigns]和[!DNL Content]资源创建GenStudio所需的核心权限。 他们还可以编辑和删除自己创建的资产。 GenStudio性能营销人员支持快速创建数百个内容。 这些用户可以生成内容片段或整个体验，这些片段或体验可以编排已批准内容的离散片段，以满足特定营销活动的需求。

编辑人员通过&#x200B;_提示_&#x200B;与GenStudio交互，以获得性能营销人员的创作AI技术。 画布中的提示区域提供了一些工具，用于在特定营销活动准则的上下文中放置提示。 因此，生成的内容的质量和成功部分取决于贵组织上传的品牌指南的质量以及提示的特定性。

请参阅[编写有效的提示](effective-prompts.md)。

下表显示了默认编辑器权限：

| 专题 | 创建 | 更新 | 删除 | 查看 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 否 | 否 | 否 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 只能配置ad连接器 |    |     | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 是 | 是 | 是 | 是 |

### GenStudio协作者

**协作者**&#x200B;可以在GenStudio中查看性能营销人员资源，但不能创建、编辑或删除这些资源。 协作者包括对内容的审阅和批准流程取得成功至关重要的利益相关者，但他们不需要创建或直接编辑内容。 法律专家和创建者的经理是潜在合作者的示例。 GenStudio for Performance营销人员协作者可能有权在其他Creative Cloud产品中创建和查看资源。

下表显示默认的Collaborator权限：

| 专题 | 创建 | 更新 | 删除 | 查看 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 否 | 否 | 否 | 是 |
| [!DNL Campaigns] | 否 | 否 | 否 | 是 |
| [!DNL Content] | 否 | 否 | 否 | 是 |
| [!DNL Insights] | 否 | 否 | 否 | 是 |
| [!DNL Personas] | 否 | 否 | 否 | 是 |
| [!DNL Products] | 否 | 否 | 否 | 是 |
| [!DNL Reviews and approvals] | 否 | 否 | 否 | 是 |

### GenStudio系统管理员

**GenStudio系统管理员**&#x200B;完成初始任务，让您的组织为部署面向性能营销人员的GenStudio做好准备。

下表显示默认的GenStudio系统管理员权限：

| 专题 | 创建 | 更新 | 删除 | 查看 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 是 | 是 | 是 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 是 | 是 | 是 | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 是 | 是 | 是 | 是 |


## 准备GenStudio以供性能营销人员生成内容

GenStudio系统管理员准备其组织的GenStudio for Performance Marketers环境，以供编辑和协作者创建营销活动资产。 这些初步设置任务包括：

1. [为[!DNL Brands]、[!DNL Products]和[!DNL Personas]添加准则](./guidelines/overview.md)。 设置组织品牌标识的关键构建块是创建者和协作者工作的重要先决条件。 您可以上传品牌准则文档或手动输入品牌信息。
   * **准备您的指南文档**。 品牌指南的描述性越强、内容越全面，效果越好。 包含您认为对品牌至关重要的功能的简短示例，并添加要从内容创建中排除的行为描述。 GenStudio性能营销人员会从这些上传的文档中提取信息，并开始构建您的品牌。 品牌声音、渠道和图像准则等信息，填充为GenStudio绩效营销人员从您上传的文档中汇编每个准则。
   * **根据需要编辑或完成品牌指南字段**。 全面的品牌指南构成了GenStudio绩效营销人员了解您组织品牌的基础。 GenStudio for Performance营销人员从品牌指南文档中提取所需信息后，系统会提示您手动编辑或填写提取信息的字段。 通过添加[!DNL Product]指定内容创建的各个产品焦点区域。 [!DNL Personas]指南帮助为定义的客户区段定制内容创建。

   虽然设置组织的品牌指南可能只是一次性操作，但您可能需要根据组织的波动、增长和不断变化的市场环境修订和增强这些指南。

1. **[上载模板](./content/use-templates.md)**。 模板提供了快捷方式并加快了内容创建。 模板包含批准的功能（如页眉和页脚），并为内容创建建立防护。 系统管理员通常为其组织上传和管理模板。 创建者使用模板在组织品牌的既定范围内快速启动内容创建过程。

1. **[上传已批准的资源](./content/manage-assets.md)**。 [!DNL Content]中的已批准资源可供所有GenStudio性能营销人员创建。 您可以使用创建者可用于创建新体验或资源的资源为[!DNL Content]提供种子。

1. **[连接到元(Facebook)帐户](./insights/connect-channel.md)**。 在面向绩效营销人员的GenStudio与贵组织的社交帐户之间配置连接，以接收来自有效营销活动、资源和体验的数据。 [[!DNL Insights]](./insights/overview.md)提供了用于分析渠道派生数据的工具。
