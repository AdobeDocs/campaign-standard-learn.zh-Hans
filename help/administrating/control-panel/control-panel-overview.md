---
title: 控制面板
description: 控制面板允许您按实例和允许列表 IP 地址监视和管理 SFTP 存储。
feature: Control Panel
topics: Control Panel
kt: 4696
doc-type: feature video
activity: use
team: PM
translation-type: tm+mt
source-git-commit: a078367ce8ffece206d3b83bfeefc4df4f8078d6
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 100%

---


# [!UICONTROL Control Panel] {#control-panel}

>[!NOTE]
>
>术语“[!UICONTROL whitelist]”和“[!UICONTROL blacklist]”已在 Adobe Campaign 文档中替换为“[!UICONTROL allow list]”和“[!UICONTROL block list]”。产品 UI、选项名称、内部代码以及教程视频中可能仍然存在这些术语的某些实例。在即将发布的控制面板版中将替换它们。

使用 [!UICONTROL Control Panel]，Adobe Campaign 管理员可以监测关键资产并执行管理任务，如按实例管理 SFTP 存储或将 IP 地址添加到[!UICONTROL allow list] 。

## 访问 [!UICONTROL Control Panel]

要访问控制面板，请转至 Experience Cloud 主页： [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com):

* **[!UICONTROL Experience Cloud Home]** > **[!UICONTROL Quick Access]**

   或者
* **[!UICONTROL Experience Cloud Home]**  > [!UICONTROL Solution picker]: **Campaign** > **[!UICONTROL Control Panel]card**

   或者

* 直接从 URL 访问：[https://experience.adobe.com/#/controlpanel](https://experience.adobe.com/#/controlpanel)

## 先决条件

在开始之前，请完成以下先决条件：

### 确认 [!DNL IMS Org ID]

您需要知道您的 [!DNL IMS org ID]。以下视频介绍查看实例 [!DNL IMS org ID] 的位置。

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*查看[!DNL IMS Org ID]（00:26 分钟）*

### 管理员权限

需要管理员权限才能访问 [!UICONTROL Control Panel]。
以下视频介绍如何向 Campaign 实例添加管理员

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*如何将管理员在产品用户档案中添加为“[!UICONTROL Administrators]”，以便能够使用[!UICONTROL Control Panel]（01:03 分钟）*

## 控制面板教程

* **管理 SFTP 服务器**

   *了解如何监控服务器容量、允许列表 IP 地址和添加 SSH 密钥：*

   * [监视服务器容量、允许列表 IP 地址和添加 SSH 密钥](/help/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.md)
   * [生成 SSH 密钥](/help/administrating/control-panel/generate-ssh-key.md)
   * [连接到 SFTP 服务器](/help/administrating/control-panel/connect-to-sftp-server.md)
* **[委派子域](/help/administrating/control-panel/subdomain-delegation.md)**

   *了解如何将子域完全委派给 Adobe Campaign*
* **[添加 SSL 证书](/help/administrating/control-panel/adding-ssl-certificates.md)**

   *了解如何添加 SSL 证书以保护子域。*

* **[Google TXT 记录管理](/help/administrating/control-panel/google-txt-record-management.md)**

   *了解如何将 Google TXT 网站验证记录添加到所有子域，这些子域用于通过 Campaign 控制面板向 Gmail 地址发送电子邮件。*

* **GPG 密钥管理**

   *了解如何在指定的 Campaign 实例上生成和安装公钥/私钥对，以加密出站数据，以及在 Campaign 实例上导入和安装公钥，以解密入站数据。*

   * [生成和安装用于数据加密的 GPG 密钥](./gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.md)
   * [使用 GPG 密钥加密数据](./gpg-key-management/using-a-gpg-key-to-encrypt-data.md)
   * [解密数据](./gpg-key-management/decrypting-data.md)

* **[故障排除](/help/administrating/control-panel/trouble-shooting.md)**

   *了解如何对控制面板进行故障排除*

## 其他资源

* [控制面板帮助中心](https://docs.adobe.com/content/help/zh-Hans/control-panel/using/control-panel-home.html)

