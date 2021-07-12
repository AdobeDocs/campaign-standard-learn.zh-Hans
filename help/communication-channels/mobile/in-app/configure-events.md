---
title: 配置事件
description: “了解事件如何定义由用户启动的操作将触发要显示的应用程序内消息。 ”
feature: 应用程序内
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---

# 配置[!UICONTROL Events] {#configuring-events}

配置[!UICONTROL In-App]消息时，您需要定义用户启动的操作触发要显示的消息。 这些操作称为[!UICONTROL events]。 提供了三类[!UICONTROL events]:[!UICONTROL Mobile Application events]、[!UICONTROL Life Cycle events]和[!UICONTROL Analytics events]。

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] 是在 [!UICONTROL custom events] 移动应用程序中实施的。

示例包括：

* 客户已查看项目
* 客户将项目添加到购物车
* 放弃购买
* 客户已购买了某些商品

必须在Adobe Campaign中配置这些[!UICONTROL events]。 以下视频介绍了如何执行此操作。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] 开箱即用 [!UICONTROL events]。以下[!UICONTROL events]可用：

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

示例用例可以是在升级后引入新功能的消息，或事件促销。

>[!NOTE]
>
>[!UICONTROL Lifecycle module]需要在移动应用程序中配置。 请参阅此处，以了解有关[如何将生命周期添加到应用程序的更多信息](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

根据移动设备应用程序中的感知方式，支持以下三个类别：

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] 需要Adobe Analytics许可证。配置了[[!DNL Analytics] 扩展](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch)并将[Analytics添加到应用程序](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)后，这些事件便可在ACS的[!UICONTROL In-App]配置中使用。

## 其他资源

* [启用生命周期量度（文档）](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
