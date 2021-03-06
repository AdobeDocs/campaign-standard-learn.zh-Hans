---
title: 在 Adobe Campaign Standard (ACS) 中处理隐私请求 - 概述
description: 本教程介绍如何通过 Adobe Campaign Standard 界面创建隐私请求。
feature: Privacy Tools
kt: 1480
doc-type: feature video
activity: use
team: TM
recommendations: noDisplay
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: ht
source-wordcount: '349'
ht-degree: 100%

---

# 通过 Adobe Campaign Standard 用户界面处理隐私请求

Adobe Campaign 为数据控制者提供了三种方法，以符合 GDPR（通用数据保护条例）和 CCPA（加州消费者隐私法案）等隐私法案的方式执行个人身份信息数据的隐私访问和删除请求：

* **通过隐私核心服务集成：**&#x200B;从 [!UICONTROL Privacy Service] 推送到所有 Experience Cloud 解决方案的隐私请求会通过专门工作流程由 Campaign 自动处理。要了解如何从隐私核心服务创建隐私请求，请参阅 [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)

* **通过 API：** Adobe Campaign 提供一个 API，允许使用 REST 自动处理隐私请求

* **通过 Adobe Campaign 界面：**&#x200B;数据控制者在 Adobe Campaign 中为每项隐私请求创建新的隐私请求

>[!NOTE]
>
> **ACS 19.4 中的更改：**
> 
> [Privacy Service 集成](https://www.adobe.io/apis/experienceplatform/gdpr.html)是您应当用于所有访问和删除请求的方法。从 19.4 版开始，将 Campaign API 和接口用于访问和删除请求的方法已被弃用。有关 Campaign Standard 的已弃用和已删除功能的详细信息，请参阅[此页面](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=zh-Hans)。
>
>**选择禁用个人信息销售 (CCPA)**
>
> 在 Campaign 界面和 API 中提供现成的“CCPA 选择禁用”字段。
>
> 您可以检查版本，单击右上角的 **?** 图标，然后选择“关于”。

## 视频教程

### 隐私请求的先决条件

1. [创建命名空间](/help/privacy/namespaces-for-privacy-requests.md)
1. [修改自定义资源](/help/privacy/custom-resources-for-privacy-requests.md)

### 通过 Adobe Campaign 用户界面创建、跟踪和执行隐私请求

* [通过 Adobe Campaign 用户界面创建和跟踪隐私请求](/help/privacy/create-and-track-privacy-requests.md)
* [执行隐私请求](/help/privacy/execute-privacy-requests.md)

## 其他资源

* [Campaign 的一般隐私准则](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=zh-Hans#getting-started)
* [ACS 的 CCPA 合规](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=zh-Hans#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [Adobe Campaign Standard REST API 文档](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
