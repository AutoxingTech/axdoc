# Delete Cruise Route

## `deleteCruise(ids) -> {Promise<boolean>}`

Delete Cruise Route

### Parameters

| Name  | Data Type | Description |
| ----- | --------- | ----------- |
| `ids` | number[]  | Ids         |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
const success = await axRobot.deleteCruise(ids);
...
```
