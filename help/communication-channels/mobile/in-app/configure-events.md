---
title: 配置事件
description: “了解事件如何定义哪些用户启动的操作会触发要显示的应用程序内消息。 ”
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 56b973566e9dee412aeee1412fe6271537fc1295
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# 配置[!UICONTROL Events] {#configuring-events}

配置时 [!UICONTROL In-App] 消息时，您必须定义用户启动的操作触发消息显示。 这些操作称为 [!UICONTROL events]. 三类 [!UICONTROL events] 可用： [!UICONTROL Mobile Application events]， [!UICONTROL Life-Cycle events]、和 [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] 是 [!UICONTROL custom events] 移动应用程序中实现的服务。

示例包括：

* 客户已查看项目
* 客户将商品添加到购物车
* 放弃购买
* 客户购买了一些东西

您必须配置这些 [!UICONTROL events] 在Adobe Campaign中。 以下视频介绍了如何执行此操作。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Life-Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] 开箱即用 [!UICONTROL events]. 以下各项 [!UICONTROL events] 可用：

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

示例用例可能是在升级后引入新功能的消息，或事件促销活动。

>[!NOTE]
>
>此 [!UICONTROL Lifecycle module] 必须在移动应用程序中配置。 请参阅此处，了解更多有关 [如何向应用程序添加生命周期](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

根据移动应用程序中的感知方式，支持以下三个类别：

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] 需要Adobe Analytics许可证。 一旦您拥有 [!DNL Analytics] 扩展已配置并已将Analytics添加到您的应用程序中，以下事件将变得可用： [!UICONTROL In-App] 配置。
