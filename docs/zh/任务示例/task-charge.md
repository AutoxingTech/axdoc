# 回桩充电任务

充电任务-回桩充电

操作回桩：
回桩充电
```typescript
	const chargingPoi = {...} // 充电桩点位数据
	const task = {
		name: '回桩任务...',
		runNum: 1,
		taskType: 7,
		runType: 25,  //25回桩充电
		sourceType: 6, // 二开
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
