---
title: GenStudio入门
description: 了解如何设置GenStudio以生成新的品牌整合营销内容。
level: Beginner
feature: Prompt, Brands Service, Personas Service, Products Service, Generative AI, Guidelines
source-git-commit: 2501d1e36f76d1534a735b9147fb42f762a665e8
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 1%

---


# GenStudio入门

GenStudio是一个全面的平台，用于创建、评估和管理可反映并遵循您的品牌识别的营销体验。

利益相关者对其多种功能的访问权限由分配的用户角色控制。 您分配的用户角色决定了您可以在GenStudio中执行的任务。 GenStudio管理员会设置您的权限，这些权限在欢迎电子邮件中定义。

如果您不熟悉基于创作的人工智能工具，或只是想知道如何运用GenStudio的核心原则，请参阅[GenStudio概念](concepts.md)和[编写有效的提示](effective-prompts.md)。

## GenStudio用户角色

创建和部署现代营销活动需要具有不同责任和技能的利益相关者之间的协作。

三种类型的GenStudio用户角色支持这种多样化的组织角色。 权限针对其中每种用户类型量身定制，并支持每个用户在营销组织中的职责。

**三种用户角色类型为**：

* **创建者**&#x200B;使用GenStudio的创作AI功能创建营销活动资源、请求内容审查和批准以及发布此内容的已批准草稿。 创建者将资产保存到Content后，所有GensStudio用户都可以访问和使用资产。

* **协作者**&#x200B;是范围最广的GenStudio用户。 协作者可以查看和批准GenStudio内容，是工作流的重要组成部分，可确保生成的内容符合贵组织的需求和标准。

* **系统管理员**&#x200B;在GenStudio中拥有最广泛的权限集。 系统管理员可以从Genstudio添加和删除用户和内容。 管理员执行基本入门任务，为营销活动资产创建和部署建立基本保障。 管理员通过上传品牌和组织特定的信息（如[品牌指南](/help/user-guide/guidelines/overview.md)）来实施这些护栏。

>[!NOTE]
>在将任何用户配置为这些角色之前，必须在Adobe管理控制台中将管理员指定为超级用户，才能执行一次性设置任务。 此超级用户角色仅在Adobe Admin Console的上下文中运行。 它在GenStudio平台界面中没有角色。 GenStudio角色分配中没有超级用户的概念。

### 创建者

**创建者**&#x200B;具有创建GenStudio [!DNL Brands]、[!DNL Campaigns]和[!DNL Content]资源所需的核心权限。 他们还可以编辑和删除自己创建的资产。 GenStudio支持快速创建数百个内容。 这些用户可以生成内容片段或整个体验，这些片段或体验可以编排已批准内容的离散片段，以满足特定营销活动的需求。

创建者通过&#x200B;_提示_&#x200B;与GenStudio的创作AI技术交互。 GenStudio在画布中的提示区域提供了一些工具，用于在特定营销活动准则的上下文中放置提示。 因此，生成的内容的质量和成功部分取决于贵组织上传的品牌指南的质量以及提示的特定性。

请参阅[编写有效的提示](effective-prompts.md)。

下表显示了默认的GenStudio创建者权限：

| 专题 | 创建 | 更新 | 删除 | 查看 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 否 | 否 | 否 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 只能配置ad连接器 |    |     | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 是 | 是 | 是 | 是 |

### 协作者

**协作者**&#x200B;可以在GenStudio中查看资源，但不能创建、编辑或删除这些资源。 协作者包括一些利益相关者，他们对GenStudio内容的审阅和批准流程取得成功至关重要，但不需要创建或直接编辑内容。 法律专家和创建者的经理是潜在合作者的示例。 GenStudio协作者可能有权在其他Creative Cloud产品中创建和查看资源。

下表显示默认的GenStudio Collaborator权限：

| 专题 | 创建 | 更新 | 删除 | 查看 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 是 | 是 | 是 | 是 |
| [!DNL Campaigns] | 是 | 是 | 是 | 是 |
| [!DNL Content] | 是 | 是 | 是 | 是 |
| [!DNL Insights] | 否 | 否 | 否 | 是 |
| [!DNL Personas] | 是 | 是 | 是 | 是 |
| [!DNL Products] | 是 | 是 | 是 | 是 |
| [!DNL Reviews and approvals] | 否 | 否 | 否 | 是 |

### 管理员

管理员用户可创建用户并将其分配给任何GenStudio支持的角色。 他们可以根据需要向各个创建者或协作者分配新权限。 他们最关键的工作是完成初始入门培训任务，让您的组织做好部署GenStudio的准备。

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


## 准备GenStudio以生成内容

系统管理员准备其组织的GenStudio环境，以便创建者和协作者创建活动资源。 这些初步设置任务包括：

1. [为[!DNL Brands]、[!DNL Products]和[!DNL Personas]设置准则](./guidelines/overview.md)。 设置贵组织3月&#x200B;**[的关键构建块将准则](./guidelines/overview.md)** （[!DNL Brands]、[!DNL Products]和[!DNL Personas]）添加到GenStudio。 设置组织品牌标识的关键构建块是GenStudio创建者和协作者工作的重要先决条件。 您可以上传品牌准则文档或手动输入品牌信息。
   * **准备您的指南文档**。 品牌指南的描述性越强、内容越全面，GenStudio的输出效果就越好。 包含您认为对品牌至关重要的功能的简短示例，并添加要从GenStudio内容创建中排除的行为描述。 GenStudio会从这些上传的文档中提取信息，并开始构建您的品牌。 品牌声音、渠道和图像指南等信息，将填充为GenStudio从您上传的文档中汇编每个指南。
   * **根据需要编辑或完成品牌指南字段**。 全面的品牌指南构成了GenStudio了解您组织品牌的基础。 GenStudio从品牌准则文档中提取所需信息后，系统会提示您手动编辑或填写提取信息的字段。 通过添加[!DNL Product]指定内容创建的各个产品焦点区域。 [!DNL Personas]指南帮助为定义的客户区段定制内容创建。

   虽然设置组织的品牌指南可能只是一次性操作，但您可能需要根据组织的波动、增长和不断变化的市场环境修订和增强这些指南。

1. **[上载模板](./content/use-templates.md)**。 模板提供了快捷方式并加快了内容创建。 模板包含批准的功能（如页眉和页脚），并为内容创建建立防护。 管理员通常会为其组织上传和管理模板。 创建者使用模板在组织品牌的既定范围内快速启动内容创建过程。

1. **[上传已批准的资源](./content/manage-assets.md)**。 GenStudio [!DNL Content]中已批准的资源可供所有GenStudio创建者使用。 您可以使用创建者可用于创建新体验或资源的资源为[!DNL Content]提供种子。

1. **[连接到元(Facebook)帐户](./insights/connect-channel.md)**。 您必须在GenStudio与贵组织的社交帐户之间配置连接，以接收来自有效营销活动、资源和体验的数据。 GenStudio [Insights](./insights/overview.md)提供了用于分析渠道派生数据的工具。
