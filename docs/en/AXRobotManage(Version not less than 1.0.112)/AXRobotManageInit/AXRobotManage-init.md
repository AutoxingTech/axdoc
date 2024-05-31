# Initialization

## `init() -> {Promise.<boolean>}`

Initialize Instance

### Return Value `Promise.<boolean>`

  success

  * `true` - success
  * `false` - failed

### Example

```typescript
import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

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
const success = await axRobot.init();
if (success) {
  // success
  ...
} else {
  // failed
  ...
}
```

