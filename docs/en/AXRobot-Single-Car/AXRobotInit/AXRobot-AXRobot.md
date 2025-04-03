# AXRobot Constructor

## `AXRobot("<appId>", "<appSecret>", "<AppMode>", "<serverUrl>", "<websocketUrl>")`

Constructor

### Parameters

| Name     | Type | Description     |
| -------- | -------- | -------- |
| `appId` | string   | appId |
| `appSecret` | string   | appSecret |
| [`AppMode`](../../../Define/Define-AppMode) | string   | Application mode |
| `serverUrl` | string   | serverUrl: <br>Mainland access point:"https://api.autoxing.com/"<br>Overseas access point:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | websocketUrl:<br>Mainland access point:"wss://service.autoxing.com/"<br>Overseas access point:"wss://serviceglobal.autoxing.com/" |

???+ warning "warning"
    Please select the relevant access point for your business


### Return Value

无

### Example
???+ Example "Example"

    === "Mainland access point"

        ```typescript
            import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

            const axRobot = new AXRobot(
                "<appId>", 
                "<appSecret>",
                AppMode.WAN_APP, 
                "https://api.autoxing.com/", 
                "wss://service.autoxing.com/"
            );

        ```

    === "Overseas access point"

        ```typescript
            import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

            const axRobot = new AXRobot(
                "<appId>", 
                "<appSecret>", 
                AppMode.WAN_APP, 
                "https://apiglobal.autoxing.com/", 
                "wss://serviceglobal.autoxing.com/"
            );

        ```
