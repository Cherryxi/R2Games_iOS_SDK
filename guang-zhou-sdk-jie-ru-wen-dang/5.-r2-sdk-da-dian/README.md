# 5. R2 SDK打点

说明：SDK支持四个厂商的事件打点服务，分别为**FireBase Analytics**、**AppsFlyer**、**Facebook**、**Adjust**. 请研发方在对接SDK事件打点功能时，务必和游戏运营或者市场人员确认需要使用哪些厂商的打点服务。

 所有事件分为两大部分：**基础事件**和**游戏内打点事件**。 

对于基础事件如**激活、注册、登录、支付**等。这些事件SDK内部会自动打点，无需游戏研发方再次对这些事件进行打点。研发方请注意若使用R2 SDK自动打点功能，则无需对激活、注册、登录、支付事件进行重复打点。 

对于**游戏内打点事件**，即SDK无法自动打点的事件，需要游戏方自行打点。这些事件您可以通过SDK的事件打点方法进行打点。

 您若不需要SDK自动打点，想手动接入。也可以在配置文件中关闭渠道。具体关闭方式可在**R2TrackerConfiguration.plist**文件中将相应渠道的**activate**设为**NO**。

**R2EventConfiguration.plist**文件里包含了SDK内部打点的数据，**R2TrackerConfiguration.plist为配置打点服务的文件。请确保这两个文件拖入您的Xcode工程目录里。**

您若想了解更多，请参照官方技术文档。 

Firebase:[https://firebase.google.com/docs/analytics/get-started?authuser=0&platform=ios](https://firebase.google.com/docs/analytics/get-started?authuser=0&platform=ios) 

AppsFlyer:[https://support.appsflyer.com/hc/en-us/articles/207032066\#integration](https://support.appsflyer.com/hc/en-us/articles/207032066#integration) 

Facebook:[https://developers.facebook.com/docs/app-events/getting-started-app-events-ios/\#log-manually](https://developers.facebook.com/docs/app-events/getting-started-app-events-ios/#log-manually) 

Adjust:[https://github.com/adjust/ios\_sdk\#sdk-add](https://github.com/adjust/ios_sdk#sdk-add)



