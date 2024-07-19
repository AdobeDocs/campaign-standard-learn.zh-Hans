---
title: 步骤4 — 设置pushidentifier
description: '**pushIdentifier**是一个字符串，其中包含用于推送通知的设备令牌。 它与Firebase发送的令牌相同，并使用MobileCore.setPushIdentifier方法传递到SDK。'
feature: Push
user: Admin
level: Experienced
jira: KT-4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 757afce50981b96b7820c987308d639a73746c0c
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# 步骤4 — 设置[!DNL pushidentifier]

**[!DNL pushidentifier]**&#x200B;是包含[!DNL Push]通知的设备令牌的字符串。 它是由[!DNL Firebase]发送并使用[!DNL MobileCore.setPushIdentifier]方法传递到SDK的相同令牌。

在[!DNL Android™]studio中打开您的项目。 删除[!DNL MainActivity] **中的整个代码，但第一行是您的包语句**&#x200B;除外。

将以下代码粘贴到[!DNL MainActivity]中：

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

## 测试您的应用程序

在继续下一步之前，现在非常适合测试您的应用程序。

* 通过单击绿色箭头或选择&#x200B;**[!DNL Run->Run'app']**&#x200B;运行您的应用程序。
* [!DNL Android™]模拟器应该启动，您应该会看到您的应用程序运行了[!DNL "Hello World"]文本。
* 打开[!DNL logcat]窗口。 搜索“[!DNL Got]”。 您应该看到从[!DNL Firebase]收到的令牌已写入日志，如下所示。 “[!DNL Got token]”之后的长字符串是发送到Adobe Campaign的[!DNL pushidentifier]。

![logcat-token](assets/logcat-got-token.PNG)

### 检查移动应用程序订阅者

登录到您的Adobe Campaign Standard实例。
导航**[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**。 打开相应的移动设备应用程序。 按Tab键转到[!UICONTROL Mobile Application Subscribers]选项卡。 您应该会看到[!UICONTROL registration token]已列出。

![移动应用程序订阅者](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>如果您在[!UICONTROL Mobile Application Subscribers]选项卡中没有看到注册令牌，请在此处停止，然后再继续。
