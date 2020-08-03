---
title: Adobe Campaign Standard(ACS)隐私请求——概述
description: 本教程介绍如何通过Adobe Campaign Standard(ACS)界面创建隐私请求。
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 1%

---


# 通过Adobe Campaign Standard用户界面提出隐私请求

Adobe Campaign优惠数据管理者根据隐私法(如GDPR（一般数据保护规定）和CCPA（加利福尼亚州消费者隐私法）)执行PII数据隐私访问和删除请求的三种方法：

* **通过隐私核心服务集成：** 活动通过专用工 [!UICONTROL Privacy Service] 作流程自动处理从所有Experience Cloud解决方案推送的隐私请求。 请参阅 [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) ，了解如何从隐私核心服务创建隐私请求

* **通过API:** Adobe Campaign提供一个API，允许使用REST自动处理隐私请求

* **通过Adobe Campaign界面：** 对于每个隐私请求，Adobe Campaign控制器在

>[!NOTE]
>
> **ACS 19.4的更改：**
> 
> Privacy Service [集成](https://adobe.io/apis/cloudplatform/gdpr.html) 是您应用于所有访问和删除请求的方法。 从19.4开始，已弃用活动API和接口访问和删除请求。 有关Campaign Standard已弃用和已删除功能的详细信息，请 [参阅此页](https://helpx.adobe.com/cn/campaign/kb/acs-deprecated-and-removed-features.html)。
>
>**选择退出个人信息销售(CCPA)**
>
>从19.4开始，在活动界面和API中提供了现成的CCPA退出字段。 对于19.3，要利用此信息，您需要以Adobe Campaign Standard创建此字段。 有关详细信息， [请参阅](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa) 详细的文档。
>
> 单击？ 图标，然后选择“关于”。

## 视频Tutorials

### 隐私请求的先决条件

1. [创建命名空间](/help/privacy/namespaces-for-privacy-requests.md)
1. [修改自定义资源](/help/privacy/custom-resources-for-privacy-requests.md)

### 通过Adobe Campaign用户界面创建、跟踪和执行隐私请求

* [通过Adobe Campaign用户界面创建和跟踪隐私请求](/help/privacy/create-and-track-privacy-requests.md)
* [执行隐私请求](/help/privacy/execute-privacy-requests.md)

## 其他资源

* [活动的一般隐私准则](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html)
* [CCPA for ACS](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Adobe Campaign StandardREST API文档](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
