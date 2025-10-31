# 单任务统计

## `getSingleTaskStatistics() -> {Promise<any>}`

单任务统计

### 参数

| 名称         | 类型   | 说明               |
| ------------ | ------ | ------------------ |
| `singleTaskStatistics` | [SingleTaskStatistics](../../Define/Define-SingleTaskStatistics) |  |

### 返回值 `Promise.<any>`

| 名称      | 类型 | 说明     |
| --------- | ---- | -------- |
| `result` | any  | 统计信息 |

### 示例

```typescript
...
const result = await axRobot.getSingleTaskStatistics(singleTaskStatistics);
console.log(result)
...
```