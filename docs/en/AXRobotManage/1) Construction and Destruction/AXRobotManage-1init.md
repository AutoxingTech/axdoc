````markdown
# Initialization

## `init() -> {Promise.<boolean>}`

Initialize instance

### Return Value `Promise.<boolean>`

Whether initialization was successful

* `true` - Success
* `false` - Failure

### Example

```typescript
import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

const axRobot = new AXRobotManage(
  {
    appId:appId, // Get appid from robot management platform based on permissions
    secret: appSecret, // Get appSecret from robot management platform based on permissions
    mode: AppMode.WAN_APP, // Application mode: AppMode is exported in the package, can be imported directly
    serverUrl: serverUrl, // Private serverUrl 
    wsUrl: wsUrl, // Private wsUrl
    viewLanguage: getApp().globalData.language, // Language, optional
  }
);
const success = await axRobot.init();
if (success) {
  // Initialization successful
  ...
} else {
  // Initialization failed
  ...
}
```


````
