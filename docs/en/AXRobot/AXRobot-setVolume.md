# Set Volume

## `setVolume(volume, mode) -> {Promise.<boolean>}`

Set the robot volume

### Parameters

| Name | Data Type | Description |
| -------- | -------- | -------------------------------------- |
| `volume` | number | volume, value range 0~100 |
| `mode` | number | Execution mode<br/>1 - Host computer<br/>2 - Chassis |

### Return value `Promise.<boolean>`

Whether the setting is successful

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.setVolume(50, 1);
...
```
