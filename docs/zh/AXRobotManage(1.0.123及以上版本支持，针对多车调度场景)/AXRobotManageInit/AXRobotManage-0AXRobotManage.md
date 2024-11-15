# 继承之前AXRobot
AXRobotManage继承之前AXRobot，之前AXRobot方法在AXRobotManage实例化后同样适用。

#  AXRobotManage 构造函数

## `AXRobotManage({tokenData: {}, appId: "", secret: "", mode:  "mode", serverUrl: '', wsUrl: ''， viewLanguage： ''})`

构造函数

### 参数

| 参数        | 对应        | 数据类型 | 说明     |
| ----------- | ---------- | -------- | -------- |
| `tokenData` | `tokenData`| any      |  用户登录token，可不传，不传时默认appId授权 |
| `appId`     | `appId`    | string   | 机器人管理平台根据权限获取 |
| `secret`    | `appSecret`| string   |机器人管理平台根据权限获取 |
| `mode`      | [`AppMode`](../../../Define/Define-AppMode) | string   | 应用模式:AppMode已在包内export，可直接引入 |
| `serverUrl` | `serverUrl` | string   | 私有化地址，不传时默认autoxing指定地址 |
| `wsUrl` | `websocketUrl` | string   | 私有化地址，不传时默认autoxing指定地址 |
| `viewLanguage` | `viewLanguage` | string   | 异常返回的默认语言（目前支持中英文，默认英文 -- zh开头：中文 其它：英文）|



### 返回值

无

### 示例

???+ example 

    === "大陆接入点"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobotManage 私有化实例
            const axRobot = new AXRobotManage(
                new AXRobot({
						tokenData: {
                            "token": "...", // 登录token
                            "tokenTime": tokenTime, // 登录时间
                            "tokenKey": "...", // 登录token的key
                            "expireTime": expireTime // token 过期时间
                        },
						appId:appId, // 机器人管理平台根据权限获取appid
						secret: appSecret, // 机器人管理平台根据权限获取appSecret
						mode: AppMode.WAN_APP, // 应用模式:AppMode已在包内export，可直接引入
						serverUrl: serverUrl, // 私有化serverUrl 
						wsUrl: wsUrl, // 私有化wsUrl
						viewLanguage: getApp().globalData.language, // 语言 可不传
					})
            );
           

        ```

    === "海外接入"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobotManage 私有化实例
            const axRobot = new AXRobotManage(
                new AXRobot({
						tokenData: {
                            "token": "...", // 登录token
                            "tokenTime": tokenTime, // 登录时间
                            "tokenKey": "...", // 登录token的key
                            "expireTime": expireTime // token 过期时间
                        },
						appId:appId, // 机器人管理平台根据权限获取appid
						secret: appSecret, // 机器人管理平台根据权限获取appSecret
						mode: AppMode.WAN_APP, // 应用模式:AppMode已在包内export，可直接引入
						serverUrl: serverUrl, // 私有化serverUrl 
						wsUrl: wsUrl, // 私有化wsUrl
						viewLanguage: getApp().globalData.language, // 语言 可不传
					})
            );

        ```