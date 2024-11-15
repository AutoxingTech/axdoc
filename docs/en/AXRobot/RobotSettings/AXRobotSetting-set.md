# Set Robot Custom Settings

## `axRobot.sendPyCommand('setCustomSettings', settingsData)`

### Parameters

| Name | Data Type | Description |
| ------ | --------------------------------- | -------- |
| `settingsData` | [SettingsData](../../../Define/Define-SettingsData) | robot settingsData |

### response `Promise.<boolean>`

Set Result

* `true` - 成功
* `fales` - 失败

### example

```typescript

const success = await axRobot.sendPyCommand('setCustomSettings', settingsData)
if (success) {
  // settings success
  ...
} else {
  // settings failed
  ...
}
```

