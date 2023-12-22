# Task Statistics

## `getTaskStatistics() -> {Promise<any>}`

Task Statistics

### Parameters

| Name | Data Type | Description |
| ------------ | ------ | ------------------ |
| `taskStatistics` | [TaskStatistics](#/Define-TaskStatistics) |  |

### Return value `Promise.<any>`

| Name | Data Type | Description |
| --------- | ---- | -------- |
| `result` | any  | Statistics Information |

### Example

```javascript
...
const result = await axRobot.getTaskStatistics(taskStatistics);
console.log(result)
...
```
