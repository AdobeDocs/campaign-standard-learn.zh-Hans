---
title: 过渡流程——切换电子邮件平台
description: '在移动电子邮件服务提供商(ESP)时，不可能同时过渡您现有的已建立IP地址。 在重新开始时，务必遵循最佳实践，以建立良好的声誉。 由于您使用的新IP地址尚无信誉，因此ISP无法完全信任来自它们的邮件，因此需要谨慎处理它们允许向其客户提供的邮件。 '
feature: null
topics: Deliverability
kt: null
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f4dbccc1fea3db4dbddec0d4329b359993b62d20
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---


# 过渡流程——切换电子邮件平台

在移动电子邮件服务提供商(ESP)时，不可能同时过渡您现有的已建立IP地址。 在重新开始时，务必遵循最佳实践，以建立良好的声誉。 由于您使用的新IP地址尚无信誉，因此ISP无法完全信任来自它们的邮件，因此需要谨慎处理它们允许向其客户提供的邮件。

想想你遇到新人时会做什么。 通常，您需要建立信任而不是立即信任他们。 不要认为您的品牌会自动帮助您建立这种信任，因为垃圾邮件发送者会用您的名字做坏事。 ISP需要重新评估您的发送实践，因为行动在电子邮件发送能力中最能说明问题。

建立良好声誉是一个过程。 但一旦建立，小的负面指标对您和邮件投放的影响就会减小。

![过渡过程](assets/transition-process.png)

温暖您的IP地址和域的时间可能不同，但通常发送方在大多数第1级ISP(、//[!DNL Gmail]/等)建立声誉时，最多 [!DNL Microsoft]可 [!DNL Verizon]采用8周[!DNL Yahoo][!DNL AOL]的基准。
在接下来的几节中，我们将调查重点关注的关键领域，以正确安装。

## 基础架构

能否成功交付取决于坚实的基础。 电子邮件基础架构是核心元素。 构建得当的电子邮件基础架构包括多个组件，即域和IP地址。 这些组件就像您发送电子邮件背后的机器，它们通常是发送声誉的锚。 交付能力顾问可确保在实施过程中正确设置这些元素，但由于信誉元素，因此您必须具备这一基本理解。

### 域设置和策略

时代已经改变，一些ISP( [!DNL Gmail] 如 [!DNL Yahoo]及)现在在将域名声誉附加到发送方电子邮件声誉时，会将域名声誉作为附加条件。 您的域信誉基于您的发送域而不是您的IP地址。 这意味着在ISP筛选决策方面，您的品牌优先。

Adobe Campaign新发送方的入门过程包括设置发送域并确保正确建立基础结构。 您应与专家合作，了解您计划长期使用的领域。 下面是形成良好域策略的一些技巧：

* 在您选择的域中尽可能清晰地反映品牌，以便用户不会错误地将邮件识别为垃圾邮件。 例如 [!DNL newsletter.foo.com], [!DNL receipts.foo.com]等等。
* 您不应使用您的父级或公司域，因为它可能会影响组织向ISP发送邮件的投放。
* 考虑使用父域的子域来使发送域合法化。
* 为交易和营销消息类别分离子域。 这将帮助您的电子邮件流量以更可靠的方式流动，因为ISP会寻找这种发送方法，这种方法是已知的电子邮件最佳实践，强烈推荐使用。

### IP战略

形成结构良好的IP战略有助于建立良好的声誉，这一点非常重要。 IP的数量和设置因您的业务模式和营销目标而异。 与专家合作，制定明确的战略以正确开始。 请注意以下重要事项：

* 太多的IP可能会引发声誉问题，因为它是垃圾邮件发送者对雪地车的常见策略，而垃圾邮件发送者使用这种策略，即流量在许多IP之间传播，以最大化垃圾邮件的投放。 即使您不是垃圾邮件发送者，如果您使用的IP过多，尤其是那些IP之前没有任何流量，您也可能看起来像垃圾邮件发送者。
* IP太少可能会导致吞吐量问题，并可能引发信誉问题。 吞吐量因ISP而异。 ISP愿意接受多少和多快，通常取决于其基础架构和发送信誉阈值。
* 为消息传递类型划分流量是关键。 在单独的IP池上至少单独使用营销和交易邮件，这一点很重要。
* 根据您的邮件策略，如果您的信誉大不相同，则最好在不同的IP池上分别使用不同的产品或营销流。 部分营销人员还按地区进行细分。 将IP与声誉较低的流量分开不会解决信誉问题，但会防止您的“良好”声誉电子邮件投放出现问题。 毕竟，你不想牺牲好受众，换回风险更高的客户。

### 反馈循环

Adobe Campaign在后台处理有关退回、投诉、取消订阅等的数据。 这些反馈环的设置是可交付性的一个重要方面。 投诉会损害声誉，因此您应删除从目标受众中注册投诉的电子邮件地址。 请务必注意，不 [!DNL Gmail] 能提供此数据。 列表取消订阅标头和参与过滤对于订阅者尤 [!DNL Gmail] 为重要，订阅者现在占大多数订阅者数据库。

### 身份验证

身份验证是ISP用来验证发送方身份的过程。 最常见的两种身份验证协 [!DNL Sender Policy Framework (SPF)] 议是 [!DNL DomainKeys Identified Mail] 和(DKIM)。 最终用户看不到这些内容，但确实可以帮助ISP过滤来自经过验证的发件人的电子邮件。 [!DNL Domain-based Message Authentication Reporting and Conformance] (DMARC)越来越受欢迎，但其政策尚未被所有ISP纳入其声誉系统。

#### **SPF**

[!DNL Sender Policy Framework (SPF)] 是一种身份验证方法，允许域的所有者指定用于从该域发送邮件的邮件服务器。

#### **DKIM**

[!DNL Domain Keys Identified Mail (DKIM)] 是用于检测伪造发件人地址（通常称为）的身份验证 [!DNL spoofing]方法。 如果启用了DKIM，则允许接收者确认发送者是否获得从该域发送邮件的授权。

#### **DMARC**

[!DNL Domain-based Message Authentication, Reporting and Conformance (DMARC)] 是一种身份验证方法，使域所有者能够保护其域免遭未经授权的使用。 DMARC使用SPF或DKIM，或者同时使用DKIM或两者允许域所有者控制未通过身份验证的邮件发生的情况：已交付、已隔离或已拒绝。

## 定位条件

发送新流量时，只目标IP加热初期参与度最高的用户。 这有助于在您投入较少参与的受众之前，建立起积极的声誉，以有效建立信任。 下面是参与的基本公式：

![管理公式](assets/formula-for-enagement.png)

通常，参与率基于特定时间段。 此度量可能会因公式是否适用于整体级别或特定邮寄类型或活动而显着不同。 需要与Adobe Campaign交付性顾问一起提供特定定位标准，因为每个发送方和ISP都不同，通常需要自定义计划。

## IP加温期间的ISP特定考虑事项

ISP有不同的规则和不同的流量观察方式。 例如，ISP [!DNL Gmail] 是最成熟的ISP之一，因为除了所有其他声誉衡量指标，它们还非常严格地考虑参与（打开和点击）。 这需要一个自定义计划，该计划仅目标参与度最高的用户。 其他ISP也可能要求相同。 与您的Adobe Campaign交付性顾问合作制定特定计划。

## 卷

您发送的邮件数量对于建立良好的信誉至关重要。 把你自己放在ISP的角度上——如果开始看到陌生人发来的大量流量，那会令人担忧。 立即发送大量邮件是有风险的，并且会导致通常难以解决的信誉问题。 从糟糕的名声中挖出自己、膨胀和阻止因过早发送过多而导致的问题，可能会令人沮丧、耗时、代价高昂。

音量阈值因ISP而异，也可能因您的平均参与度指标而异。 有些发送方需要非常低且缓慢的音量斜坡，而另一些发送方可能会允许音量陡降。 我们建议与专家(如Adobe Campaign交付性顾问)合作，制定自定义的批量计划。

以下是一列表有关如何顺畅过渡的提示和提示：

* **权限** 是任何成功的电子邮件项目的基础。
* **低开始和慢** ，发送量低，随后在建立发件人信誉时增加。
* 汇 **编邮寄策略** 可让您在使用当前ESP时增加活动量，而不会中断电子邮件日历。
* **参与度很重要** -与定期打开并单击您电子邮件的订阅者进行开始。
* **遵循计划** -我们的建议已帮助数百个活动客户成功提升其电子邮件项目。
* **监控回复电子邮件帐户**。 客户使用或不响应是一 [!DNL nore-ply@xyz.com] 种糟糕的体验。
* 非活动地址可能会对交付能力产生负面影响。 **在当前平台** （而非新IP）上重新激活和重新许可。
* **域** -使用作为公司实际域的子域的发送域。 例如，如果公司域为， [!DNL xyz.com]则 [!DNL email.xyz.com] ISP的可信度高于 [!DNL xyzemail.com]
* **透明度** -电子邮件域的注册详细信息应公开提供，并且不应为私人信息。

在许多情况下，交易邮件不遵循传统的促销升温方法。 由于邮件的性质，控制邮件的音量显然很困难，因为它通常需要用户交互来触发电子邮件。 在某些情况下，事务性邮件可以在没有正式计划的情况下进行转换。 在其他情况下，随着时间的推移，最好过渡每个消息类型，以缓慢增大音量。 例如，您可能希望按如下方式进行过渡:

1. 购买确认——一般情况下参与度较高
2. 购物车放弃——一般中高参与度
3. 欢迎电子邮件——参与度高，但可能包含不良地址，具体取决于列表收集方法
4. 回收电子邮件——通常降低参与度

## 其他资源

* [启动新平台](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/managing-deliverability/starting-new-platform.html)