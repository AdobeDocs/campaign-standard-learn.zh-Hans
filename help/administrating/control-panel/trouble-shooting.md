---
title: 拍摄控制面板时出现问题
description: 控制面板允许您按实例和白名单IP地址监视和管理SFTP存储。
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# 拍摄[!UICONTROL控制面板}时遇到问题

了解如何在使用控制面板时对问题进行疑难解答。

## 登录和主页

登录和主页出现问题。

### 症状： 无法登录Adobe Experience Cloud

**要做什么：**
用户需要找到他们 [!DNL IMS Org ID] 的(xxx)。 管理员需要将用户添加到 [!UICONTROL product profile] 其要管 [!DNL “Campaign-xxx-Admins”] 理的每个实例中。 如果用户是所有实例的管理员，则他们仍可能需要将自己添加为 *[!UICONTROL user]*。

### 症状： 访问链 [!UICONTROL Adobe Experience Cloud Home] 接不 [!UICONTROL Control Panel] 显示给用户

**原因：**
用户只有在将其添加为 [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**要做什么：**
管理员需要将用户添加到 [!UICONTROL product profile] 其要管 *[!DNL Campaign-xxx-Admins]* 理的每个实例中。 如果用户是所有实例的管理员，则他们仍可能需要将自己添加为 *[!UICONTROL user]*。

### 症状： 实例未列在 [!UICONTROL Control Panel]

**原因：**
最可能的用户需要添加为缺 *[!UICONTROL user]* 失实 `!DNL Campaign-xxx-Administrators/Admin` 例的产品用户档案

**要做什么：**
管理员需要将用户添加到其要管 `Campaign-xxx-Admins` 理的每个实例的产品用户档案。 如果用户是所有实例的管理员，则他们仍可能需要将自己添加为 *[!UICONTROL user]*。

### 实用视频

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*检[!DNL IMS Org ID]查（00:26分钟）*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*如何向添加管理员[!UICONTROL product profile]以&#x200B;*[!DNL administrators]*便使用([!UICONTROL Control Panel]01:03分钟)*

### 帮助文档

* [发现[!UICONTROL控制面板]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [管理对[!UICONTROL控制面板]的权限](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## 建立与SFTP服务器（客户端或API）的连接

连接到SFTP服务器需要：

* [!UICONTROL Whitelisting] 您连接到SFTP服务器的IP地址
* 需要向Adobe Campaign注册的私钥／公钥对
* 如果直接连接到SFTP服务器，您还需要SFTP客户端软件

### 帮助文档

* [登录SFTP服务器](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)
