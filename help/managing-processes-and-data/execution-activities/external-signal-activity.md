---
title: 外部信号活动 — 使用参数调用工作流
description: 了解如何将一个工作流程与另一个工作流程开始，以支持更复杂的客户旅程，同时更好地监控和响应问题。
feature: 执行活动
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: Business Practitioner, Developer
level: Experienced
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ] — 使用参数调用工作流

[!UICONTROL External Signal activity]用于组织和安排属于同一客户旅程到不同工作流的不同流程。 利用该活动，可从另一个工作流启动一个工作流，从而支持更复杂的客户历程，同时能够更好地进行监控，从而出现问题时作出反应。

在ACS 19.2中，[!UICONTROL External Signal activity]不仅可以调用工作流，还可以将参数传递到工作流(要导入的受众名、要导入的文件名、部分消息内容等) 从另一个工作流或REST API调用到工作流，以与外部系统集成。

这还包括新的&#x200B;**Test**&#x200B;活动，您可以在其中对此功能运行测试。

以下视频介绍了完成以下操作所需的配置步骤：

1. **从外部** 系统(如内容管理系统(CRM))接收外部参数：

   * 在“外部信号”活动中声明参数
   * 配置API调用以定义参数并触发工作流外部信号活动。 有关如何配置API调用的详细信息，请参阅[触发信号活动](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)。

1. **使用外部参数(事件变量** )自定义工作流：

   触发工作流后，这些参数将被引入工作流的事件变量中，并可在工作流中使用。 有关可使用活动变量自定义的所有事件，请参阅[documentation](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html):

   * 配置测试活动（19.2中的新增功能）
   * 配置读取受众和电子邮件投放活动

1. **配置结束活** 动以使用外部参数调用工作流

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## 其他资源

* [外部信号（文档）](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
