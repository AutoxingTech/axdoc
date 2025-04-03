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
const success = await axRobot.init();
if (success) {
  // success
  ...
} else {
  // failed
  ...
}
```

