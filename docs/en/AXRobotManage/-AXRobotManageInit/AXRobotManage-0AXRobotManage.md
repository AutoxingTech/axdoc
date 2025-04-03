# extends AXRobot before
AXRobotManage inherits the previous AXRobot, and the previous AXRobot method is also applicable after AXRobotManage is instantiated.

#  AXRobotManage Constructor

## `AXRobotManage({tokenData: {}, appId: "", secret: "", mode:  "mode", serverUrl: '', wsUrl: ''， viewLanguage： ''})`


Constructor

### Parameters

| Fields        | Relative        | Type | Description     |
| ----------- | ---------- | -------- | -------- |
| `tokenData`    | `tokenData`   | any   |  User id |
| `appId`     | `appId`    | string   | appId |
| `secret`    | `appSecret`| string   |appSecret |
| `mode`      | [`AppMode`](../../../Define/Define-AppMode) | string   | Application mode |
| `serverUrl` | `serverUrl` | string   |  private serverUrl   |
| `wsUrl` | `websocketUrl` | string   | private wsUrl |
| `viewLanguage` | `viewLanguage` | string   | Default language for exception return (currently supports both Chinese and English, default English - starting with zh: Chinese Other: English)|

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
                    tokenData: {
                        "token": "...", // token
                        "tokenTime": tokenTime, // login time
                        "tokenKey": "...", // login key
                        "expireTime": expireTime // expireTime
                    },
                    appId:appId, // appid
                    secret: appSecret, // appSecret
                    mode: AppMode.WAN_APP, 
                    serverUrl: serverUrl, // private serverUrl 
                    wsUrl: wsUrl, // private wsUrl
                    viewLanguage: getApp().globalData.language, // viewLanguage
                }
            );
           

        ```

    === "Overseas access"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // Create a private instance of AXRobotManage
            const axRobot = new AXRobotManage(
                {
                    tokenData: {
                        "token": "...", // token
                        "tokenTime": tokenTime, // login time
                        "tokenKey": "...", // login key
                        "expireTime": expireTime // expireTime
                    },
                    appId:appId, // appid
                    secret: appSecret, // appSecret
                    mode: AppMode.WAN_APP, 
                    serverUrl: serverUrl, // private serverUrl 
                    wsUrl: wsUrl, // private wsUrl
                    viewLanguage: getApp().globalData.language, // viewLanguage
                }
            );

        ```