````markdown
# Get Task List

## Method

## `getTaskList(taskRequestParam) -> {Promise.<any>}`

Get task list.

### Parameters

| Name               | Type                                                        | Description     |
| ------------------ | ------------------------------------------------ | -------- |
| `taskRequestParam` | [TaskRequestParam](../../Define/Define-TaskRequestParam.md) | Request parameter object |

### Return Value `Promise.<any>`

| Name         | Type             | Description                         |
| ------------ | --------------- | ---------------------------  |
| `count`      | Integer         | Total data count                    |
| `list`       | Object          | Data collection (taskInfo details below)          |

taskInfo:

| Name         | Type            | Description                          |
| ------------ | ---------------------------- | --------------  |
| `isExcute`   | Boolean        | Whether executed          |
| `isCancel`   | Boolean        | Whether cancelled  |
| `businessId` | String         | Business ID  |
| `name`       | String         | Task name  |
| `busiType`   | Integer        | Business type  |
| `robotId`    | String         | Robot SN     |
| `isDel`      | Boolean        | Whether deleted  |
| `taskId`     | Integer        | Task ID  |
| `buildingId` | String         | Building ID     |
| `createTime` | Integer        | Creation time  |
| `startName`  | Integer        | Task start point  |
| `endName`    | String         | Task end point     |
| `robotName`  | Boolean        | Robot name  |
| `creatorName`| Boolean        | Creator  |
| `startTime`  | Integer        | Task start time, unit: ms  |




### Request Example

```javascript
...
let task = {
	"pageNum": 1, // Current page number
	"pageSize": 10, // Data count needed for current page, max 200
	"busiIds": ["6461a0449a3fd283a5c0bbd7"], // Business ID list
	"robotId": "", // Robot ID
	"executeStatus": 1, // 1 Waiting 2 Running 3 Historical tasks
	"orderField": 1, // 1 Creation time 2 sortNo, default is 1
	"orderType": -1, // -1 Descending  1 Ascending, default -1
	"dataItems": ["taskPts"], // Fields needed in query results
	"isTaskStatic": true, // Whether to enable statistics query
	"fields": ["cStartTime", "cEndTime", "mileage"] // Fields for statistics output
}
const result = await axRobot.getTaskList(taskRequestParam);
if (result && result.data) {
	let list = result.data.list;
}
...
```

### Response Data Example

```JSON
...
{
	"count": 12126, // Total data count
	"list": [{
		"isExcute": true, // Whether executed
		"isCancel": false, // Whether cancelled
		"businessId": "xxxx", // Business ID
		"name": "Charging task", // Task name
		"busiType": 1, // Business type
		"robotId": "xxxx", // Robot SN
		"isDel": false, // Whether deleted
		"taskId": "xxxxx", // Task ID
		"buildingId": "xxxx", // Building ID
		"createTime": 1706234769745, // Creation time
		"startName": "", // Task start point
		"endName": "Charging station", // Task end point
		"robotName": "", // Robot name
		"creatorName": "xxx", // Creator
		"startTime": 1709273534942 // Task start time, unit: ms
	}] // Data collection
} // Data body
...
```



````
