---
title: 步骤4 — 设置推信符
description: '**pushIdentifier**是包含推送通知设备令牌的字符串。 这是由Firebase发送的、使用MobileCore.setPushIdentifier方法传递到SDK的相同令牌。'
feature: 推送
topic: 移动
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
translation-type: tm+mt
source-git-commit: ddbb0843ea45a83d9ab5bfa0877287f6ba7d6210
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# 步骤4 — 设置[!DNL pushidentifier]

**[!DNL pushidentifier]**&#x200B;是包含[!DNL Push]通知的设备令牌的字符串。 这是由[!DNL Firebase]发送并使用[!DNL MobileCore.setPushIdentifier]方法传递到SDK的相同令牌。

在[!DNL Android ]studio中打开您的项目。 删除[!DNL MainActivity] **中的整个代码，但包语句**&#x200B;的第一行除外。

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

## 测试应用程序

现在是测试应用程序的好时机，然后再继续。

* 单击绿色箭头或选择&#x200B;**[!DNL Run->Run'app']**&#x200B;运行您的应用程序。
* [!DNL Android]模拟器应开始，您会看到应用程序使用[!DNL "Hello World" ]文本运行。
* 打开[!DNL logcat]窗口。 搜索“[!DNL Got]”。 您应当看到从[!DNL Firebase]收到的标记写入日志，如下所示。 “[!DNL Got token]”后面的长字符串是发送到Adobe Campaign的[!DNL pushidentifier ]。

![logcat-token](assets/logcat-got-token.PNG)

### 检查移动应用程序订阅者

登录Adobe Campaign Standard实例。
导航**[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**。 打开相应的移动应用程序。 [!UICONTROL Mobile Application Subscribers]选项卡。 应当列出[!UICONTROL registration token ]。

![移动应用程序用户](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>如果在继续操作之前，未在[!UICONTROL Mobile Application Subscribers]选项卡STOP此处看到注册令牌。
