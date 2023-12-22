# AXRobot 构造函数

## `AXRobot("<appId>", "<appSecret>", "<AppMode>", "<serverUrl>", "<websocketUrl>")`

构造函数

### 参数

| 名称     | 数据类型 | 说明     |
| -------- | -------- | -------- |
| `appId` | string   | appId |
| `appSecret` | string   | appSecret |
| [`AppMode`](../../Define/Define-AppMode) | string   | 应用模式 |
| `serverUrl` | string   | serverUrl: <br>大陆接入点:"https://api.autoxing.com/"<br>海外接入点:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | websocketUrl:<br>大陆接入点:"wss://service.autoxing.com/"<br>海外接入点:"wss://serviceglobal.autoxing.com/" |




### 返回值

无

### 示例

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// 创建 AXRobot 私有化实例
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP, "<serverUrl>", "<websocketUrl>");

```

