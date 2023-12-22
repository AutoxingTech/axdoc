# SDK 初始化示例

SDK 初始化完成后才可以正常使用。以下为 SDK 初始化代码示例：

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// 创建 AXRobot 实例
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP);

// 初始化 AXRobot 实例
const successed = await axRobot.init();
if (successed) {
  try {
    // 连接指定机器人
    const res = await axRobot.connectRobot({
      robotId: "<robotId>"
    });
    console.log("connect success: " + res.robotId);
    // do something with robot
  } catch(err) {
    console.log(err.errText)
  }
} else {
  // 初始化失败
}
```

> * **appId** - 应用 ID，可向相关运营人员申请提供
> * **appSecret** - 数据请求密钥，可向相关运营人员申请提供
> * **AppMode** - [AppMode](../Define/Define-AppMode)

[示例](https://service.autoxing.com/sdk/v1.0/example/#/)

