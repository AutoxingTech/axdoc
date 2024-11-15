# getRobotList

## Method

## `getRobotList(businessId, areaId) -> {void}`

Obtain the list data of all robots under the business and map. 

### Parameters

| Fields         | Type           | Description            |
| ------------------ | ------ | -------- |
| `businessId`       | string |  businessId |
| `areaId`           | string |  areaId |

### Response Data

| Fields         | Type           | Description            |
| ------------------ | ------ | -------- |
| `robotId`          | string  |  robotId |
| `areaId`           | string  |  areaId |
| `x`                | number  |  X coordinate |
| `y`                | number  |  Y coordinate|
| `yaw`              | integer |  yaw, in degrees|
| `speed`            | number  |  speed |
| `locQuality`       | integer |  0~100 |
| `battery`          | integer |  battery |
| `hasObstruction`   | boolean |  hasObstruction |
| `isCharging`       | boolean |  isCharging |
| `isEmergencyStop`  | boolean |  isEmergencyStop |
| `isGoHome`         | boolean |  isGoHome |
| `isManualMode`     | boolean |  isManualMode |
| `isRemoteMode`     | boolean |  isRemoteMode |
| `errors`           | Array<integer> |  errors |
| `timestamp`        | integer  |  timestamp |
| `taskObj`          | object  |  taskObj |
| `taskObj.taskId`   | string  |  taskId |
| `taskObj.isFinish` | boolean |  isFinish |
| `taskObj.isCancel` | boolean |  isCancel |


### Example

```javascript
...
let robotList = await axRobot.getRobotList(businessId, areaId)
...
```

### Response Data Example

```JSON
...
"list": [
	{
	"img": "../../static/img/ic_def_robot.png",
	"isTask": false,
	"isManualMode": false,
	"isCharging": false,
	"isRemoteMode": false,
	"battery": 0,
	"robotId": "618110810000110",
	"mac": "test",
	"yaw": 0.0,
	"isError": false,
	"areaId": "",
	"activeStatus": 1,
	"name": "",
	"x": 0.0,
	"y": 0.0,
	"isEmergencyStop": false,
	"model": "è½»èˆŸH1",
	"errors": [],
	"status": ""
	},
	...
]
...
```