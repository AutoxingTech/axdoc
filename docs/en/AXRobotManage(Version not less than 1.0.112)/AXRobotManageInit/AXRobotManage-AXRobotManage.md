# extends AXRobot before
AXRobotManage inherits the previous AXRobot, and the previous AXRobot method is also applicable after AXRobotManage is instantiated.

#  AXRobotManage Constructor

## `AXRobotManage({openId: '', appId: "", secret: "", mode:  "mode", serverUrl: '', wsUrl: ''})`

Constructor

### Parameters

| Fields        | Relative        | Type | Description     |
| ----------- | ---------- | -------- | -------- |
| `openId`    | `openId`   | string   |  User id |
| `appId`     | `appId`    | string   | appId |
| `secret`    | `appSecret`| string   |appSecret |
| `mode`      | [`AppMode`](../../../Define/Define-AppMode) | string   | Application mode |
| `serverUrl` | `serverUrl` | string   | serverUrl: <br>Mainland access point:"https://api.autoxing.com/"<br>Overseas access point:"https://apiglobal.autoxing.com/"<br> |
| `wsUrl` | `websocketUrl` | string   | websocketUrl:<br>Mainland access point:"wss://service.autoxing.com/"<br>Overseas access point:"wss://serviceglobal.autoxing.com/" |


### Return Value

None

### Example

???+ Example 

    === "Mainland access"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // Create a private instance of AXRobotManage
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

    === "Overseas access"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // Create a private instance of AXRobotManage
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