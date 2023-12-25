# Get Cruise Route

## `getCruises() -> {Promise<any>}`

Get Cruise Route

### Parameters

| Name | Data Type | Description |
| ------------ | ------ | ------------------ |
| `businessId` | string | optional; Business Id |

### Return value `Promise.<any>`

| Name | Data Type | Description |
| --------- | ---- | -------- |
| `result` | any  | Cruise Information |

### Example

```javascript
...
const result = await axRobot.getCruises(cruiseInfo);
console.log(result.status)
console.log(result.data)
let cruise = result.data[0]
console.log(cruise.id)
console.log(cruise.name)
console.log(cruise.businessId)
console.log(cruise.sites)
...
```
