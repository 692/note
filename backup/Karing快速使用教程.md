### 主要特性[​](about:blank#%E4%B8%BB%E8%A6%81%E7%89%B9%E6%80%A7 "主要特性的直接链接")

*   使用简单, 快速上手, 一键起飞
*   支持Clash/Clash.Meta、V2ray(支持批量)、Stash、Sing-box、Shadowsocks、Sub、Github配置链接及配置导入.
*   支持主流协议, 包括 Shadowsocks,ShadowsocksR,VMess, Vless, Trojan, Tuic, Socks, Http, Hysteria, Hysteria2, Wireguard 等.
*   一套路由规则应用于多个订阅源, 自动选择高效节点.
    *   支持自定义路由规则组、节点组.
    *   为小白用户定制默认路由规则组 - 开箱即用.
*   内置支持 魔改版sing-box核心, 性能优越.
*   支持备份和同步, 一次配置多设备同步.
*   增加新手模式 配置更简单.

### 界面预览[​](about:blank#%E7%95%8C%E9%9D%A2%E9%A2%84%E8%A7%88 "界面预览的直接链接")

![软件界面](https://karing.app/assets/images/qs-1-2baf458e67dd732ebf6c52b409a05d61.png#center)

一、 下载[​](about:blank#%E4%B8%80-%E4%B8%8B%E8%BD%BD "一、 下载的直接链接")
---------------------------------------------------------------

### iOS(iphone/ipad)/Mac用户[​](about:blank#iosiphoneipadmac%E7%94%A8%E6%88%B7 "iOS(iphone/ipad)/Mac用户的直接链接")

*   AppStore(搜索关键词 karing vpn)
    *   [https://apps.apple.com/us/app/karing/id6472431552](https://apps.apple.com/us/app/karing/id6472431552)
*   TestFlight
    *   [https://testflight.apple.com/join/RLU59OsJ](https://testflight.apple.com/join/RLU59OsJ)
*   注意: 需要非中国大陆AppStore账号
    *   不会注册?请参考 [苹果ID专卖小店](https://dot.karing.app/pi.html?r_c=xda)

### Windows/Android/Harmony用户[​](about:blank#windowsandroidharmony%E7%94%A8%E6%88%B7 "Windows/Android/Harmony用户的直接链接")

*   下载最新版安装包
    *   [https://github.com/KaringX/karing/releases/latest](https://github.com/KaringX/karing/releases/latest)
*   Windows 建议下载安装包:文件名规则 karing\_xxx\_windows\_x64.exe (xxx为版本号)
    *   下载后运行安装(如果遇到defender拦截,请点击'显示详细信息' - '仍要运行' 即可安装)
    *   如果github.com无法访问,也可使用 [win\_x64 备用下载链接](https://dot.karing.app/client.html?p=windows)
*   Android/Harmony 下载: karing\_xxx\_android\_arm64.apk
    *   如无法访问,也可使用 [android 备用下载链接](https://dot.karing.app/client.html?p=android)
    *   [APKPure 应用市场](https://apkpure.com/p/com.nebula.karing)

### 系统要求[​](about:blank#%E7%B3%BB%E7%BB%9F%E8%A6%81%E6%B1%82 "系统要求的直接链接")

*   Windows >= 10
*   Android >= 8
*   IOS >= 15
*   MacOS >= 12
*   TvOS >= 17

### 购买价格[​](about:blank#%E8%B4%AD%E4%B9%B0%E4%BB%B7%E6%A0%BC "购买价格的直接链接")

*   karing 全平台**免费**

推广

*   这里收集了一些比较靠谱的收费节点, 请移步 [节点分享](https://dot.karing.app/pi.html?r_c=cn)
*   怎么获取免费流量, 请看 [新用户福利](https://karing.app/newuser)

二、快速使用/quickstart[​](about:blank#%E4%BA%8C%E5%BF%AB%E9%80%9F%E4%BD%BF%E7%94%A8quickstart "二、快速使用/quickstart的直接链接")
------------------------------------------------------------------------------------------------------------------

1.  点击APP左上角设置按钮 -> 进入 `添加配置`
    
    *   打开 `添加配置链接`(也可以通过导入或者扫描添加)
        *   ![设置](data:image/png;base64,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)
    *   将 Clash/V2ray/SS 等配置链接或者配置内容粘贴到输入框
        *   如果没有配置,可以通过 [新用户福利](https://karing.app/newuser) 申请
    *   点击右上角添加按钮
        *   ![添加配置](https://karing.app/assets/images/qs-3-a06e6b8d632e415046ca393ae1b77e2c.png)
2.  返回到主屏
    
    *   默认已为您选择了一个服务器
        *   点击下方的服务器名称可以重新选择服务器
    *   点击 连接(开关按钮) 即可开始您的网络之旅了
        *   ![连接](data:image/png;base64,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)

### 如何选择更快的服务器[​](about:blank#%E5%A6%82%E4%BD%95%E9%80%89%E6%8B%A9%E6%9B%B4%E5%BF%AB%E7%9A%84%E6%9C%8D%E5%8A%A1%E5%99%A8 "如何选择更快的服务器的直接链接")

*   点击主屏下方的服务器名称后，打开 '选择服务器'
*   点击 '延时检测' 按钮
    *   ![节点列表](https://karing.app/assets/images/qs-5-8e4e4900ccaa5acaf63a0878d2243547.png)
*   稍等一会后, 每个服务器后面会展示对应服务器延时
    *   延时数值越低越好
    *   三角提示的表示有错误,服务器可能无法使用,点击后可以查看具体错误信息
*   选择一个延时数值低的服务器即可
*   建议使用 `自动选择` 服务器功能

### Apple TV(tvos)版本如何使用[​](about:blank#apple-tvtvos%E7%89%88%E6%9C%AC%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8 "Apple TV(tvos)版本如何使用的直接链接")

*   下载安装Apple TV(tvos)及移动端Karing
*   移动端安装上述流程\[1\]添加配置
*   打开Apple TV端Karing
*   使用安装有Karing的移动设备扫描Apple TV端Karing的二维码
*   扫描连接成功后,移动端Karing会进入Apple TV控制中心
*   点击右上角的 \[上传\] 按钮,同步核心配置(同步后,Apple TV端Karing会多一个 \[连接\] 按钮)
*   回到Apple TV端Karing, 开启连接即可
*   Apple TV端Karing连接成功后,可以在移动端Karing Apple TV控制中心查看相关状态信息

三、进阶功能[​](about:blank#%E4%B8%89%E8%BF%9B%E9%98%B6%E5%8A%9F%E8%83%BD "三、进阶功能的直接链接")
----------------------------------------------------------------------------------

*   👉[内置分流规则集](https://karing.app/tutorial/diversion)
*   👉[自定义分流规则、节点组](https://karing.app/tutorial/custom-diversion)
*   👉[应用入站代理(Android)](https://karing.app/tutorial/perapp-proxy)
*   👉[备份和多端同步配置](https://karing.app/tutorial/backup-sync)

最后、常见问题/FAQ[​](about:blank#%E6%9C%80%E5%90%8E%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98faq "最后、常见问题/FAQ的直接链接")
--------------------------------------------------------------------------------------------------------

*   我把karing装入U盘随身携带？ 👉[便携配置(Windows)](https://karing.app/tutorial/portable)
    
*   我是ISP(机场主)
    
    *   怎么在karing上集成我的套餐链接? 👉[ISP集成](https://karing.app/cooperation/menu)
    *   一键导入karing配置的快速链接怎么写? 👉[scheme格式](https://karing.app/cooperation/scheme)
*   其他问题请移步 [FAQ](https://karing.app/faq/)
    

[编辑此页](https://github.com/KaringX/karing-docu/tree/main/docs/quickstart/index.md)

  

本文转自 [https://karing.app/quickstart/](https://karing.app/quickstart/)，如有侵权，请联系删除。

















































































