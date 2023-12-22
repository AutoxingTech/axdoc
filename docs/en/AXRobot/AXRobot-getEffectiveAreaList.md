# Get Effective Area List

## `getEffectiveAreaList() -> {Promise.<any>}`

Get effective area list

### Parameters

None

### Return Value `Promise.<any>`

| Field Name                   | Type   | Description                                                                                            |
| ---------------------------- | ------ | ------------------------------------------------------------------------------------------------------ |
| `status`                     | number | Response status code<br />200 - Success<br />400 - Failed parameters<br />500 - Service internal error |
| `message`                    | string | Response status description                                                                            |
| `data`                       | object | Response data                                                                                          |
| `data.effective`             | array  | The list of effective areas - actual floor                                                             |
| `data.ineffective`           | array  | The list of ineffective areas - actual floor                                                           |
| `data.effectiveFloorNames`   | array  | The list of effective area - show floor                                                                |
| `data.ineffectiveFloorNames` | array  | The list of ineffective areas - show floor                                                             |

```json
{
  "status": 200,
  "message": "ok",
  "data": {
    "effective": [-1, 1, 3],
    "ineffective": [-2, 2, 5, 6, 7],
    "effectiveName": [-1, 1, 3],
    "ineffectiveName": [-2, 2, 5, 6, 7]
  }
}
```

### Example

```javascript
...
const result = await getEffectiveAreaList();
// todo someting
...
```
