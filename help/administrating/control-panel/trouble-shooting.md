---
title: 控制面板故障排除
description: 控制面板允许您按实例和允许列表 IP 地址监视和管理 SFTP 存储。
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 2f0527f3d9e2248eea68079e00855cce7a96fce4
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 100%

---


# 控制面板故障排除

了解如何在使用控制面板时进行故障排除。

## 登录和主页

登录和主页出现问题。

### 症状：无法登录 Adobe Experience Cloud

**要做什么：**
用户需要找到他们的 [!DNL IMS Org ID] (xxx)。管理员需要将用户添加到其要管理的每个实例的 [!UICONTROL product profile][!DNL “Campaign-xxx-Admins”]。如果用户是所有实例的管理员，则他们仍可能需要将自己添加为 *[!UICONTROL user]*。

### 症状： [!UICONTROL Adobe Experience Cloud Home]中访问 [!UICONTROL Control Panel]的链接不显示给用户

**原因：**
用户只有在将其添加为 [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin` 的用户时才能看到链接

**要做什么：**
管理员需要将用户添加到 [!UICONTROL product profile]其要管理的每个实例的 *[!DNL Campaign-xxx-Admins]*。如果用户是所有实例的管理员，则他们仍可能需要将自己添加为 *[!UICONTROL user]*。

### 症状：实例未列在 [!UICONTROL Control Panel]中

**原因：**
最可能的原因是用户需要添加为缺失实例的 *[!UICONTROL user]*&#x200B;产品用户档案`!DNL Campaign-xxx-Administrators/Admin`

**要做什么：**
管理员需要将用户添加到其要管理的每个实例的产品用户档案`Campaign-xxx-Admins`。如果用户是所有实例的管理员，则他们仍可能需要将自己添加为 *[!UICONTROL user]*。

### 有用视频

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*检查[!DNL IMS Org ID]（00:26 分钟）*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*如何添加管理员到[!UICONTROL product profile]*[!DNL administrators]*以便使用[!UICONTROL Control Panel]（01:03 分钟）*

### 帮助文档

* [了解 [!UICONTROL Control Panel]](https://docs.adobe.com/content/help/zh-Hans/control-panel/using/control-panel-home.html)
* [管理 [!UICONTROL Control Panel]](https://docs.adobe.com/content/help/zh-Hans/control-panel/using/control-panel-home.html) 的权限

## 建立与 SFTP 服务器（客户端或 API）的连接

连接到 SFTP 服务器需要：

* [!UICONTROL allow listing] 您连接到 SFTP 服务器的 IP 地址
* 需要向 Adobe Campaign 注册的私钥/公钥对
* 如果直接连接到 SFTP 服务器，您还需要 SFTP 客户端软件

### 帮助文档

* [登录 SFTP 服务器](https://docs.adobe.com/content/help/zh-Hans/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)

