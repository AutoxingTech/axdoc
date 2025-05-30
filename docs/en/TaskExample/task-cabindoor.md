# Task examples of cabin doors (full)

Provide task examples for the following scenarios, which have been implemented (->B opens the cabin door ->intermediate waiting for the cabin door to close ->to C):

Open the cabin door to B:

```typescript
  const task1 = {
    "name": "<taskName>",
    "robotId": "<robotId>",
    "runNum": runNum,
    "taskType": taskType,
    "runType": runType,
    "routeMode": 1,
    "runMode": 1,
    "ignorePublicSite": false,
    "speed": -1,
    "curPt": { // current point info (unnecessary)
      "x": 2.13,
      "y": 19.3725,
      "yaw": 1.67,
      "areaId": "<areaId>",
      "type": -1,
      "stopRadius": 1
    },
    "pts": [{ // point B info
      "x": 2.583684539558817,
      "y": 16.177015024538832,
      "yaw": 0,
      "stopRadius": 1,
      "areaId": "<areaId>",
      "type": -1,
      "ext": {
        "id": "<poiId>",
        "name": "<poiName>"
      },
      "stepActs": [{
        "type": 6,
        "data": {
          "mode": 1,
          "doorIds": [1, 2, 3, 4]
        }
      }]
    }]
  }
  const success = axRobot.startTask(task1)

```

(Waiting in the middle for items to be placed)
Close the cabin door (wait for 10 seconds)

```typescript
	const task2 = {
		"name": "<taskName>",
		"robotId": "<robotId>",
		"runNum": 1,
		"taskType": 6,
		"runType": 21,
		"routeMode": 1,
		"runMode": 1,
		"ignorePublicSite": false,
		"speed": -1,
		"curPt": {
			"x": 2.58,
			"y": 16.19,
			"yaw": 0,
			"areaId": "<areaId>",
			"type": -1,
			"stopRadius": 1
		},
		"pts": [{ // point B info
			"x": 2.583684539558817,
			"y": 16.177015024538832,
			"yaw": 0,
			"stopRadius": 1,
			"areaId": "<areaId>",
			"type": -1,
			"ext": {
				"id": "<poiId>",
				"name": "<poiName>"
			},
			"stepActs": [{
				"type": 28,
				"data": {
					"mode": 1,
					"doorIds": [1, 2, 3, 4]
				}
			}, {
				"type": 18,
				"data": {
					"pauseTime": 10
				}
			}]
		}]
	}
	const success = axRobot.startTask(task2)
```

to poi C ：

```typescript
	const task3 = {
		"name": "<taskName>",
		"robotId": "<robotId>",
		"runNum": 1,
		"taskType": 6,
		"runType": 21,
		"routeMode": 1,
		"runMode": 1,
		"ignorePublicSite": false,
		"speed": -1,
		"curPt": {
			"x": 2.58,
			"y": 16.1875,
			"yaw": 0,
			"areaId": "<areaId>",
			"type": -1,
			"stopRadius": 1
		},
		"pts": [{ // point C info
			"x": 2.3959287090816908,
			"y": 23.672481677407802,
			"yaw": 0,
			"stopRadius": 1,
			"areaId": "<areaId>",
			"type": -1,
			"ext": {
				"id": "<poiId>",
				"name": "<poiName>"
			}
		}]
	}
	const success = axRobot.startTask(task3)
```




