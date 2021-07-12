---
title: 应用程序内消息简介
description: 了解如何向用户展示与上下文相关的应用程序内消息，以响应客户在移动应用程序中的实时行为。
feature: 应用程序内
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 12%

---

# [!UICONTROL In-App]消息简介 {#introduction}

[!UICONTROL In-App Messaging]渠道允许您在用户在移动应用程序中处于活动状态时显示消息。 此渠道要求将移动应用程序与[!UICONTROL Adobe Experience Platform SDK]集成。

本教程将介绍设置移动属性（[!UICONTROL In-App Messaging]渠道的[!UICONTROL Launch]扩展）以及如何在Adobe Campaign Standard中准备、自定义和发送[!UICONTROL In-App]消息所需的步骤。 这些链接将引导您查看有关每个突出显示主题的视频教程。

## 先决条件 {#prerequisites}

1. 确保可以访问&#x200B;**[!UICONTROL In-App]**&#x200B;通道。 如果您无法访问这些渠道，请与帐户管理团队联系。
1. 验证您的&#x200B;**用户**&#x200B;是否在Adobe Campaign Standard和[!UICONTROL Launch]中具有必要的&#x200B;**权限**。

   1. 在Adobe Campaign Standard中，确保IMS用户是[!UICONTROL Standard User]和[!UICONTROL Administrator]组的一部分。\
      此步骤允许用户登录Adobe Campaign Standard，导航到Experience PlatformSDK移动设备应用程序页面，并查看您在[!UICONTROL Launch]中创建的移动设备应用程序属性。
   1. 在[!UICONTROL Launch]中，确保您的IMS用户是[!UICONTROL Launch]产品配置文件的一部分。\
      此步骤允许用户登录到[!UICONTROL Launch]以创建和查看属性。 有关[!UICONTROL Launch]中产品配置文件的更多信息，请参阅[创建产品配置文件](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)。 在产品配置文件中，不应对公司或资产设置任何权限，但用户仍应能够登录。

1. 在Adobe Experience Platform Launch:

   1. 通过创建移动资产创建移动应用程序，并使用Experience PlatformSDK来设计移动应用程序。
   1. 为移动应用程序安装&#x200B;**Adobe Campaign Standard**&#x200B;扩展。

有关扩展的更多信息，请参阅[!UICONTROL Adobe Launch ]文档中的[在AdobeLaunch](Https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard)中配置Campaign Standard扩展。

## 设置[!UICONTROL In-App]消息的步骤 {#steps-to-set-up}

1. [使用 Adobe Experience Platform SDK 配置移动应用程序](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [配置事件](/help/communication-channels/mobile/in-app/configure-events.md)。

## 创建、管理和发布[!UICONTROL In-App]投放 {#create-manage-publish}

您可以通过单击主页中的&#x200B;**[!UICONTROL Create an In-App Message]**&#x200B;卡片（位于[!UICONTROL Marketing Activities]中）创建一次应用程序内投放，也可以通过在工作流中[创建应用程序内投放（位于](/help/communication-channels/mobile/in-app/in-app-activity.md)中）。

在设置投放时，您可以通过从不同的投放模板中进行选择来定位用户，具有三个选项：

1. [**广播应用程序内消**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) 息以定位移动应用程序的所有用户。

   利用此消息类型，可向移动应用程序的所有用户（当前或未来）发送消息，即使他们当前在Adobe Campaign中没有用户档案。 因此，在自定义消息时不可能进行个性化，因为用户配置文件不一定存在于Adobe Campaign中。

1. 根据所有用户的移动应用程序配置文件来定位所有用户。

   利用此消息类型，可定向在Adobe Campaign中具有移动用户档案的移动应用程序的所有已知或匿名用户。 此消息类型可仅使用非个人属性和非敏感属性进行个性化，并且不需要 Mobile SDK 与 Adobe Campaign 的应用程序内消息传递服务之间进行安全握手。因此，个性化策略基于您从用户与设备的交互中学到的关于用户的信息。 例如，定位在上周启动了应用程序超过5次的所有用户。

1. [**基于 Campaign 用户档案的目标用户**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   利用此消息类型，可定向订阅了您移动应用程序的Adobe Campaign用户档案（CRM用户档案）。 该消息可以使用Adobe Campaign中所有可用的用户档案属性进行个性化，但需要在Mobile SDK与Campaign的应用程序内消息传递服务之间进行安全握手，以确保包含个人和敏感信息的消息仅供授权用户使用。

此模板对于支持跨渠道编排用例非常有用，在这些用例中，您已经将用户定向到其他渠道（如电子邮件或推送），并且根据用户的响应，您希望让他们与应用程序内消息互动。

## 报告应用程序内投放 {#report}

发布投放后，您可以[报告应用程序内投放](/help/communication-channels/mobile/in-app/in-app-reporting.md)。

## 其他资源

* [应用程序内报表](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [设置移动资产](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [使用Adobe Experience Platform SDK配置移动应用程序](https://helpx.adobe.com/cn/campaign/kb/configuring-app-sdk.html)
* [准备和发送应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [自定义应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [在工作流中发送应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [启用生命周期量度](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
