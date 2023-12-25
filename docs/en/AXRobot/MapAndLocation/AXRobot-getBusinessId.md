# Get Robot Business ID

## `getBusinessId(mode) -> {Promise.<string>}`

Get business ID of the robot

### Parameters

| Name   | Type   | Description                     |
| ------ | ------ | ------------------------------- |
| `mode` | number | Optional; The mode of the robot |

### Return Value `Promise.<string>`

The business ID

### Example

```javascript
...
const businessId = await axRobot.getBusinessId();
...
```

