# Subscribe To Robot Status

## `subscribeRealState(listener) -> {void}`

Subscribe to bot real-time status

### Parameters

| Name | Data Type | Description |
| ---------- | ------------------------------------------ | ---------------------- |
| `listener` | [OnRobotListner](../../../Define/Define-OnRobotListener) | Robot real-time status subscription callback |

### Return Value

none

### Example

```javascript
...
axRobot.subscribeRealState({
  onStateChanged: state => {
    console.log(state.isManualMode); // whether to push the mode
    console.log(state.isTasking); // Whether the task is being executed
    console.log(state.isCharging); // is charging
    console.log(state.isRemoteMode); // Whether remote control
    console.log(state.battery); // current battery (percentage)
    console.log(state.robotId); // Robot ID
    console.log(state.speed); // current speed (m/s)
    console.log(state.areaId); // current area ID
    console.log(state.isEmergencyStop); // Whether emergency stop state
    console.log(state.x); // x component of position coordinates
    console.log(state.y); // y component of position coordinates
    console.log(state.yaw); // current angle (radians)
    console.log(state.locQuality); // Current positioning quality (0-100)
    console.log(state.hasObstruction); // Is there an obstacle currently
    console.log(state.errors); // fault code
    console.log(state.isGoHome); // Whether it is returning to the pile for charging
    console.log(state.timestamp); // timestamp of robot state

    // do something
  }
});
...
```
