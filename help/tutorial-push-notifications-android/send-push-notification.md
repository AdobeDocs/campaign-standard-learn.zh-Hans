---
title: 第6部分 — 发送推送通知以测试您的工作
description: 第6部分 — 发送推送通知以测试您的工作
feature: Push
jira: KT-4830
user: Admin
level: Experienced
doc-type: tutorial
activity: use
team: TM
exl-id: 10218e1f-6e85-490a-84d9-c5d42bd2321d
TQID: 'https://experienceleague.adobe.com/NrQc40vzqTy0fNfVT6fN0IjMKuXjilt6eZV-lgZpAcQ'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a4671286-a59f-47e3-b97b-90627a1977d5
    internal-label: Communication channels
subfeature_v2:
  - id: a4657621-810c-498b-8a27-7ced9c176dda
    internal-label: Push notifications
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 508c3590ce956401ccfba3a256000cbc5849a684
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%
---
# 第6部分 — 发送[!UICONTROL Push Notification]以测试您的工作

我们现在需要使用Adobe Campaign创建并发送[!UICONTROL Push Notification]。 要创建简单推送通知以进行测试，请执行以下步骤。

* 登录到您的Adobe Campaign Standard实例
* 单击&#x200B;**[!UICONTROL Marketing Activities]->[!UICONTROL Create]->[!UICONTROL Push Notification]**
* 选择&#x200B;**[!UICONTROL Send push to app subscribers(mobileApp)]**&#x200B;并单击“下一步”
* 从&#x200B;**[!UICONTROL Associate a Mobile App to a delivery]**&#x200B;下拉列表中选择适当的移动设备应用程序，然后单击&#x200B;**[!UICONTROL Next]**
* 单击计数标签，它应返回大于0的值。 单击&#x200B;**[!UICONTROL Next]**
* 提供有意义的[!UICONTROL Message title]和[!UICONTROL Message body]，然后单击&#x200B;**[!UICONTROL Create]**。
* 单击 **[!UICONTROL Prepare]**。 准备完成后，单击&#x200B;**[!UICONTROL Confirm]**&#x200B;发送消息。

如果一切顺利，您应该会在模拟器中运行的™应用程序中看到通知

## 其他资源

* [有关推送通知的详细文档](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/push-notifications/about-push-notifications.html?lang=en)
* [创建推送通知（视频）](/help/communication-channels/mobile/push-notifications/creating-a-push-notification.md)
