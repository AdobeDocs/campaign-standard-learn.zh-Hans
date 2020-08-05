---
title: 应用程序内消息简介
description: Adobe Campaign Standard(ACS)应用程序内消息传递渠道允许您向用户呈现上下文相关的应用程序内消息，以响应客户在移动应用程序中的实时行为。
feature: In-App
topics: Mobile
kt: 1911
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 9%

---


# 消息简 [!UICONTROL In-App] 介 {#introduction}

渠道 [!UICONTROL In-App Messaging] 允许您在用户在移动应用程序中处于活动状态时显示消息。 This channel requires mobile applications to be integrated with [!UICONTROL Adobe Experience Platform SDK].

本教程将说明设置移动属性、渠道的扩 [!UICONTROL Launch] 展以及 [!UICONTROL In-App Messaging] 如何在Adobe Campaign Standard准备、自定义和发送 [!UICONTROL In-App] 消息所需的步骤。 这些链接将引导您观看每个高亮显示主题的视频教程。

## 先决条件{#prerequisites}

1. 确保可以访问 **[!UICONTROL In-App]** 渠道。 如果您无法访问这些渠道，请与帐户管理团队联系。
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and [!UICONTROL Launch].

   1. 在Adobe Campaign Standard，确保IMS用户是组和组的一 [!UICONTROL Standard User] 部分 [!UICONTROL Administrator] 。\
      此步骤允许用户登录Adobe Campaign Standard，导航到Experience PlatformSDK移动应用程序页面，并视图您在中创建的移动应用程序属性 [!UICONTROL Launch]。
   1. 在 [!UICONTROL Launch]中，确保您的IMS用户是产品用户档案的 [!UICONTROL Launch] 一部分。\
      此步骤允许用户登录以创 [!UICONTROL Launch] 建和视图属性。 有关中的产品用户档案的详 [!UICONTROL Launch]细信息， [请参阅创建产品用户档案](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)。 在产品用户档案中，公司或属性上不应设置任何权限，但用户仍应能够登录。

1. 在Adobe Experience Platform Launch:

   1. 通过创建移动属性并使用Experience PlatformSDK对移动应用程序进行仪表，创建移动应用程序。
   1. 为您的移 **动应用** 程序安装Adobe Campaign Standard扩展。

有关扩展的详细信息，请参阅文 [档中的“在Adobe启动中配](Https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) 置Campaign Standard扩展 [!UICONTROL Adobe Launch ]”一节。

## 设置消息的步 [!UICONTROL In-App] 骤 {#steps-to-set-up}

1. [使用Adobe Experience PlatformSDK配置移动应用程序](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md)。

1. [配置事件](/help/communication-channels/mobile/in-app/configure-events.md)。

## 创建、管理和发布 [!UICONTROL In-App] 投放 {#create-manage-publish}

您可以通过单击主页中的卡或从中创建一次 **[!UICONTROL Create an In-App Message]** 应用程序内投放，也 [!UICONTROL Marketing Activities]可以在工 [作流中创建一个应用程序内投放](/help/communication-channels/mobile/in-app/in-app-activity.md)。

设置投放时，您有三个选项，可通过从不同的投放模板中进行选择来目标用户：

1. [**广播应用程序内消息&#x200B;**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)，以目标移动应用程序的所有用户。

   此消息类型允许您向移动应用程序的所有用户（当前或将来）发送消息，即使他们没有Adobe Campaign用户档案。 因此，在自定义消息时不可能进行个性化，因为用户档案中不一定存在用户Adobe Campaign。

1. 目标所有用户，具体取决于其移动App用户档案。

   此消息类型允许您目标具有移动用户档案的移动应用程序的所有已知或匿名用户。 此消息类型可仅使用非个人属性和非敏感属性进行个性化，并且不需要 Mobile SDK 与 Adobe Campaign 的应用程序内消息传递服务之间进行安全握手。因此，个性化策略基于您从用户与设备的交互中了解到的信息。 例如，目标上周启动其App超过5次的所有用户。

1. [**目标用户的活动用户档案&#x200B;**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md)。

   此消息类型允许您目标订阅了您的移动应用程序的Adobe Campaign用户档案(CRM用户档案)。 该消息可在Adobe Campaign中以所有可用的用户档案属性进行个性化，但需要Mobile SDK与活动的应用程序内消息传递服务之间进行安全握手，以确保包含个人和敏感信息的消息仅由授权用户使用。

此模板有助于支持跨渠道业务流程使用案例，您已经将目标锁定在其他渠道（如电子邮件或推送）上的用户，并且根据他们的响应，您希望通过应用程序内消息与他们互动。

## 报告应用程序内投放 {#report}

投放发布后，您可以报告 [应用程序内投放](/help/communication-channels/mobile/in-app/in-app-reporting.md)。

## 其他资源

* [应用程序内报告](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [设置移动属性](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [使用Adobe Experience PlatformSDK配置移动应用程序](https://helpx.adobe.com/cn/campaign/kb/configuring-app-sdk.html)
* [准备和发送应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [自定义应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [在工作流中发送应用程序内消息](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [启用生命周期指标](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
