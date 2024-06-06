# subscribeRobotsStateByBus

## Method

## `subscribeRobotsStateByBus(businessId, areaId, listener) -> {void}`

Real time status of all robots under subscription services and maps. If the status of a robot changes, it will return the real-time status of a certain robot one by one.

### Parameters

| Fields         | Type           | Description            |
| ------------------ | ------------------------------------------------ | -------- |
| `listener`         | Object |  listener |


### Example

```javascript
...
await axRobot.subscribeRobotsStateByBus({
	onRobotListStatusChanged: state => {
		console.log(state.isManualMode); 
		console.log(state.isTasking);
		console.log(state.isCharging); 
		console.log(state.isRemoteMode); 
		console.log(state.battery);
		console.log(state.robotId); 
		console.log(state.speed); 
		console.log(state.areaId); 
		console.log(state.isEmergencyStop); 
		console.log(state.x); 
		console.log(state.y); 
		console.log(state.yaw);
		console.log(state.locQuality);
		console.log(state.hasObstruction);
		console.log(state.errors);
		console.log(state.isGoHome);
		console.log(state.timestamp);
		...
		// do something
	}
})
...
```

