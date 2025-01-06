# Relocation

## `resetPose(mapPose, isChargingPose) -> {Promise.<boolean>}`

Reset the robot pose

### Parameters

| Name | Data Type | Description |
| --------- | --------------------------- | ---- |
| `mapPose` | [MapPose](../../../Define/Define-MapPose) | Pose |
| `isChargingPose` | boolean                     | optional; Whether it is the charging pile pose | **The default is the pose of the charging pile** <br> **`false`: the current pose of the robot, `true`: the pose of the charging pile** |

### Return value `Promise.<boolean>`

Whether the setting is successful

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await resetPose({
   areaId: "<areaId>",
   x: 0,
   y: 0,
   yaw: 0
}, false);
...
```
