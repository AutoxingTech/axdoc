# Single Task Statistics

## `getSingleTaskStatistics() -> {Promise<any>}`

Single Task Statistics

### Parameters

| Name | Type | Description |
| ------------ | ------ | ------------------ |
| `singleTaskStatistics` | [SingleTaskStatistics](../../Define/Define-SingleTaskStatistics) |  |

### Return value `Promise.<any>`

| Name | Data Type | Description |
| --------- | ---- | -------- |
| `result` | any  | Statistics Information |

### Example

```javascript
...
const result = await axRobot.getSingleTaskStatistics(singleTaskStatistics);
console.log(result)
...
```