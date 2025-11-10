# 构造函数

## `AXRobot("<appId>", "<appSecret>", "<AppMode>", "<serverUrl>", "<websocketUrl>")`

构造函数

### 参数

| 名称     | 数据类型 | 说明     |
| -------- | -------- | -------- |
| `appId` | string   | appId |
| `appSecret` | string   | appSecret |
| [`AppMode`](../../8.数据定义/Define-AppMode) | string   | 应用模式 |
| `serverUrl` | string   | serverUrl: <br>国服接入点:"https://api.autoxing.com/"<br>海外接入点:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | websocketUrl:<br>国服接入点:"wss://service.autoxing.com/"<br>海外接入点:"wss://serviceglobal.autoxing.com/" |

???+ warning "warning"
    请选择和业务相关的接入点


### 返回值

无

### 示例

???+ example 

    === "国服接入点"

        ```typescript
            import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobot 初始化实例
            const axRobot = new AXRobot(
                "<appId>", 
                "<appSecret>",
                AppMode.WAN_APP, 
                "https://api.autoxing.com/", 
                "wss://service.autoxing.com/"
            );

        ```

    === "海外接入"

        ```typescript
            import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobot 初始化实例
            const axRobot = new AXRobot(
                "<appId>", 
                "<appSecret>", 
                AppMode.WAN_APP, 
                "https://apiglobal.autoxing.com/", 
                "wss://serviceglobal.autoxing.com/"
            );

        ```