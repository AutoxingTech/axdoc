# Go back to the station to charge

Go back to the station to charge

Go Home：
```typescript
	const chargingPoi = {...} // chargingPoi
	const task = {
		name: 'Charging Task...',
		runNum: 1,
		taskType: 7,
		runType: 25,  //25 charge
		sourceType: 6, // Secondary development
		taskPts: [{
			type: chargingPoi.type,
			x: chargingPoi.coordinate[0],
			y: chargingPoi.coordinate[1],
			yaw: chargingPoi.yaw,
			areaId: chargingPoi.areaId,
			ext: {
				name: chargingPoi.name,
				id: chargingPoi.id
			}
		}]
	}
	const success = axRobot.startTask(task3)
```
