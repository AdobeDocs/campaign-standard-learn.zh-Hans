---
title: 配置事件
description: “了解事件如何定义由用户启动的操作将触发要显示的应用程序内消息。 ”
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 89df23d00913d36b93d3be03b62c74320524f9c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# 配置[!UICONTROL Events] {#configuring-events}

配置 [!UICONTROL In-App] 消息中，您需要定义用户启动的操作触发要显示的消息。 这些操作称为 [!UICONTROL events]. 三类 [!UICONTROL events] 可用： [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]和 [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] are [!UICONTROL custom events] 在移动应用程序中实施的ID、ID和ID。

示例包括：

* 客户已查看项目
* 客户将项目添加到购物车
* 放弃购买
* 客户已购买了某些商品

您必须配置这些 [!UICONTROL events] 在Adobe Campaign。 以下视频介绍了如何执行此操作。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] 现成 [!UICONTROL events]. 以下 [!UICONTROL events] 可用：

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

示例用例可以是在升级后引入新功能的消息，或事件促销。

>[!NOTE]
>
>的 [!UICONTROL Lifecycle module] 需要在移动应用程序中配置。 有关 [如何向应用程序添加生命周期](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

根据移动设备应用程序中的感知方式，支持以下三个类别：

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] 需要Adobe Analytics许可证。 在您 [[!DNL Analytics] 已配置扩展](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) 添加 [将Analytics添加到您的应用程序](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)，则这些事件将在 [!UICONTROL In-App] 配置。
