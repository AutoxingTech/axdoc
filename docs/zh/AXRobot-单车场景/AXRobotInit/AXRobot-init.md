# 初始化

## `init() -> {Promise.<boolean>}`

初始化实例

### 返回值 `Promise.<boolean>`

初始化是否成功

* `true` - 成功
* `fales` - 失败

### 示例

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP);
const successed = await axRobot.init();
if (successed) {
  // 初始化成功
  ...
} else {
  // 初始化失败
  ...
}
```

