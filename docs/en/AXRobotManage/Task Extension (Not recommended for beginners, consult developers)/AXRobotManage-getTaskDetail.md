````markdown
# Get Task Details

## Method

## `getTaskDetail(taskId) -> {Promise.<any>}`

Get task detail data.

### Parameters

| Name               | Type                                                        | Description     |
| ------------------ | ------------------------------------------------ | -------- |
| `taskId` | string |  Task ID |

### Return Value `Promise.<any>`

| Name         | Type             | Description                         |
| ------------ | --------------- | ---------------------------  |
| `taskId`      | Integer         | Task ID                    |
| `name`       | Object          | Task name          |
| `taskPts`      | Array         | Task execution point collection                    |
| `taskPts.ext`      | Object         | Extension field                    |
| `taskPts.ext.name`      | String         | Point name                    |
| `taskPts.areaId`      | String         | Area ID                    |
| `runType`      | Integer         | Run type                    |
| `businessId`      | String         | Business ID                    |
| `backPt`      | Object         | Return point                    |
| `backPt.areaId`      | String         | Return point area ID                    |
| `backPt.ext`      | Object         | Return point extension                    |
| `backPt.ext.id`      | String         | Return point ID                    |
| `backPt.ext.name`      | String         | Return point name                    |
| `backPt.key`      | String         | Return point key                    |
| `backPt.stepActs`      | Array         | Return point actions                    |
| `backPt.stepActs.data`      | Object         | Return point action data                    |
| `backPt.stepActs.data.color`      | Integer         |                     |
| `backPt.stepActs.data.feature`      | Integer         |                     |
| `backPt.stepActs.data.mode`      | Integer         |                     |
| `backPt.stepActs.type`      | Integer         |                     |
| `backPt.stopRadius`      | Integer         |                     |
| `backPt.type`      | Integer         | Return point type                    |
| `backPt.x`      | Number         | Return point x                    |
| `backPt.y`      | Number         | Return point y                    |
| `backPt.yaw`      | Integer         | Return point yaw                    |
| `speed`      | Integer         | Speed                    |
| `taskType`      | Integer         | Task type                    |
| `runNum`      | Integer         | Run count                    |
| `busiType`      | Integer         | Business type                    |
| `ignorePublicSite`      | Boolean         |                     |
| `isCancel`      | Boolean         | Whether cancelled                    |
| `isFinish`      | Boolean         | Whether finished                    |
| `robotId`      | String         | Robot ID                    |
| `robotName`      | String         | Robot name                    |
| `runMode`      | Integer         | Run mode                    |
| `buildingId`      | String         | Building ID                    |
| `isExcute`      | Boolean         | Whether executed                    |
| `createTime`      | Integer         | Creation time                    |
| `routeMode`      | Integer         | Route mode                    |
| `isDel`      | Boolean         | Whether deleted                    |
| `taskState`      | String         | Task state: waiting: waiting, running: running, abort: task aborted, cancel: task cancelled, success: task completed                    |
| `useTime`      | Integer         | Time used, unit: ms                    |
| `taskLogs`      | Array         | Task logs                    |
| `taskLogs._id`      | String         | Task log ID                    |
| `taskLogs.taskType`      | Integer         | Task type                    |
| `taskLogs.logType`      | Integer         | Log type                    |
| `taskLogs.logName`      | String         | Log name                    |
| `taskLogs.timestamp`      | Integer         | Log time                    |
| `taskLogs.createTime`      | Integer         | Creation time                    |
| `taskTracks`      | Object         | Task tracks                    |
| `data.taskTracks.65b0b1xxxxxxxdea1`      |    Array      |                     |
| `data.taskTracks.65b0b1xxxxxxxdea1.timestamp`      | Integer         |                     |
| `taskTracks.65b0b1xxxxxxxdea1.x`      | Number         |                     |
| `taskTracks.65b0b1xxxxxxxdea1.y`      | Number         |                     |
| `taskTracks.65b0b1xxxxxxxdea1.yaw`      | Number         |                     |


### Request Example

```javascript
...
let taskInfo = await axRobot.getTaskDetail(taskId);
...
```

### Response Data Example

```JSON
...
{
	"taskId": "61xxxxxxxxxxxxxx99", // Task ID
	"name": "Multi-point task 1706079197009", // Task name
	"taskPts": [{
		"ext": {
			"name": "3"
		}, // Extension field
		"areaId": "65bxxxxxxxxxxa1" // Area ID
	}], // Task execution point collection
	"runType": 21, // Run type
	"businessId": "655xxxxxxxxxeeb", // Business ID
	"backPt": {
		"areaId": "6xxxxxxxa1",
		"ext": {
			"id": "65xxxxxxea2",
			"name": "Returning"
		},
		"key": "",
		"stepActs": [{
			"data": {
				"color": 4,
				"feature": 1,
				"mode": 1
			},
			"type": 37
		}],
		"stopRadius": 1,
		"type": 9,
		"x": -0.2579306188960005,
		"y": -0.3057315748102021,
		"yaw": 50
	}, // Return point
	"speed": -1,
	"taskType": 2, // Task type
	"runNum": 1, // Run count
	"busiType": 5, // Business type
	"ignorePublicSite": true,
	"isCancel": false, // Whether cancelled
	"isFinish": false, // Whether finished
	"robotId": "8981307a02163yT",
	"robotName": "63yT",
	"runMode": 1, // Driving mode, default is 1 <br/>1: Flexible obstacle avoidance<br/>2: Drive along track<br/>3: Strictly drive along track<br/>4: Drive along track without rack docking point<br/>5: Segmented mode<br/>
	"buildingId": "64xxxxxxxc", // Building ID
	"isExcute": false, // Whether executed
	"createTime": 1706079196905, // Creation time
	"routeMode": 1, // Route mode
	"isDel": false, // Whether deleted
	"taskState": "success", // Task state: waiting: waiting, running: running, abort: task aborted, cancel: task cancelled, success: task completed
	"useTime": 29078, // Time used, unit: ms
	"taskLogs": [{
			"_id": "65b0b3e28171a93d2ca362db",
			"taskType": "restaurant",
			"logType": "state",
			"logName": "task-start",
			"timestamp": 1706079198426,
			"createTime": 1706079202386
		},
		{
			"_id": "65b0b3e28171a93d2ca362dc",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "turn-on-light",
			"Data": {
				"color": 4,
				"feature": 1,
				"mode": 1
			},
			"timestamp": 1706079198446,
			"createTime": 1706079202389
		},
		...
	], // Task logs
	"taskTracks": {
		"65b0b1xxxxxxxdea1": [{
				"timestamp": 1706079198600,
				"x": 0.0725,
				"y": -0.005,
				"yaw": 1.53
			},
			...
		]
	} // Task tracks
} // Data body
...
```



````
