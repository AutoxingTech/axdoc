# 设置wifi

## `setWifi(ssId, password) -> {Promise.<boolean>}`

设置机器人底盘wifi

### 参数

| 名称       | 类型   | 说明    |
| ---------- | ------ | ------- |
| `ssId`     | string | wifi 名 |
| `password` | string | 密码    |

### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败

### 示例

```typescript
...
const success = await axRobot.setWifi("test-wifi", "123456");
...
```
