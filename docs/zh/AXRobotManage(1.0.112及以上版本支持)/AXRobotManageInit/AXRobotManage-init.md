# 初始化

## `init() -> {Promise.<boolean>}`

初始化实例

### 返回值 `Promise.<boolean>`

初始化是否成功

* `true` - 成功
* `fales` - 失败

### 示例

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
  // 初始化成功
  ...
} else {
  // 初始化失败
  ...
}
```

