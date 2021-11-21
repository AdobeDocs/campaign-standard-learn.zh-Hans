---
title: 步骤 3 - 使用移动应用程序注册扩展
description: 在本部分中，我们将添加代码以注册UserProfile、Identity、Lifecycle和Signal扩展。
feature: Push
kt: 4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 11%

---

# 步骤 3 - 使用移动应用程序注册扩展

在本部分中，我们将添加代码以注册用户配置文件、身份、生命周期和信号扩展。 这些扩展是 [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). 我们还需要注册Adobe Campaign Standard扩展，如以下代码所示。

在中打开您的项目 [!DNL Android] 工作室。 删除MainApp中的整个代码 **除了第一行是包语句**.

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

第32行[!UICONTROL  Launch] 属性的环境文件ID。 可从 [!UICONTROL environment tab] 您的 [!UICONTROL Launch] 属性。

![launch-id](assets/launch-id-property.PNG)
