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
    appId:appId, // 机器人管理平台根据权限获取appid
    secret: appSecret, // 机器人管理平台根据权限获取appSecret
    mode: AppMode.WAN_APP, // 应用模式:AppMode已在包内export，可直接引入
    serverUrl: serverUrl, // 私有化serverUrl 
    wsUrl: wsUrl, // 私有化wsUrl
    viewLanguage: getApp().globalData.language, // 语言 可不传
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

