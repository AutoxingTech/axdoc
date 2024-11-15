# 设置音量

## `setVolume(volume, mode) -> {Promise.<boolean>}`

设置机器人音量

### 参数

| 名称     | 数据类型 | 说明                                   |
| -------- | -------- | -------------------------------------- |
| `volume` | number   | 音量，取值范围 0~100                   |
| `mode`   | number   | 执行端模式<br/>1 - 上位机<br/>2 - 底盘 |

### 返回值 `Promise.<boolean>`

设置是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
const success = await axRobot.setVolume(50, 1);
...
```

