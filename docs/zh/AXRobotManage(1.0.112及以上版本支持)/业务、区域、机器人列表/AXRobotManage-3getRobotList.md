# 获取机器人列表

## 方法

## `getRobotList(businessId, areaId) -> {void}`

获取业务下、地图下 所有机器人列表数据。

### 请求参数

| 名称               | 类型    | 说明     |
| ------------------ | ------ | -------- |
| `businessId`       | string |  业务标识 |
| `areaId`           | string |  区域标识 |

### 响应数据

| 名称               | 类型    | 说明     |
| ------------------ | ------ | -------- |
| `robotId`          | string  |  机器人标识 |
| `areaId`           | string  |  当前所在区域标识 |
| `x`                | number  |  当前位姿的 X 坐标 |
| `y`                | number  |  当前位姿的 Y 坐标 |
| `yaw`              | integer |  当前位姿的朝向，单位：度 |
| `speed`            | number  |  当前行驶速度 |
| `locQuality`       | integer |  定位精度，0~100 |
| `battery`          | integer |  是否有障碍物 |
| `hasObstruction`   | boolean |  机器人标识 |
| `isCharging`       | boolean |  是否在充电 |
| `isEmergencyStop`  | boolean |  是否按下了急停 |
| `isGoHome`         | boolean |  是否正在回桩 |
| `isManualMode`     | boolean |  是否处于手动模式 |
| `isRemoteMode`     | boolean |  是否处于远控模式 |
| `errors`           | Array<integer> |  故障码 |
| `timestamp`        | integer  |  状态时间戳 |
| `taskObj`          | object  |  任务对象 |
| `taskObj.taskId`   | string  |  任务ID |
| `taskObj.isFinish` | boolean |  任务是否已结束 |
| `taskObj.isCancel` | boolean |  任务是否取消 |


### 请求示例

```javascript
...
let robotList = await axRobot.getRobotList(businessId, areaId)
...
```

### 响应数据示例

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