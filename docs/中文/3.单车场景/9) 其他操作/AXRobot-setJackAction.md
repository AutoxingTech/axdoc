# 设置顶升动作

## `setJackAction(type) -> {Promise.<boolean>}`

设置顶升机器人顶起落下的动作

### 参数

| 名称       | 类型     | 说明               |
| ---------- |--------|------------------|
| `type`     | number | 动作类型 0: 顶起 1: 落下 |

### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败

### 示例

```typescript
...
const success = await axRobot.setJackAction(0);
...
```
