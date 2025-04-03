# Synchronize cloud cruise routes

## `syncCruiseCloud(businessId) -> {Promise<boolean>}`

Synchronize cloud cruise routes

### Parameters

| Name         | Data Type | Description |
| ------------ | --------- | ----------- |
| `businessId` | string    | Business Id |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
const success = await axRobot.syncCruiseCloud(businessId);
...
```
