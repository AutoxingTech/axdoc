# 设置机器人设置数据

## `axRobot.sendPyCommand('setCustomSettings', settingsData)`

### Parameters

| Name | Data Type | Description |
| ------ | --------------------------------- | -------- |
| `settingsData` | [SettingsData](../../8.数据定义/Define-SettingsData) | 机器人设置数据 |

### 返回值 `Promise.<boolean>`

设置是否成功

* `true` - 成功
* `fales` - 失败

### 示例

```typescript

const success = await axRobot.sendPyCommand('setCustomSettings', settingsData)
if (success) {
  // 设置成功
  ...
} else {
  // 设置失败
  ...
}
```

