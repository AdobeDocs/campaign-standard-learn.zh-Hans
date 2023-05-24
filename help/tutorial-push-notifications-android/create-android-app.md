---
title: 步骤1 — 创建Android应用程序并配置以使用Firebase Cloud Messaging
description: 在本部分中，我们将创建 [!DNL Android] 要接收的应用程序 [!UICONTROL Push notifications] 发送自Adobe Campaign Standard。 要接收推送通知，需要在Google的注册中注册应用程序 [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---

# 步骤1 — 创建 [!DNL Android] 要使用的应用程序和配置 [!DNL Firebase Cloud Messaging]

在此部分中，您将创建 [!DNL Android] 要接收的应用程序 [!UICONTROL Push notifications] 发送自Adobe Campaign Standard。 要接收推送通知，需要在Google的注册中注册应用程序 [!DNL Firebase Cloud Service].

1. 登录 [!DNL Firebase] 帐户。

   [!DNL Firebase] 是Google的移动平台，可帮助您快速开发高质量应用程序。 如果您没有 [!DNL Firebase] 帐户，请创建一个 [从此处](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. 单击 **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. 选择 **[!UICONTROL Empty Activity]** 并单击 **[!UICONTROL Next]。**

   ![android-project](assets/android-project.PNG)

5. 为项目提供一个有意义的名称。

   在本演示中，我们已将我们的项目命名为 *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. 接受默认程序包名称并单击 **[!DNL Finish]** 以创建您的项目。
7. 您的项目结构应类似于下面的屏幕快照

   ![android-project-structure](assets/android-project-structure.PNG)

8. 单击 **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (这会将项目添加到 [!DNL Firebase])
9. 单击 **[!UICONTROL Set up Firebase Cloud Messaging]。**

   ![设置firebase](assets/android-project-firebase-messaging.PNG)

10. 单击 **[!UICONTROL Connect to Firebase]。**
11. 将应用程序连接到Firebase后，单击 **[!UICONTROL Add FCM to your app].**
12. 单击 **[!UICONTROL Accept Changes]。**

   将FCM添加到应用程序时，向导需要您的权限才能对项目进行某些更改。

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

成功将应用程序与Firebase集成后，您应会收到如下所示的消息：

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[确保您的项目列在 [!DNL Firebase ]控制台](https://console.firebase.google.com/)

## 配置 [!UICONTROL Push Channel] 设置

1. 登录 [!DNL Firebase] 控制台
2. 打开 **[!UICONTROL ACSPushTutorial]** 项目。
3. 单击 **齿轮图标** 并打开项目设置

   ![项目设置](assets/firebase-project-settings.PNG)

4. 按Tab键转到 **[!UICONTROL Cloud Messaging]** 选项卡。
5. 复制服务器密钥

   ![server-key](assets/firebase-server-key.PNG)

6. 登录Adobe Campaign Standard实例
7. 单击 **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. 选择适当的 **[!UICONTROL Mobile Application Property].**
9. 单击 **[!DNL Android]图标** 在 **[!UICONTROL Push Channel settings]** 部分。
10. 将服务器密钥粘贴到“服务器密钥”字段中。

如果一切顺利，您应会看到一条成功消息。

![推送渠道设置](assets/push-channel-settings.PNG)

总之，我们创建了一个 [!DNL Android App] 并连接 [!DNL Android App] 替换为 [!DNL Firebase]. Adobe Campaign然后，我们通过 [!DNL Android App] 通过粘贴 [!DNL Android] 应用程序指向Adobe Campaign Standard中移动设备应用程序的服务器密钥。
