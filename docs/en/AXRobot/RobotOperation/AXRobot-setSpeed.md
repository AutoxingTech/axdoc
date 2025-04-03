# Set Speed

## `setSpeed(speed) -> {Promise.<boolean>}`

Set the robot movement speed

### Parameters

| Name | Data Type | Description |
| ------- | -------- | --------------------- |
| `speed` | number | Movement speed, unit: m/s |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.setSpeed(0.5);
...
```
