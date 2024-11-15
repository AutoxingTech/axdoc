# Set Robot Custom Settings

## `axRobot.sendPyCommand('setCustomSettings', settingsData)`

### Parameters

| Name | Data Type | Description |
| ------ | --------------------------------- | -------- |
| `settingsData` | [SettingsData](../../../Define/Define-SettingsData) | robot settingsData |

### response `Promise.<boolean>`

Set Result

* `true` - success
* `fales` - failed

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

