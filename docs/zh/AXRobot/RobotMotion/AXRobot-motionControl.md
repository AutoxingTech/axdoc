# 双步运动

## `motionControl(linearVelocity, angularVelocity) -> {void}`

控制机器人移动

### 参数

| 名称              | 数据类型 | 说明       |
| ----------------- | -------- | ---------- |
| `linearVelocity`  | number   | 移动线速度 |
| `angularVelocity` | number   | 移动角速度 |

### 返回值

无

### 示例

```typescript
...
axRobot.motionControl(0.1, 0.2);
...
```

