---
title: 了解 Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector通过将XTK数据（在Campaign中摄取的数据）映射到Adobe Experience Platform上的Experience Data Model(XDM)数据，帮助现有客户在Adobe Experience Platform上提供其数据。
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 了解Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>此功能目前处于测试阶段，可能会频繁更新和修改，恕不另行通知。
>
>如果您计划实施此功能，请联系[!UICONTROL Adobe Customer Support]。

## 概述

Adobe Experience Platform [!UICONTROL Data Connector]通过将XTK数据(在Adobe Campaign中摄取的数据)映射到Adobe Experience Platform上的[!DNL Experience Data Model](XDM)数据，可帮助现有客户在Adobe Experience Platform上使其数据可用。

请注意，连接器是单向的，会将数据从Adobe Campaign Standard发送到Adobe Experience Platform。 数据从不会从Adobe Experience Platform发送到Adobe Campaign Standard。

Adobe Experience Platform [!UICONTROL Data Connector]面向了解Adobe Campaign Standard [!UICONTROL custom resources]并了解客户整体数据架构如何在Adobe Experience Platform内部的数据工程师。

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*此视频概述Adobe Experience Platform( [!UICONTROL Data Connector] 09:35分钟)*

>[!NOTE]
>
>不支持[!UICONTROL subscription events]的现成传输。 要传输[!UICONTROL subscription events]，您可以在Adobe Experience Platform上创建相应的XDM和数据集，然后为这些数据配置自定义数据映射。
>
>现有的[!UICONTROL experience events]无法摄取到Adobe Experience Platform中，但持续生成的[!UICONTROL experience events]将流式传输到Adobe Experience Platform。

## 执行数据映射的关键步骤

以下教程介绍了在Campaign Standard和Adobe Experience Platform之间执行数据映射的关键步骤：

1. [映射自定义资源](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [映射 Experience 事件](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [映射种子表数据](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [修改数据映射](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [检查数据摄取作业的状态](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## 其他资源

* [关于 Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [体验数据模型概述](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [映射定义](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [映射激活](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [通过 API 触发数据摄取](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
