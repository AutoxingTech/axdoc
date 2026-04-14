````markdown
# Inherits from AXRobot
AXRobotManage inherits from AXRobot, all methods from AXRobot are available after AXRobotManage is instantiated.

# Business Channel (Multi-Robot) vs Single Robot Channel
Business channel and single robot channel are two different channels that do not affect each other;  
If you want to connect to another robot through the single robot channel, you must first destroy the previous single robot connection;  
To switch business, you must first destroy the previous business connection.

# Development Guide
Subscribe to business: Monitor real-time status of multiple robots, generally used for multi-robot status monitoring; but if you want to control robots or issue commands/tasks, you still need to connect through the single robot channel.

# AXRobotManage Constructor

## `AXRobotManage({appId: "", secret: "", mode: "mode", serverUrl: '', wsUrl: '', viewLanguage: ''})`

Constructor

### Parameters

| Name     | Data Type | Description     |
| -------- | -------- | -------- |
| `appId` | string   | Application ID, can be obtained from relevant operations personnel |
| `appSecret` | string   | Data request secret key, can be obtained from relevant operations personnel |
| [`AppMode`](../../Define/Define-AppMode.md) | string   | Application mode |
| `serverUrl` | string   | Optional <br> If not provided, the service defaults to domestic endpoint<br> serverUrl: <br>Domestic endpoint:"https://api.autoxing.com/"<br>Overseas endpoint:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | Optional <br> If not provided, the service defaults to domestic endpoint<br>websocketUrl:<br>Domestic endpoint:"wss://service.autoxing.com/"<br>Overseas endpoint:"wss://serviceglobal.autoxing.com/" |
| `viewLanguage` | string   | Default language for exception returns (currently supports Chinese and English, default is English -- zh prefix: Chinese, others: English)|



### Return Value

None

### Example

???+ example 

    === "Domestic Endpoint"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // Create AXRobotManage initialization
            const axRobot = new AXRobotManage({
                appId:appId, // Get appid from robot management platform based on permissions
                secret: appSecret, // Get appSecret from robot management platform based on permissions
                mode: AppMode.WAN_APP, // Application mode: AppMode is exported in the package, can be imported directly
                serverUrl: serverUrl, // Private serverUrl 
                wsUrl: wsUrl, // Private wsUrl
                viewLanguage: getApp().globalData.language, // Language, optional
            });
           

        ```

    === "Overseas Endpoint"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // Create AXRobotManage private instance
            const axRobot = new AXRobotManage(
              {
                appId:appId, // Get appid from robot management platform based on permissions
                secret: appSecret, // Get appSecret from robot management platform based on permissions
                mode: AppMode.WAN_APP, // Application mode: AppMode is exported in the package, can be imported directly
                serverUrl: serverUrl, // serverUrl 
                wsUrl: wsUrl, // wsUrl
                viewLanguage: getApp().globalData.language, // Language, optional
              }
            );

        ```
````
