---
title: 步骤 3 - 使用移动应用程序注册扩展
description: 在此部分中，我们添加了用于注册UserProfile、Identity、Lifecycle和Signal扩展的代码。
feature: Push
user: Admin
level: Experienced
jira: KT-4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
TQID: 'https://experienceleague.adobe.com/WjKV0qe9zi7cV37Wn54BJdI91n92i302t4k-yMIenZ4'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: a4671286-a59f-47e3-b97b-90627a1977d5
    internal-label: Communication channels
subfeature_v2:
  - id: a4657621-810c-498b-8a27-7ced9c176dda
    internal-label: Push notifications
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 508c3590ce956401ccfba3a256000cbc5849a684
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 14%
---
# 步骤 3 - 使用移动应用程序注册扩展

在此部分中，我们添加了用于注册用户配置文件、身份、生命周期和信号扩展的代码。 我们还必须注册Adobe Campaign Standard扩展，如以下代码中所示。

在[!DNL Android]工作室中打开您的项目。 删除MainApp **中的整个代码，但第一行是您的包语句**&#x200B;除外。

将以下代码粘贴到MainApp中

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

第32行，您必须提供[!UICONTROL  Launch]属性的环境文件ID。 可从[!UICONTROL Launch]属性的[!UICONTROL environment tab]访问。

![启动ID](assets/launch-id-property.PNG)
