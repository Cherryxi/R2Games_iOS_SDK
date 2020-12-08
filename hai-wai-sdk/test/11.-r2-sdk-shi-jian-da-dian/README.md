# 11. R2 SDK事件打点

为了方便游戏研发进行打点功能的集成，R2SDKFramework集成了SDK平台、FireBase Analytics、Adjust 三个方面的打点服务。其中Firebase为必选打点服务,作为SDK平台打点的参考。由于SDK平台打点和Adjust打点事件需求可能不同，故开放两个接口，一个是SDK平台打点trackEvent: ，另一个是第三方打点trackThirdPartyEvent:,请研发方按需接入，如有不详，请咨询SDK技术人员。 您若想了解更多资料，请参照官方技术文档。

 Firebase:[https://firebase.google.com/docs/analytics/get-started?authuser=0&platform=ios](https://firebase.google.com/docs/analytics/get-started?authuser=0&platform=ios) Adjust:[https://github.com/adjust/ios\_sdk\#sdk-add](https://github.com/adjust/ios_sdk#sdk-add)

