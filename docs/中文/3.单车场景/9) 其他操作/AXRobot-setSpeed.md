# 设置速度

## `setSpeed(speed) -> {Promise.<boolean>}`

设置机器人移动速度

### 参数

| 名称    | 数据类型 | 说明                  |
| ------- | -------- | --------------------- |
| `speed` | number   | 移动速度，单位：米/秒 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
const success = await axRobot.setSpeed(0.5);
...
```

