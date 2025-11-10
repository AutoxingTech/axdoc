# 回桩充电

## `goHome(pose) -> {Promise.<boolean>}`

控制机器人回充电桩

### 参数

| 名称   | 数据类型              | 说明 |
| ------ | --------------------- | ---- |
| `pose` | [Pose](../../8.数据定义/Define-Pose) | 位姿 |

	### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
axRobot.goHome({
  x: 0,
  y: 0,
  yaw: 0
});
...
```

