---
title: 配置事件
description: '在Adobe Campaign Standard(ACS)事件中配置应用程序内消息时，定义由哪个用户启动的操作将触发要显示的消息。 '
feature: In-App
topics: Mobile
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 2%

---


# 配置[!UICONTROL Events] {#configuring-events}

配置[!UICONTROL In-App]消息时，您需要定义由用户启动的操作触发要显示的消息。 这些操作称为[!UICONTROL events]。 有三类别[!UICONTROL events]可用：[!UICONTROL Mobile Application events]、[!UICONTROL Life Cycle events]和[!UICONTROL Analytics events]。

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] 是在 [!UICONTROL custom events] 您的移动应用程序中实现的。

例如：

* 客户已查看项目
* 客户将项目添加到购物车
* 购物车放弃
* 客户已购买某些产品

必须以Adobe Campaign配置这些[!UICONTROL events]。 以下视频介绍如何执行此操作。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] 现成的 [!UICONTROL events]。以下[!UICONTROL events]可用：

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

示例用例可以是介绍升级后新功能的消息，也可以是事件促销。

>[!NOTE]
>
>[!UICONTROL Lifecycle module]需要在移动应用程序中配置。 请参见此处，了解有关如何将生命周期添加到应用程序的更多信息[](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

根据移动应用程序中所指导的内容，支持以下三种类别:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] 需要获得Adobe Analytics执照。将[[!DNL Analytics] 扩展配置为](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch)并将[分析添加到App](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)后，这些事件在ACS的[!UICONTROL In-App]配置中变为可用。

## 其他资源

* [启用生命周期指标（文档）](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
