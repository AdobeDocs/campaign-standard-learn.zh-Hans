---
title: 第1步——创建Android应用程序并配置为使用Firebase Cloud消息传递
description: 在这部分，我们将从 [!DNL Android] App to receive [!UICONTROL Push notifications] Adobe Campaign Standard创建。 要接收推送通知，该应用程序需要在Google's注册 [!DNL Firebase Cloud Service]。
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# 步骤1 —— 创建应 [!DNL Android] 用程序并配置为使用 [!DNL Firebase Cloud Messaging]

在此部分，您将创建应 [!DNL Android] 用程序以接收 [!UICONTROL Push notifications] 来自Adobe Campaign Standard的发送。 要接收推送通知，该应用程序需要在Google的注册 [!DNL Firebase Cloud Service]。

1. 登录您的 [!DNL Firebase] 帐户。

   [!DNL Firebase] 是Google的移动平台，可帮助您快速开发高质量应用。 如果您没有帐 [!DNL Firebase] 户，请从此处 [创建](https://firebase.google.com)。

2. 启动 [!DNL Android Studio]
3. Click **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. 选择 **[!UICONTROL Empty Activity]** 并单击 **[!UICONTROL Next]。**

   ![android-project](assets/android-project.PNG)

5. 为项目提供有意义的名称。

   为了演示，我们已将我们的项目命名为 *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. 接受默认包名称，然后单 **[!DNL Finish]** 击以创建项目。
7. 您的项目结构应类似于下面的屏幕快照

   ![android-project-structure](assets/android-project-structure.PNG)

8. 单击 **[!UICONTROL Tools]** > **[!UICONTROL Firebase].**(这会将项目添加到[!DNL Firebase])
9. 单击 **[!UICONTROL Set up Firebase Cloud Messaging]。**

   ![设置firebase](assets/android-project-firebase-messaging.PNG)

10. 单击 **[!UICONTROL Connect to Firebase]。**
11. 将应用程序连接到Firebase后，单击 **[!UICONTROL Add FCM to your app]。**
12. 单击 **[!UICONTROL Accept Changes]。**

   将FCM添加到应用程序时，向导需要您的权限才能对项目进行一些更改。

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

成功将应用程序与Firebase集成后，您应会收到如下消息：

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[确保在控制台中列出您的 [!DNL Firebase ]项目](https://console.firebase.google.com/)

## 配置设 [!UICONTROL Push Channel] 置

1. 登录控 [!DNL Firebase] 制台
2. 打开项 **[!UICONTROL ACSPushTutorial]** 目。
3. 单击齿轮 **图标** ，然后打开项目设置

   ![项目设置](assets/firebase-project-settings.PNG)

4. Tab to the **[!UICONTROL Cloud Messaging]** tab.
5. 复制服务器密钥

   ![服务器密钥](assets/firebase-server-key.PNG)

6. 登录Adobe Campaign Standard实例
7. Click **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. 选择相应的 **[!UICONTROL Mobile Application Property]。**
9. 单击 **[!DNL Android]部分&#x200B;**中的&#x200B;**[!UICONTROL Push Channel settings]**图标。
10. 将服务器密钥粘贴到服务器密钥字段中。

如果一切顺利，您应看到一条SUCCESS消息。

![推送渠道设置](assets/push-channel-settings.PNG)

总而言之，我们已创建 [!DNL Android App] 并连接 [!DNL Android App] 了 [!DNL Firebase]。 然后，我们将移动应用程序与Adobe Campaign [!DNL Android App] 连接， [!DNL Android] 方法是将应用程序的服务器密钥粘贴到Adobe Campaign Standard中的移动应用程序。
