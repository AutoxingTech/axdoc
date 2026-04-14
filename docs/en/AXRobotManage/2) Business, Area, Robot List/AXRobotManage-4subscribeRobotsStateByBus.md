````markdown
# Subscribe to All Robot Status Under Business and Map

## Method

## `subscribeRobotsStateByBus(listener) -> {void}`
Note: To subscribe to business, you need to connect to the business first, refer to [Connect Business](./AXRobotManage-4connctBusiness.md)

Subscribe to real-time status of all robots under business and map. If robot status changes, it will return the real-time status of each robot individually.

### Parameters

| Name               | Type                                                        | Description     |
| ------------------ | ------------------------------------------------ | -------- |
| `listener`         | Object |  Robot real-time status subscription callback |


### Request Example

```javascript
...
await axRobot.subscribeRobotsStateByBus({
	onRobotListStatusChanged: state => {
		// Common
    console.log(state.isManualMode); // Whether in push mode
    console.log(state.isTasking); // Whether executing task
    console.log(state.isCharging); // Whether charging
    console.log(state.isRemoteMode); // Whether in remote control
    console.log(state.battery); // Current battery level (percentage)
    console.log(state.robotId); // Robot identifier
    console.log(state.isFrontBumperPressed); // Front collision detected, robot stops moving
    console.log(state.isRearBumperPressed); // Rear collision detected, robot stops moving
    console.log(state.isWaitingForDest); // Temporarily stopped, waiting for other robots to leave
    console.log(state.speed); // Current speed (m/s)
    console.log(state.areaId); // Current area ID
    console.log(state.isEmergencyStop); // Whether in emergency stop state
    console.log(state.x); // X component of position coordinate
    console.log(state.y); // Y component of position coordinate
    console.log(state.yaw); // Current angle (radians)
    console.log(state.locQuality); // Current positioning quality (0-100)
    console.log(state.hasObstruction); // Whether there is an obstacle
    console.log(state.errors); // Error codes
    console.log(state.isGoHome); // Whether returning to charging station
    console.log(state.timestamp); // Robot status timestamp
    // Less common
    console.log(state.moveCreator); // Move creator
    console.log(state.stuckState); // Stuck state [none: not stuck, move_stucked: movement blocked, viewport_blocked: vision blocked]
    console.log(state.moveState); // Move state [idle: idle, moving: moving, succeeded: move succeeded, cancelled: move cancelled, failed: move failed]
    console.log(state.dispatch); // Dispatch state [0: not dispatched, 3: being dispatched]
    console.log(state.isOnLine); // Robot online status, if not present, current SDK version does not support
    console.log(state.enableRcs); // Whether robot has RCS enabled, if not present, current SDK version does not support
    console.log(state.isDeviceLocked); // Locked; field missing: unlocked, if not present, current SDK version does not support
    console.log(state.voicePercent); // Volume adjustment area, if not present, current SDK version does not support
    // Lifting robot
    console.log(state.jackProgress); // Lifting up state
    // Forklift robot
    console.log(state.pushHandleMode); // Forklift driving mode
    console.log(state.robotSignal); // Forklift steering state
		...
		// do something
	}
})
...
```


````
