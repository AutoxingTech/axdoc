# Lifting tasks (full)

The lifting task requires the operation point type to be a shelf point type

Operation lifting:

Lift up point A (requires point A to be a shelf point):
```typescript
	const task3 = {
		"name": "<taskName>",
		"robotId": "<robotId>",
		"runNum": <runNum>,
		"taskType": <taskType>,
		"runType": <runType>,
		"routeMode": 1,
		"runMode": 1,
		"ignorePublicSite": false,
		"speed": -1,
		"curPt": {
		},
		"pts": [{ // point A info
			"x": 2.3959287090816908,
			"y": 23.672481677407802,
			"yaw": 0,
			"stopRadius": 1,
			"areaId": "<areaId>",
			"type": -1,
			"ext": {
				"id": "<poiId>",
				"name": "<poiName>"
			},
			stepActs: [{
				type: 47 // Raise the top up
			}]
		}]
	}
	const success = axRobot.startTask(task3)
```
Place the top lift at point A (the type of point A must be a shelf point):
```typescript
	const task3 = {
		"name": "<taskName>",
		"robotId": "<robotId>",
		"runNum": <runNum>,
		"taskType": <taskType>,
		"runType": <runType>,
		"routeMode": 1,
		"runMode": 1,
		"ignorePublicSite": false,
		"speed": -1,
		"curPt": {
		},
		"pts": [{ // point A info
			"x": 2.3959287090816908,
			"y": 23.672481677407802,
			"yaw": 0,
			"stopRadius": 1,
			"areaId": "<areaId>",
			"type": -1,
			"ext": {
				"id": "<poiId>",
				"name": "<poiName>"
			},
			stepActs: [{
				type: 48 // Put down the top lift
			}]
		}]
	}
	const success = axRobot.startTask(task3)
```