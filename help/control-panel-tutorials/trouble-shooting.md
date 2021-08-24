---
title: 控制面板故障排除
description: 利用控制面板，可按实例监控和管理SFTP存储并允许列表IP地址。
feature: 控制面板
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!UICONTROL Control Panel] 故障排除

了解如何在使用控制面板时进行故障排除。

## 登录和主页

登录和主页出现问题。

### 症状：无法登录Adobe Experience Cloud

**要做什么：**
用户必须找到 [!DNL IMS Org ID] 其(xxx)。管理员必须将用户添加到其要管理的每个实例的[!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”]中。 如果用户是所有实例的管理员，则必须将自己添加为&#x200B;*[!UICONTROL user]*。

### 症状： [!UICONTROL Adobe Experience Cloud Home]中访问 [!UICONTROL Control Panel]的链接不显示给用户

**原因：**
用户只有在将其添加为 [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin` 的用户时才能看到链接

**要做什么：**
管理员必须将用户添加 [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* 到要管理的每个实例的。如果用户是所有实例的管理员，则必须将自己添加为&#x200B;*[!UICONTROL user]*。

### 症状：实例未列在 [!UICONTROL Control Panel]中

**原因：**
最可能的情况是，必须将用户添加 *[!UICONTROL user]* 为缺 `Campaign-xxx-Administrators/Admin` 少实例的产品用户档案

**要做什么：**
管理员必须将用户添加到其要管理的 `Campaign-xxx-Admins` 每个实例的产品配置文件中。如果用户是所有实例的管理员，则必须将自己添加为&#x200B;*[!UICONTROL user]*。

### 实用视频

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*查看 [!DNL IMS Org ID]（00:26 分钟）*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*如何添加管理员到 [!UICONTROL product profile][!DNL administrators]以便使用 [!UICONTROL Control Panel]（01:03 分钟）*

### 帮助文档

* [了解 [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=zh-Hans)
* [管理 [!UICONTROL Control Panel] 的权限](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## 建立与 SFTP 服务器（客户端或 API）的连接

连接到 SFTP 服务器需要：

* [!UICONTROL allow listing] 您连接到 SFTP 服务器的 IP 地址
* 必须在Adobe Campaign中注册的私钥/公钥对
* 如果直接连接到SFTP服务器，则需要SFTP客户端软件

### 帮助文档 {#helpful-docs}

* [登录 SFTP 服务器](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
