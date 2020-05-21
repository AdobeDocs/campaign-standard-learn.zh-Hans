---
title: 步骤3 —— 使用移动应用程序注册扩展
description: 在本部分，我们将添加代码来注册UserProfile、Identity、Lifecycle和Signal扩展。
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 步骤3 —— 使用移动应用程序注册扩展

在本部分中，我们将添加代码来注册用户用户档案、身份、生命周期和信号扩展。 这些扩展是[! [UICONTROL移动核心扩展]的一部分](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core)。 我们还需要注册Adobe Campaign标准扩展，如下面的代码所示。

在Studio中打开 [!DNL Android] 项目。 删除MainApp中的整个代 **码，但第一行是包语句**。

将以下代码粘贴到MainApp中

```java{.line-numbers}
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

第32行，您需要提供属性[!UICONTROL  Launch] 的环境文件id。 您可以从您的属 [!UICONTROL environment tab] 性访问 [!UICONTROL Launch] 此项。

![启动ID](assets/launch-id-property.PNG)
