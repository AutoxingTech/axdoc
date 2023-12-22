# Back To Charge

## `goHome(pose) -> {Promise.<boolean>}`

Control the robot back to the charging pile

### Parameters

| Name | Data Type | Description |
| ------ | --------------------- | ---- |
| `pose` | [Pose](../../Define/Define-Pose) | pose |

### Return Value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
axRobot.goHome({
   x: 0,
   y: 0,
   yaw: 0
});
...
```
