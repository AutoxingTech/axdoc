# 获取机器人所属业务标识

## `getBusinessId(mode) -> {Promise.<string>}`

获取机器人所属业务标识

### 参数

| 名称   | 类型   | 说明             |
| ------ | ------ | ---------------- |
| `mode` | number | 可选；机器人模式 |

### 返回值 `Promise.<string>`

业务标识

### 示例

```typescript
...
const businessId = await axRobot.getBusinessId();
...
```

