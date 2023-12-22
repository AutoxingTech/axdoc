# 设置服务器信息

## `setServerInfos(serverInfo) -> {Promise.<boolean>}`

设置机器人连接的服务信息

### 参数

| 名称         | 类型                              | 说明       |
| ------------ | --------------------------------- | ---------- |
| `serverInfo` | [ServerInfo](../../Define/Define-ServerInfo) | 服务器信息 |

### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败

### 示例

```typescript
...
let serverInfo = {
    ip: "http://127.0.0.1:8080/",
    type: -1,
    offline: 0
}
const success = await axRobot.setServerInfos(serverInfo);
...
```
