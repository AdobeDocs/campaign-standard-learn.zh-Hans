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
source-git-commit: 9be31e056800b806c49a2c5ffbf9f9f42b001d4c
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 13%

---

# 步骤 3 - 使用移动应用程序注册扩展

在此部分中，我们添加了用于注册用户配置文件、身份、生命周期和信号扩展的代码。 我们还必须注册Adobe Campaign Standard扩展，如以下代码中所示。

在中打开您的项目 [!DNL Android] 工作室。 删除MainApp中的整个代码 **除了第一行，即您的包语句**.

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

第32行，您必须提供[!UICONTROL  Launch] 属性的环境文件ID。 这可以从以下位置访问 [!UICONTROL environment tab] 的 [!UICONTROL Launch] 属性。

![launch-id](assets/launch-id-property.PNG)
