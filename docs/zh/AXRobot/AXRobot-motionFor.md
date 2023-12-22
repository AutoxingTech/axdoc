# 单步运动

## `motionFor(type) -> {void}`

机器人运动控制

### 参数

| 名称   | 数据类型                          | 说明     |
| ------ | --------------------------------- | -------- |
| `type` | [MotionType](#/Define-MotionType) | 运动方式 |

### 返回值

无

### 示例

```typescript
...
axRobot.motionFor(MotionType.Forward);
...
```

