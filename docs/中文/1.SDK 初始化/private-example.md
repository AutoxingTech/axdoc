# SDK 私有化初始化

SDK 初始化完成后才可以正常使用。以下为 SDK 私有化代码示例：

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// 创建 AXRobot 私有化实例
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
| `serverUrl` | string   |私有化服务地址|
| `websocketUrl` | string   | 可选 <br> 若只填写serverUrl，不填写websocketUrl，则websocketUrl会根据serverUrl自动生成websocket连接地址|

> * **说明:** 
> * **1:** 版本要求：使用sdk v1.0.74或以上
> * **2:** 若只填写serverUrl，不填写websocketUrl，则websocketUrl会根据serverUrl自动生成websocket连接地址
> * **例如:** “http://127.0.0.1:8080/” -> “ws://127.0.0.1:8080/”、“https://127.0.0.1:8080/” -> “wss://127.0.0.1:8080/”
> * **3:** 若是填写websocketUrl，则使用当前填写url
> * **4:** 若不知道如何获取私有化服务地址，请咨询相关运营人员

[示例](https://service.autoxing.com/sdk/v1.0/example/#/)

