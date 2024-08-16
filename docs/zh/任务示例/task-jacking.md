# 顶升任务具体示例（全）

顶升任务要求操作点类型为为货架点类型

操作顶升：
到点A举起顶升（要求点A类型必须是货架点）：
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
				type: 47 // 举起顶升
			}]
		}]
	}
	const success = axRobot.startTask(task3)
```
到点A放下顶升（要求点A类型必须是货架点）：
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
				type: 48 // 放下顶升
			}]
		}]
	}
	const success = axRobot.startTask(task3)
```