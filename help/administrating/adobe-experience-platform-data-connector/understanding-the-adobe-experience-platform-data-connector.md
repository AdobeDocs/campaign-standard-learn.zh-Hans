---
title: 了解Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector将XTK数据(以活动摄取的数据)映射到Adobe Experience Platform上的Experience Data Model(XDM)数据，帮助现有客户在Adobe Experience Platform上提供其数据。
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 4%

---


# 了解Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>此功能目前为测试版，如有频繁更新和修改，恕不另行通知。
>如果您计划实 [!UICONTROL Adobe Customer Support] 施此功能，请联系。

## 概述

Adobe Experience Platform将 [!UICONTROL Data Connector] XTK数据(以Adobe Campaign摄取的数据)映射到Adobe Experience Platform上的(XDM)数据， [!DNL Experience Data Model] 从而帮助现有客户在Adobe Experience Platform上提供数据。

请注意，该连接器是单向的，会将数据从Adobe Campaign标准发送到Adobe Experience Platform。 数据从不从Adobe Experience Platform发送到Adobe CampaignStandard。

Adobe Experience Platform面 [!UICONTROL Data Connector] 向了解Adobe Campaign标准并了 [!UICONTROL custom resources] 解客户的整体数据模式如何位于Adobe Experience Platform内的数据工程师。

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*此视频概述了Adobe Experience Platform([!UICONTROL Data Connector]09:35分钟)*

>[!NOTE]
>
>不支持现成的 [!UICONTROL subscription events] 传输。 要进行传 [!UICONTROL subscription events]输，您可以在Adobe Experience Platform上创建相应的XDM和数据集，然后为这些数据配置自定义数据映射。
>现有 [!UICONTROL experience events] 内容无法引入Adobe Experience Platform，但持续生成 [!UICONTROL experience events] 的内容将流式传输到Adobe Experience Platform。

## 执行数据映射的关键步骤

以下教程介绍在Campaign Standard和Adobe Experience Platform之间执行数据映射的关键步骤：

1. [映射自定义资源](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [映射体验事件](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [映射种子表数据](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [修改数据映射](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [检查数据摄取作业的状态](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## 其他资源

* [关于 Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [体验数据模型概述](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [映射定义](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [映射激活](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [通过 API 触发数据摄取](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
