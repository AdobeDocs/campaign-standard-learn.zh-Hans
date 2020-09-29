---
title: 第4步——设置推信器
description: '**pushIdentifier**是包含推送通知设备令牌的字符串。 这是由Firebase发送并使用MobileCore.setPushIdentifier方法传递到SDK的相同令牌。'
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: aa01c2f8fe1560468d0d8f3fae6291bb82f9a21f
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# 第4步——设置 [!DNL pushidentifier]

该 **[!DNL pushidentifier]** 字符串包含通知的设备令牌 [!DNL Push] 。 这是由发送并使用方 [!DNL Firebase] 法传递到SDK的相同标 [!DNL MobileCore.setPushIdentifier] 记。

在Studio中打开 [!DNL Android ]项目。 删除中的整个代 [!DNL MainActivity] 码， **但第一行是包语句**。

将以下代码粘贴到 [!DNL MainActivity]:

<!--
Removed `{.line-numbers}` below
-->

```java
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## 测试应用程序

现在是测试应用程序的好时机，然后再继续。

* 通过单击绿色箭头或选择来运行应用程 **[!DNL Run->Run'app']**&#x200B;序。
* 模拟 [!DNL Android] 器应开始，您应看到您的应用程序运行 [!DNL "Hello World" ]着文本。
* 打开窗 [!DNL logcat] 口。 搜索“[!DNL Got]”。 您应当看到从写入日志中收 [!DNL Firebase] 到的令牌，如下所示。 “”后面的长[!DNL Got token]字符串 [!DNL pushidentifier ]是发送给Adobe Campaign的。

![logcat-token](assets/logcat-got-token.PNG)

### 检查移动应用程序订阅者

登录您的Adobe Campaign Standard实例。
导航 **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**。 打开相应的移动应用程序。 Tab to the [!UICONTROL Mobile Application Subscribers] tab. 您应当看到列 [!UICONTROL registration token ]表。

![移动——应用程序——用户](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>如果在继续操作之前未在选项卡“停止” [!UICONTROL Mobile Application Subscribers] 中看到注册令牌。
