---
title: 应用程序内消息简介
description: 了解如何向用户展示与上下文相关的应用程序内消息，以响应客户在移动应用程序中的实时行为。
feature: In App
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 10%

---

# 简介 [!UICONTROL In-App] 消息 {#introduction}

此 [!UICONTROL In-App Messaging] 渠道允许您在用户激活移动应用程序时显示消息。 此渠道要求将移动应用程序与 [!UICONTROL Adobe Experience Platform SDK].

本教程将介绍设置移动资产、 [!UICONTROL Launch] 的扩展 [!UICONTROL In-App Messaging] 渠道以及如何准备、自定义和发送 [!UICONTROL In-App] Adobe Campaign Standard中的消息。 这些链接指向有关每个突出显示主题的视频教程。

## 先决条件 {#prerequisites}

1. 确保您可以访问 **[!UICONTROL In-App]** 渠道。 如果您无法访问这些渠道，请与帐户管理团队联系。
1. 验证您的 **用户** 具有必要的 **权限** 在Adobe Campaign Standard和 [!UICONTROL Launch].

   1. 在Adobe Campaign Standard中，确保IMS用户属于 [!UICONTROL Standard User] 和 [!UICONTROL Administrator] 组。

      此步骤允许用户登录Adobe Campaign Standard，导航到Experience PlatformSDK移动应用程序页面，并查看您在中创建的移动应用程序属性 [!UICONTROL Launch].

   1. In [!UICONTROL Launch]，确保您的IMS用户属于 [!UICONTROL Launch] 产品配置文件。 此步骤允许用户登录到 [!UICONTROL Launch] 创建和查看属性。 在产品配置文件中，不应在公司或资产上设置权限，但用户应能够登录。

1. 在Adobe Experience Platform Launch中：

   1. 通过创建移动资产创建移动应用程序，并使用Experience PlatformSDK检测移动应用程序。
   1. 安装 **Adobe Campaign Standard** 移动应用程序的扩展。

有关扩展的更多信息，请参阅 [在Adobe启动项中配置Campaign Standard扩展](Https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) 在文档中。

## 要设置的步骤 [!UICONTROL In-App] 消息 {#steps-to-set-up}

1. [使用 Adobe Experience Platform SDK 配置移动应用程序](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [配置事件](/help/communication-channels/mobile/in-app/configure-events.md).

## 创建、管理和发布 [!UICONTROL In-App] 投放 {#create-manage-publish}

您可以通过单击 **[!UICONTROL Create an In-App Message]** 主页上的信息卡，从 [!UICONTROL Marketing Activities]，或者，您可以 [在工作流中创建应用程序内投放](/help/communication-channels/mobile/in-app/in-app-activity.md).

在设置投放时，可通过从不同的投放模板中进行选择来定位用户，方法有三种：

1. [**广播应用程序内消息**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) 定位移动应用程序的所有用户。

   利用此消息类型，可向移动应用程序的所有用户（当前或将来）发送消息，即使他们当前在Adobe Campaign中没有用户档案。 因此，在自定义消息时不可能进行个性化，因为Adobe Campaign中不一定存在用户配置文件。

1. 根据用户的移动应用程序配置文件定位所有用户。

   利用此消息类型，可定向在Adobe Campaign中具有移动用户档案的移动应用程序所有已知或匿名用户。 此消息类型可仅使用非个人属性和非敏感属性进行个性化，并且不需要 Mobile SDK 与 Adobe Campaign 的应用程序内消息传递服务之间进行安全握手。因此，个性化策略基于您从用户与设备的交互中了解到的用户情况。 例如，定向上周启动应用程序超过5次的所有用户。

1. [**基于 Campaign 用户档案的目标用户**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   利用此消息类型，可定向订阅了您的移动应用程序的Adobe Campaign用户档案（CRM用户档案）。 在Adobe Campaign中，可以使用所有可用的配置文件属性个性化消息。 它需要在Mobile SDK与Campaign的应用程序内消息传递服务之间进行安全握手，以确保包含个人和敏感信息的消息仅由授权用户使用。

此模板对于支持跨渠道编排用例非常有用，在这些用例中，您已定位了其他渠道上的用户，如电子邮件或推送。 然后，根据他们的响应，您希望向他们发送应用程序内消息。

## 报告应用程序内投放情况 {#report}

发布投放后，您可以 [报告应用程序内投放](/help/communication-channels/mobile/in-app/in-app-reporting.md).
