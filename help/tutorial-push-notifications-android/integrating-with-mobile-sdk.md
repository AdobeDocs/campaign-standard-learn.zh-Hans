---
title: 步骤 2 - 集成 Mobile SDK
description: 在此部分中，我们将将Android应用程序与Mobile SDK集成。 将Mobile SDK与Android应用程序集成
feature: Push
user: Admin
level: Experienced
jira: KT-4826
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: 913d2c08dc63e2073b3abd1de6b6b16711d817da
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# 第2步 — 集成 [!UICONTROL Mobile SDK] 使用Android应用程序

在此部分中，我们将集成 [!DNL Android] 应用程序与 [!UICONTROL Mobile SDK]. 要集成 [!UICONTROL mobile SDK] 使用 [!DNL Android] 请按照以下步骤操作：

* 打开 *ACSPushTutorial* 中的项目 [!DNL Android Studio]
* 创建一个名为的新Java类 *MainApp* 会扩展 [!DNL android.app.Application]
* 此时，您的项目结构应如下所示

![main-app](assets/android-main-app.PNG)

* 展开 [!DNL Gradle Scripts] 文件夹。 双击 [!DNL build.gradle] 模块的。 将以下依赖项粘贴到的依赖项部分 [!DNL build.gradle] 文件。 您的 [!DNL build.gradle] 文件现在应如下所示

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* 同步您的 [!DNL Android] 通过单击“立即同步”按钮来同步您的项目

## 修改 [!DNL AndroidManifest.xml]{#modify-android-manifest}

打开 *AndroidManifest.xml* 并将以下2行粘贴到清单元素之后、应用程序元素之前。 这使您的应用程序能够与外部世界通信

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

复制应用程序元素中的以下行
[!DNL android:name=".MainApp"]
保存您的 [!DNL AndroidManifest.xml]
您的 [!DNL AndroidManifest.xml] 应该像这样

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
