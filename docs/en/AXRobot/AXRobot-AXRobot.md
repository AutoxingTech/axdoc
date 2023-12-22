# AXRobot Constructor

## `AXRobot("<appId>", "<appSecret>", "<AppMode>", "<serverUrl>", "<websocketUrl>")`

Constructor

### Parameters

| Name     | Type | Description     |
| -------- | -------- | -------- |
| `appId` | string   | appId |
| `appSecret` | string   | appSecret |
| [`AppMode`](../../Define/Define-AppMode) | string   | Application mode |
| `serverUrl` | string   | serverUrl: <br>Mainland access point:"https://api.autoxing.com/"<br>Overseas access point:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | websocketUrl:<br>Mainland access point:"wss://service.autoxing.com/"<br>Overseas access point:"wss://serviceglobal.autoxing.com/" |




### Return Value

无

### Example

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// Create a private instance of AXRobot
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP, "<serverUrl>", "<websocketUrl>");

```

