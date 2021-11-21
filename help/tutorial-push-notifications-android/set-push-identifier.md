---
title: 步骤4 — 设置pushidentifier
description: '**pushIdentifier**是一个字符串，其中包含用于推送通知的设备令牌。 它是由Firebase发送并使用MobileCore.setPushIdentifier方法传递到SDK的令牌。'
feature: Push
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 步骤4 — 设置 [!DNL pushidentifier]

的 **[!DNL pushidentifier]** 是一个字符串，其中包含的设备令牌 [!DNL Push] 通知。 它是发送的相同令牌 [!DNL Firebase] 和会使用 [!DNL MobileCore.setPushIdentifier] 方法。

在中打开您的项目 [!DNL Android™ ]工作室。 删除 [!DNL MainActivity] **除了第一行是包语句**.

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

## 测试您的应用程序

现在，是测试应用程序以后再继续操作的好时机。

* 通过单击绿色箭头或选择 **[!DNL Run->Run'app']**.
* 的 [!DNL Android™] 模拟器应该启动，您应该看到应用程序正在运行 [!DNL "Hello World" ]文本。
* 打开 [!DNL logcat] 窗口。 搜索“[!DNL Got]&quot; 您应会看到从 [!DNL Firebase] 写入日志，如下所示。 “[!DNL Got token]“是 [!DNL pushidentifier ]发送到Adobe Campaign。

![logcat-token](assets/logcat-got-token.PNG)

### 检查移动应用程序订阅者

登录到Adobe Campaign Standard实例。
导航 **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. 打开相应的移动应用程序。 选项卡 [!UICONTROL Mobile Application Subscribers] 选项卡。 您应会看到 [!UICONTROL registration token ]列出。

![移动应用程序订阅者](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>如果您在 [!UICONTROL Mobile Application Subscribers] 选项卡停止，然后再继续。
