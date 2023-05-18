---
title: 面向营销人员的疑难解答
description: 了解最常见的错误有助于更快地解决问题并提高工作效率。 这些疑难解答提示可帮助您有效解决发生的类似错误。
version: Standard
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: bc9e83e1864b02208f9cd7fe591c77bf6d049a37
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 1%

---


# 面向营销人员的疑难解答：5个常见工作流和投放错误

收件人： [苏拉伊·帕特拉](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}，美杰高级顾问

作为过去5年Adobe Experience Cloud产品的高级工程师和客户专家，我在 [梅耶尔](https://www.meijer.com/){target="_blank"}美国超级中心链成立于1934年，旨在与ACS开展复杂的营销和交易活动。 我处理的一些项目包括用于存储个性化选件和订单详细信息的自定义促销活动、与Adobe Audience Manager集成的项目，以及用于区段摄取的客户分析项目。


在使用ACS时，我遇到了一些错误，这些错误很费时，而且难以解决。 了解最常见的错误有助于更快地解决问题并提高工作效率。 以下是我的故障诊断提示，可帮助您有效解决发生的类似错误。

## 数据类型不匹配错误

**错误代码:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**原因：**
当您尝试使用不同数据类型的字段进行协调时，工作流中会显示这些类型的错误。 例如，当您使用具有字符串字段的加载文件上传文件时，并尝试将字符串字段与数据类型为int的配置文件字段进行协调。

![数据类型不匹配错误](/help/assets/kt-13256/data-type-mismatch.png)

**解决方案：**
将“加载文件”活动中字段的数据类型更改为与您匹配的数据类型。 打开“加载文件”活动。 移到“COLUMN DEFINITION”选项卡，并更改所需字段的数据类型。


![数据类型不匹配解决方案](/help/assets/kt-13256/data-type-mismatch-solution.png)

## 投放个性化错误

**错误代码:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**原因：**
当您向某个地址发送电子邮件时，会显示此错误，但该电子邮件或任何其他标识符与用户档案未协调。 要发送电子邮件通信，电子邮件或标识符应始终链接到用户档案。

使用协调活动，如下所示：

![与协调活动工作流](/help/assets/kt-13256/del-persn-error-wf.png)

**解决方案：**
带有收件人表的已加载文件中必须存在通用ID。 此通用键值将加载文件联接到协调活动中的收件人表。 电子邮件不能发送到收件人表中不存在的记录，这需要在工作流中执行此协调步骤。 在执行此操作时，您需要将传入的加载文件活动与用户档案中的电子邮件ID等标识符进行协调。 的 `nms:recipient` 架构是指用户档案表，在准备电子邮件时将传入记录与用户档案进行协调以使其可用。

请参阅协调活动的屏幕截图，如下所示。

![协调详细信息工作流](/help/assets/kt-13256/del-persn-error-wf-solution.png)

详细了解 [合并](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## 常见字段数据集错误

**错误代码:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**原因：**
使用 **排除活动** 在ACS工作流中。 当基于ID执行和排除时，如果主集和排除的集没有相同的字段名称，则会出现错误。


![常见字段数据集错误](/help/assets/kt-13256/dataset-error.png)

**解决方案:**

有两种方法可解决此错误：

1. 在主字段和排除的字段中使用相同的字段名称，然后将该字段用作ID

   或者

1. 使用JOINS排除方法选择要根据其排除记录的字段。

![常见字段数据集错误 — 解决方案 ](/help/assets/kt-13256/dataset-error-solution.png)

## 字段名称丢失错误

**错误代码:**
`XTK-170036 Unable to parse expression 'i__name'`

**原因:**

在 **扩充活动**. 最常见的一种显示如下。

![字段名称丢失错误](/help/assets/kt-13256/field-name-dropped-error.png)

手动编辑活动中的表达式名称时，会发生这种情况。 图像显示了从 `name `to `i__name`.

**解决方案:**

您可以通过以下三种方式解决此错误：

1. 将名称更改回最初存在的表达式。

2. 如果要使用新名称，请更改 **扩充活动**.

3. 如果您不记得更改了哪些内容，最好重新创建活动。

## 临时表删除错误 

**错误代码:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**原因：**
在涉及扩充或其他活动的复杂工作流中，这是常见的错误。 这可能意味着在对工作流进行多次更改期间，某些活动工作流未正确保存。

![临时表删除错误 ](/help/assets/kt-13256/temp-table-dropped-error.png)

**解决方案：**
出现此错误的方法有很多，因此没有简单的修复。 如果这是一个简单的工作流，则最好重新配置活动。 在复杂的工作流中，最好将工作流活动复制到新工作流中，然后保存并重新运行该工作流。