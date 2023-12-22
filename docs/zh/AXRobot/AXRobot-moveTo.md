# 定点移动

## `moveTo(pose) -> {void}`

机器人移动到指定位置

### 参数

| 名称   | 数据类型              | 说明 |
| ------ | --------------------- | ---- |
| `pose` | [Pose](#/Define-Pose) | 位姿 |

### 返回值

无

### 示例

```typescript
...
axRobot.moveTo({
  x: 0,
  y: 0,
  yaw: 0
});
...
```

