---
title: 外部信号活动-使用参数调用工作流
description: 外部信号活动用于组织和编排不同的流程，这些流程是同一客户旅程中进入不同工作流的一部分。 利用该活动，可从另一个工作流启动一个工作流，从而支持更复杂的客户历程，同时能够更好地进行监控，从而出现问题时作出反应。
feature: External Signal Activity
topics: Workflows
kt: 2750
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 9b1d8c5fb895d84da14a0402ec1f130b90a991b0
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 16%

---


# [!UICONTROL External Signal activity ]-使用参数调用工作流

The [!UICONTROL External Signal activity] is used to organize and orchestrate different processes that are part of the same customer journey into different workflows. 利用该活动，可从另一个工作流启动一个工作流，从而支持更复杂的客户历程，同时能够更好地进行监控，从而出现问题时作出反应。

在ACS 19.2中， [!UICONTROL External Signal activity] 不仅可以调用工作流，还可以将参数传递给工作流(受众到目标的名称、要导入的文件名、消息内容的一部分等) 从另一个工作流或REST API调用连接到工作流，以与外部系统集成。

此外，还包含一个新 **的测试活动** ，您可以在该中对此功能运行测试。

以下视频介绍了完成以下操作所需的配置步骤：

1. **从外部系统** (如内容管理系统(CRM))接收外部参数：
   * 在外部信号活动中声明参数
   * 配置API调用以定义参数并触发工作流外部信号活动。 有关如何配置API调用的详细信息，请参 [阅触发信号活动](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)。

1. **使用外部参数(事件变量** )自定义工作流：
触发工作流后，参数将被引入工作流的事件变量中，并可在工作流中使用。 请参阅 [可以](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) 使用活动变量自定义的所有事件的文档：

   * 配置测试活动（19.2中新增）
   * 配置读取受众和电子邮件投放活动

1. **配置结束活动** ，以使用外部参数调用工作流

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## 其他资源

* [外部信号（文档）](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
