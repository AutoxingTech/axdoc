# 继承之前AXRobot
AXRobotManage继承之前AXRobot，之前AXRobot方法在AXRobotManage实例化后同样适用。

#  AXRobotManage 构造函数

## `AXRobotManage({openId: '', appId: "", secret: "", mode:  "mode", serverUrl: '', wsUrl: ''})`

构造函数

### 参数

| 参数        | 对应        | 数据类型 | 说明     |
| ----------- | ---------- | -------- | -------- |
| `openId`    | `openId`   | string   |  用户标识 |
| `appId`     | `appId`    | string   | 机器人管理平台根据权限获取 |
| `secret`    | `appSecret`| string   |机器人管理平台根据权限获取 |
| `mode`      | [`AppMode`](../../../Define/Define-AppMode) | string   | 应用模式:AppMode已在包内export，可直接引入 |
| `serverUrl` | `serverUrl` | string   | serverUrl: <br>大陆接入点:"https://api.autoxing.com/"<br>海外接入点:"https://apiglobal.autoxing.com/"<br> |
| `wsUrl` | `websocketUrl` | string   | websocketUrl:<br>大陆接入点:"wss://service.autoxing.com/"<br>海外接入点:"wss://serviceglobal.autoxing.com/" |


### 返回值

无

### 示例

???+ example 

    === "大陆接入点"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobotManage 私有化实例
            const axRobot = new AXRobotManage(
                {
                    openId: "<openId>",
                    appId: "<appId>",
                    secret: "<appSecret>",
                    mode:  AppMode.WAN_APP,
                    serverUrl: "https://api.autoxing.com/",
                    wsUrl: "wss://service.autoxing.com/"
                }
            );
           

        ```

    === "海外接入"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobotManage 私有化实例
            const axRobot = new AXRobotManage(
                {
                    openId: "<openId>",
                    appId: "<appId>",
                    secret: "<appSecret>",
                    mode:  AppMode.WAN_APP,
                    serverUrl: "https://apiglobal.autoxing.com/",
                    wsUrl: "wss://serviceglobal.autoxing.com/"
                }
            );

        ```