````markdown
# Get Robot List

## Method

## `getRobotList(businessId, areaId) -> {void}`

Get all robot list data under a business and map.

### Request Parameters

| Name               | Type    | Description     |
| ------------------ | ------ | -------- |
| `businessId`       | string |  Business identifier |
| `areaId`           | string |  Area identifier |

### Response Data

| Name               | Type    | Description     |
| ------------------ | ------ | -------- |
| `robotId`          | string  |  Robot identifier |
| `areaId`           | string  |  Current area identifier |
| `x`                | number  |  Current pose X coordinate |
| `y`                | number  |  Current pose Y coordinate |
| `yaw`              | integer |  Current pose orientation, unit: degrees |
| `speed`            | number  |  Current driving speed |
| `locQuality`       | integer |  Positioning accuracy, 0~100 |
| `battery`          | integer |  Battery level |
| `hasObstruction`   | boolean |  Whether there is an obstacle |
| `isCharging`       | boolean |  Whether charging |
| `isEmergencyStop`  | boolean |  Whether emergency stop is pressed |
| `isGoHome`         | boolean |  Whether returning to charging station |
| `isManualMode`     | boolean |  Whether in manual mode |
| `isRemoteMode`     | boolean |  Whether in remote control mode |
| `errors`           | Array<integer> |  Error codes |
| `timestamp`        | integer  |  Status timestamp |
| `taskObj`          | object  |  Task object |
| `taskObj.taskId`   | string  |  Task ID |
| `taskObj.isFinish` | boolean |  Whether task is finished |
| `taskObj.isCancel` | boolean |  Whether task is cancelled |


### Request Example

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
	"model": "Light Boat H1",
	"errors": [],
	"status": ""
	},
	...
]
...
```
````
