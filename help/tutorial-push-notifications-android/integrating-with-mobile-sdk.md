---
title: 第2步——集成Mobile SDK
description: 在此部分，我们将将Android应用程序与Mobile SDK集成。 将移动SDK与Android应用程序集成
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# 步骤2 —— 与Android应 [!UICONTROL Mobile SDK] 用程序集成

在此部分，我们将将应用程序 [!DNL Android] 与集成 [!UICONTROL Mobile SDK]。 要与应 [!UICONTROL mobile SDK] 用程 [!DNL Android] 序集成，请执行以下步骤：

* 在中打 *开ACSPush* Tutorial项目 [!DNL Android Studio]
* 新建一个名为MainApp的 *类* ，它扩展 [!DNL android.app.Application]
* 此时的项目结构应如下所示

![主应用程序](assets/android-main-app.PNG)

* 展开文 [!DNL Gradle Scripts] 件夹。 多次单 [!DNL build.gradle] 击模块。 将以下依赖关系粘贴到文件的“依赖关系” [!DNL build.gradle] 部分。 您的 [!DNL build.gradle] 文件现在应当如下

```java{.line-numbers}
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![模块图](assets/module-build-gradle.PNG)

* 通过单 [!DNL Android] 击“立即同步”按钮同步项目以同步项目

## 修改 [!DNL AndroidManifest.xml]{#modify-android-manifest}

打 *开AndroidManifest* .xml，在清单元素之后和应用程序元素之前粘贴以下2行。 这使您的应用程序能够与外部世界通信

```xml{.line-numbers}
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

复制应用程序元素中的以[!DNL android:name=".MainApp"]下行保 [!DNL AndroidManifest.xml]存 [!DNL AndroidManifest.xml] 应如下

```xml{.line-numbers}
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