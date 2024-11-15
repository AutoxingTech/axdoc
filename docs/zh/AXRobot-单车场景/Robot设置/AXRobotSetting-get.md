# 获取机器人设置数据

## `getRobotCustomSettings(robotId, {}, {onRobotSettingsStateChanged})`

获取

### 返回值

| Name | Data Type | Description |
| ------ | --------------------------------- | -------- |
| `settingsData` | [SettingsData](../../../Define/Define-SettingsData) | motion type |

### 示例

```typescript
axRobot.getRobotCustomSettings(robotId, {}, {
        onRobotSettingsStateChanged:function(obj) {
          // obj：机器人设置数据
          console.log('robotSettingsData', obj)
        }
      }
```

