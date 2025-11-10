# 设置急停

## `setEmergency(type) -> {void}`

设置机器人进入急停状态
### 参数

| 名称   | 数据类型                                | 说明     |
| ------ | --------------------------------------- | -------- |
| `type` | [EmergencyType](../../8.数据定义/Define-EmergencyType) | 急停方法 |

### 返回值

无

### 示例

```typescript
...
axRobot.setEmergency(EmergencyType.Start); // 进入急停状态
...
axRobot.setEmergency(EmergencyType.Stop); // 结束急停状态
...
```

