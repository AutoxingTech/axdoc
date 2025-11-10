# SDK 基本初始化

如果想使用Autoxing 机器人 SDK，需先初始化，SDK 初始化完成后才可以正常使用。  
  

以下为 SDK 初始化代码示例：

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// 创建 AXRobot 实例
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP, "<serverUrl>", "<websocketUrl>");

// 初始化 AXRobot 实例
const successed = await axRobot.init();
if (successed) {
  // 初始化成功
} else {
  // 初始化失败
}
```


### 参数解析

| 名称     | 数据类型 | 说明     |
| -------- | -------- | -------- |
| `appId` | string   | 应用 ID，可向相关运营人员申请提供 |
| `appSecret` | string   | 数据请求密钥，可向相关运营人员申请提供 |
| [`AppMode`](../8.数据定义/Define-AppMode.md) | string   | 应用模式 |
| `serverUrl` | string   |可选 <br> 如果不填，服务默认使用国服接入点<br> serverUrl: <br>国服接入点:"https://api.autoxing.com/"<br>海外接入点:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | 可选 <br> 如果不填，服务默认使用国服接入点<br>websocketUrl:<br>国服接入点:"wss://service.autoxing.com/"<br>海外接入点:"wss://serviceglobal.autoxing.com/" |

[示例](https://service.autoxing.com/sdk/v1.0/example/#/)

