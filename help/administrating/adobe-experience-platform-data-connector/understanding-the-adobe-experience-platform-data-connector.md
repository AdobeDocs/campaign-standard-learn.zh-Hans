---
title: 了解Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector通过将XTK数据（在Campaign中引入的数据）映射到Adobe Experience Platform上的Experience Data Model (XDM)数据，帮助现有客户使其数据在Adobe Experience Platform上可用。
feature: People Core Service Integration
jira: KT-2826
thumbnail: 27304.jpg
role: User
level: Experienced
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 943599bd7ce139ef846f093ebda9084a91550aca
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 4%

---

# 了解Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>此功能处于测试阶段，可能会频繁更新和修改，恕不另行通知。
>
>请联系 [!UICONTROL Adobe Customer Support] 如果您计划实施此功能。

## 概述

Adobe Experience Platform [!UICONTROL Data Connector] Adobe Experience Platform通过将XTK数据(在Adobe Campaign中引入的数据)映射到 [!DNL Experience Data Model] (XDM)数据在Adobe Experience Platform上。

该连接器是单向的，用于将数据从Adobe Campaign Standard发送到Adobe Experience Platform。 数据永远不会从Adobe Experience Platform发送到Adobe Campaign Standard。

Adobe Experience Platform [!UICONTROL Data Connector] 面向了解Adobe Campaign Standard的数据工程师 [!UICONTROL custom resources] 并了解客户的整体数据架构应如何在Adobe Experience Platform中。

>[!VIDEO](https://video.tv.adobe.com/v/27304?learn=on){transcript=true}

*此视频概述Adobe Experience Platform [!UICONTROL Data Connector] （09:35分钟）*

>[!NOTE]
>
>的开箱即用传输 [!UICONTROL subscription events] 不受支持。 要转移 [!UICONTROL subscription events]中，您可以在Adobe Experience Platform中创建相应的XDM和数据集，然后为这些数据配置自定义数据映射。
>
>现有 [!UICONTROL experience events] 无法摄取到Adobe Experience Platform，但正在生成 [!UICONTROL experience events] 流到Adobe Experience Platform。

## 执行数据映射的关键步骤

以下教程介绍了在Campaign Standard和Adobe Experience Platform之间执行数据映射的关键步骤：

1. [映射自定义资源](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [映射 Experience 事件](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [映射种子表数据](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [修改数据映射](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [检查数据摄取作业的状态](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

