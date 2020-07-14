---
title: 配置事件
description: '在Adobe Campaign Standard(ACS)事件中配置应用程序内消息时，定义由哪个用户启动的操作将触发要显示的消息。 '
feature: In-App
topics: Mobile
kt: 2548
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Configure [!UICONTROL Events] {#configuring-events}

配置消息 [!UICONTROL In-App] 时，您需要定义由用户启动的操作触发要显示的消息。 调用这些操作 [!UICONTROL events]。 有三类别 [!UICONTROL events] 可用： [!UICONTROL Mobile Application events]、 [!UICONTROL Life Cycle events]和 [!UICONTROL Analytics events]。

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] 在移 [!UICONTROL custom events] 动应用程序中实现。

例如：

* 客户已查看项目
* 客户将项目添加到购物车
* 购物车放弃
* 客户已购买某些产品

您必须在Adobe Campaign中 [!UICONTROL events] 配置这些组件。 以下视频介绍如何执行此操作。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] 现成的 [!UICONTROL events]。 The following [!UICONTROL events] are available:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

示例用例可以是介绍升级后新功能的消息，也可以是事件促销。

>[!NOTE]
>
>需要 [!UICONTROL Lifecycle module] 在移动应用程序中进行配置。 请参见此处，了解有关如何将生 [命周期添加到应用程序的更多信息](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

根据移动应用程序中所指导的内容，支持以下三种类别:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] 需要AdobeAnalytics许可。 配置扩展 [[!DNL Analytics] 并将Analytics](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) 添加到应 [用程序后](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)，这些事件在ACS的配置 [!UICONTROL In-App] 中变为可用。

## 其他资源

* [启用生命周期指标（文档）](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
