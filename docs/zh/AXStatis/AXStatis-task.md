# 任务统计

## `getTaskStatistics() -> {Promise<any>}`

任务统计

### 参数

| 名称         | 类型   | 说明               |
| ------------ | ------ | ------------------ |
| `taskStatistics` | [TaskStatistics](../../Define/Define-TaskStatistics) |  |

### 返回值 `Promise.<any>`

| 名称      | 类型 | 说明     |
| --------- | ---- | -------- |
| `result` | any  | 统计信息 |

### 示例

```typescript
...
const result = await axRobot.getTaskStatistics(taskStatistics);
console.log(result)
...
```
