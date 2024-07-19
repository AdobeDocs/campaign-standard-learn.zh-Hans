---
title: 步骤 5 - 传播通知
description: 在本部分中，我们将使用Android Notification Manager.Firebase传播从Adobe Campaign收到的消息
feature: Push
jira: KT-4829
user: Admin
level: Experienced
doc-type: tutorial
activity: use
team: TM
exl-id: b0e01224-4ddc-4999-b8c6-794e49245428
source-git-commit: 200dcb4d6698c174f7fde508779609b11043d031
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---

# 添加服务以发送通知

在本部分中，我们将使用[!DNL Android Notification Manager]传播从Adobe Campaign收到的消息。 [!DNL Notification manager]用于通知用户发生的事件。
下面是您告知用户后台发生一些事件的方式：

* 启动[!DNL Android Studio]
* 打开&#x200B;*[!DNL ACSPushTutorial]*&#x200B;项目
* 展开项目结构
* 右键单击包文件夹([!DNL com.example.acspushtutorial])和[!DNL New ->Java Class]
* 为此类命名&#x200B;*[!DNL MyService]*&#x200B;并确保它扩展[!DNL FirebaseMessagingService]
* 在此类中创建&#x200B;*[!DNL sendNotification]*&#x200B;方法。 在此方法中，您需要使用[!DNL NotificationCompat.Builder]对象设置通知的内容和渠道。 若要显示通知，请调用[!DNL NotificationManagerCompat.notify()]，向其传递通知的唯一ID和[!DNL NotificationCompat.Builder.build()]的结果。

<!--
Removed `{.line-numbers}` below
-->

```java
package com.example.pushmessaging;
import android.app.NotificationChannel;
import android.app.NotificationManager;
import android.app.PendingIntent;
import android.content.Context;
import android.content.Intent;
import android.media.RingtoneManager;
import android.net.Uri;
import android.os.Build;
import android.util.Log;

import androidx.core.app.NotificationCompat;

import com.google.firebase.messaging.FirebaseMessagingService;
import com.google.firebase.messaging.RemoteMessage;

import java.util.Map;

public class MyService extends FirebaseMessagingService {
@Override
public void onMessageReceived(RemoteMessage remoteMessage)
{
Map<String,String> data  = remoteMessage.getData();
Log.d("data payload: ", data.toString());
sendNotification(remoteMessage);
}


private void sendNotification(RemoteMessage message) {
Intent intent = new Intent(this, MainActivity.class);
intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
PendingIntent pendingIntent = PendingIntent.getActivity(this, 0 /* Request code */, intent, PendingIntent.FLAG_ONE_SHOT);

String channelId = "0";
Uri defaultSoundUri = RingtoneManager.getDefaultUri(RingtoneManager.TYPE_NOTIFICATION);
NotificationCompat.Builder notificationBuilder =
        new NotificationCompat.Builder(this, channelId)
                .setSmallIcon(R.drawable.ic_launcher_background)
                .setContentTitle("Message from AEM")
                .setContentText(message.getData().get("body"))
                .setAutoCancel(true)
                .setSound(defaultSoundUri)
                .setContentIntent(pendingIntent);

NotificationManager notificationManager =
        (NotificationManager) getSystemService(Context.NOTIFICATION_SERVICE);

// Since android Oreo notification channel is needed.
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
    NotificationChannel channel = new NotificationChannel(channelId,
            "Channel human readable title",
            NotificationManager.IMPORTANCE_DEFAULT);
    notificationManager.createNotificationChannel(channel);
}

notificationManager.notify(0 /* ID of notification */, notificationBuilder.build());
}
}
```

## 修改[!DNL AndroidManifest.xml]

将创建的服务添加到您的[!DNL AndroidManifest.xml]。 最终[!DNL AndroidManifest.xml]应如下所示：

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.pushmessaging">

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
        <service
            android:name=".MyService"
            android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.MESSAGING_EVENT" />
            </intent-filter>
        </service>

        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## 运行应用程序

通过单击工具栏或[!DNL Run]菜单中的&#x200B;**绿色箭头**&#x200B;运行应用程序。
