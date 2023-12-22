# Statistics Total

## `getStatisticsTotal() -> {Promise<any>}`

Statistics Total

### 参数

| Name | Data Type | Description |
| ------------ | ------ | ------------------ |
| `statisticsTotal` | [StatisticsTotal](#/Define-StatisticsTotal) |  |

### Return value `Promise.<any>`

| Name | Data Type | Description |
| --------- | ---- | -------- |
| `result` | any  | Statistics Information |

### Example

```javascript
...
const result = await axRobot.getStatisticsTotal(statisticsTotal);
console.log(result)
...
```