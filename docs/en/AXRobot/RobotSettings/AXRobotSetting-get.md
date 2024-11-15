# Get robot custom settings

## `getRobotCustomSettings(robotId, {}, {onRobotSettingsStateChanged})`

Get robot custom settings

### response

| Name | Data Type | Description |
| ------ | --------------------------------- | -------- |
| `settingsData` | [SettingsData](../../../Define/Define-SettingsData) | motion type |

### example

```typescript
axRobot.getRobotCustomSettings(robotId, {}, {
        onRobotSettingsStateChanged:function(obj) {
          // obj：robot custom settings
          console.log('robotSettingsData', obj)
        }
      }
```

