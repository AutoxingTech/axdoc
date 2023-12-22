# Setting/Update Cruise Route

## `saveCruise(cruiseInfo) -> {Promise<boolean>}`

Setting/Update Cruise Route

### Parameters

| Name         | Data Type                         | Description  |
| ------------ | --------------------------------- | ------------ |
| `cruiseInfo` | [CruiseInfo](../../Define/Define-CruiseInfo) | Cruise Route Information |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
let cruiseInfo = {
    id: 12,
    name: "test-cruise",
    businessId: "",
    sites: [{
        poiId: "6423afdb1162805312f27a75",
        poiName: "test-poi"
    }],
    remark: ""
}
const success = await axRobot.saveCruise(cruiseInfo);
...
```
