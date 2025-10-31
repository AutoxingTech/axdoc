# 总统计数据

## `getStatisticsTotal() -> {Promise<any>}`

总统计数据

### 参数

| 名称         | 类型   | 说明               |
| ------------ | ------ | ------------------ |
| `statisticsTotal` | [StatisticsTotal](../../Define/Define-StatisticsTotal) |  |

### 返回值 `Promise.<any>`

| 名称      | 类型 | 说明     |
| --------- | ---- | -------- |
| `result` | any  | 统计信息 |

### 示例

```typescript
...
const result = await axRobot.getStatisticsTotal(statisticsTotal);
console.log(result)
...
```