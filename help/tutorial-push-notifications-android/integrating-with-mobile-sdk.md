---
title: 步骤 2 - 集成 Mobile SDK
description: 在本部分中，我们将将Android应用程序与Mobile SDK相集成。 将Mobile SDK与Android应用程序集成
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# 步骤2 — 集成 [!UICONTROL Mobile SDK] 与Android应用程序

在本部分中，我们将 [!DNL Android] 应用程序 [!UICONTROL Mobile SDK]. 集成 [!UICONTROL mobile SDK] 和 [!DNL Android] 应用程序，请执行以下步骤：

* 打开 *ACSPush教程* 项目 [!DNL Android Studio]
* 创建一个名为 *MainApp* 延伸 [!DNL android.app.Application]
* 此时的项目结构应如下所示

![主应用程序](assets/android-main-app.PNG)

* 展开 [!DNL Gradle Scripts] 文件夹。 双击 [!DNL build.gradle] 的子目录。 将以下依赖项粘贴到的依赖项部分 [!DNL build.gradle] 文件。 您的 [!DNL build.gradle] 现在应如下所示

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![模块 — Gradle](assets/module-build-gradle.PNG)

* 同步 [!DNL Android] 单击“立即同步”按钮以同步项目

## 修改 [!DNL AndroidManifest.xml]{#modify-android-manifest}

打开 *AndroidManifest.xml* 并将以下2行粘贴到清单元素之后和应用程序元素之前。 这样，您的应用程序便能够与外部世界进行通信

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

在应用程序元素中复制以下行
[!DNL android:name=".MainApp"]
保存 [!DNL AndroidManifest.xml]
您的 [!DNL AndroidManifest.xml] 应该是这样

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
