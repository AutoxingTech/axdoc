# 任务应用场景示例

提供下以下场景的task示例：

到B开舱门：

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

(中间等待可放入物品)
关舱门 (等待10s)

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

到点C ：

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
				type: 47, // 举起顶升
				"data": {
            	}
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
				type: 48, // 放下顶升
				"data": {
            	}
			}]
		}]
	}
	const success = axRobot.startTask(task3)
```


多点任务到达后暂停等待交互：
```typescript
const task4 = {
    "name": "多点任务",
    "runMode": <runMode>,
    "runNum": <runNum>,
    "taskType": <taskType>,
    "runType": <runType>,
    "curPt": {},
    "pts": [
        {
            "x": 6.7925255925160855,
            "y": 1.2596787664165277,
            "yaw": 268,
            "areaId": "66879695c207ce62f87991c7",
            "dockingRadius": "1",
            "ext": {
                "name": "点位一",
                "id": "668796861f783f4b11c89ddc"
            },
            "stepActs": [
                {
                    "type": 40
                },
            ]
        },
        {
            "x": 9.005738806990848,
            "y": 1.2387888340015252,
            "yaw": 268,
            "areaId": "66879695c207ce62f87991c7",
            "dockingRadius": "1",
            "ext": {
                "name": "点位二",
                "id": "668796861f783f4b11c89dde"
            },
            "stepActs": [
                {
                    "type": 40
                },
            ]
        }
    ],
    "backPt": {},
    "ignorePublicSite": true,
    "ext": {
        "checkItems": [
            "elevator"
        ]
    },
    "soureceType": 1,
    "detourRadius": 1
}
const success = axRobot.startTask(task4)
```




