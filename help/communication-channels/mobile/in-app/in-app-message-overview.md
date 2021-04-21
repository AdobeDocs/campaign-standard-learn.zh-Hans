---
title: 应用程序内消息简介
description: 了解如何根据客户在移动应用程序中的实时行为向用户呈现上下文相关的应用程序内消息。
feature: 应用程序内
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: Business Practitioner
level: Beginner
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 12%

---

# [!UICONTROL In-App]消息{#introduction}简介

[!UICONTROL In-App Messaging]渠道允许您在用户在移动应用程序中处于活动状态时显示消息。 此渠道要求移动应用程序与[!UICONTROL Adobe Experience Platform SDK]集成。

本教程将说明设置移动属性([!UICONTROL In-App Messaging]渠道的[!UICONTROL Launch]扩展)所需的步骤，以及如何在Adobe Campaign Standard中准备、自定义和发送[!UICONTROL In-App]消息。 这些链接将带您观看每个高亮主题的视频教程。

## 先决条件{#prerequisites}

1. 确保可以访问&#x200B;**[!UICONTROL In-App]**&#x200B;渠道。 如果您无法访问这些渠道，请与帐户管理团队联系。
1. 验证您的&#x200B;**用户**&#x200B;是否在Adobe Campaign Standard和[!UICONTROL Launch]中具有必需的&#x200B;**权限**。

   1. 在Adobe Campaign Standard中，确保IMS用户是[!UICONTROL Standard User]和[!UICONTROL Administrator]组的一部分。\
      此步骤允许用户登录Adobe Campaign Standard，导航到Experience Platform SDK移动应用程序页面，并视图您在[!UICONTROL Launch]中创建的移动应用程序属性。
   1. 在[!UICONTROL Launch]中，确保您的IMS用户是[!UICONTROL Launch]产品用户档案的一部分。\
      此步骤允许用户登录到[!UICONTROL Launch]以创建和视图属性。 有关[!UICONTROL Launch]中产品用户档案的详细信息，请参阅[创建产品用户档案](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)。 在产品用户档案中，公司或属性上不应设置任何权限，但用户仍应能够登录。

1. 在Adobe Experience Platform Launch:

   1. 通过创建移动属性创建移动应用程序，并使用Experience Platform SDK仪表您的移动应用程序。
   1. 为您的移动应用程序安装&#x200B;**Adobe Campaign Standard**&#x200B;扩展。

有关扩展的详细信息，请参阅[!UICONTROL Adobe Launch ]文档中的[在Adobe Launch](Https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard)中配置Campaign Standard扩展。

## 设置[!UICONTROL In-App]消息{#steps-to-set-up}的步骤

1. [使用 Adobe Experience Platform SDK 配置移动应用程序](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [配置事件](/help/communication-channels/mobile/in-app/configure-events.md)。

## 创建、管理和发布[!UICONTROL In-App]投放{#create-manage-publish}

您可以单击主页中[!UICONTROL Marketing Activities]的&#x200B;**[!UICONTROL Create an In-App Message]**&#x200B;卡来创建一次应用程序内投放，也可以在工作流](/help/communication-channels/mobile/in-app/in-app-activity.md)中创建[应用程序内投放。

设置投放时，您有三个选项，可通过从不同投放模板中进行选择来目标用户：

1. [**广播应用程序内消**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) 息以目标移动应用程序的所有用户。

   此消息类型允许您向移动应用程序的所有用户（当前或将来）发送消息，即使他们没有Adobe Campaign中的现有用户档案。 因此，在自定义消息时不可能进行个性化，因为用户档案中不一定存在用户Adobe Campaign。

1. 目标所有用户的移动App用户档案。

   此消息类型允许您目标具有Adobe Campaign中移动用户档案的移动应用程序的所有已知或匿名用户。 此消息类型可仅使用非个人属性和非敏感属性进行个性化，并且不需要 Mobile SDK 与 Adobe Campaign 的应用程序内消息传递服务之间进行安全握手。因此，个性化策略基于您从用户与设备的交互中了解到的信息。 例如，目标在上周启动其App超过5次的所有用户。

1. [**基于 Campaign 用户档案的目标用户**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   此消息类型允许您目标已订阅您的移动应用程序的Adobe Campaign用户档案(CRM用户档案)。 该消息可以通过Adobe Campaign中所有可用的用户档案属性进行个性化，但需要Mobile SDK与活动的应用程序内消息传递服务之间进行安全握手，以确保包含个人和敏感信息的消息仅由授权用户使用。

此模板有助于支持跨渠道业务流程使用案例，在这些案例中，您已经将用户定向到其他渠道（如“电子邮件”或“推送”），并且根据用户的响应，您希望通过应用程序内消息与他们互动。

## 有关应用程序内投放的报告{#report}

投放发布后，您可以[报告应用程序内投放](/help/communication-channels/mobile/in-app/in-app-reporting.md)。

## 其他资源

* [应用程序内报告](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [设置移动属性](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [使用Adobe Experience Platform SDK配置移动应用程序](https://helpx.adobe.com/cn/campaign/kb/configuring-app-sdk.html)
* [准备和发送应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [自定义应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [在工作流中发送应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [启用生命周期指标](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
