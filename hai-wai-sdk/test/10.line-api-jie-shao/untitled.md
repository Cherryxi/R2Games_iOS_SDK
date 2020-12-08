# 10.2 初始化接口

调用代码前，请引入头文件\#import &lt;LineSDK/LineSDK.h&gt;

请在AppDelegate方法中的application:openURL:options:方法中调用LIneSDK的handleOpenURL 方法，来处理line登录的结果，示例如下：

```objectivec
-(BOOL)application:(UIApplication *)app openURL:(NSURL *)url options:(NSDictionary<UIApplicationOpenURLOptionsKey,id> *)options{
    return [[LineSDKLogin sharedInstance]handleOpenURL:url];
}

- (BOOL)application:(UIApplication *)application continueUserActivity:(NSUserActivity *)userActivity restorationHandler:(void (^)(NSArray<id<UIUserActivityRestoring>> * _Nullable))restorationHandler
{
    if ([[LineSDKLogin sharedInstance] handleOpenURL:userActivity.webpageURL]) {
        return YES;
    }
    // Your other code to handle universal links and/or user activities.
    return YES;
}

```

