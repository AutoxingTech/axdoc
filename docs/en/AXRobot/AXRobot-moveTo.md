# Fixed-Point Motion

## `moveTo(pose) -> {void}`

The robot moves to the specified position

### Parameters

| Name | Data Type | Description |
| ------ | --------------------- | ---- |
| `pose` | [Pose](#/Define-Pose) | pose |

### Return Value

none

### Example

```javascript
...
axRobot.moveTo({
   x: 0,
   y: 0,
   yaw: 0
});
...
```
