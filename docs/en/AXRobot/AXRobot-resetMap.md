# Reset Map

## `resetMap(areaId) -> {Promise.<boolean>}`

Reset the robot map area

### Parameters

| Name | Data Type | Description |
| -------- | -------- | ------------ |
| `areaId` | string | Map area ID |

### Return value `Promise.<boolean>`

Whether the setting is successful

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.resetMap("<areaId>");
...
```
