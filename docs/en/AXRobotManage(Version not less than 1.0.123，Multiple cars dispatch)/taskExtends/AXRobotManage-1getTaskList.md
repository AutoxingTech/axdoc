# getTaskList

## Method

## `getTaskList(taskRequestParam) -> {Promise.<any>}`

Get task list

### Parameters

| Fields         | Type           | Description            |
| ------------------ | ------------------------------------------------ | -------- |
| `taskRequestParam` | [TaskRequestParam](../../../Define/Define-TaskRequestParam) | Request parameter object |

### Return Value `Promise.<any>`

| Fields         | Type           | Description            |
| ------------ | --------------- | ---------------------------  |
| `count`      | Integer         | count                    |
| `list`       | Object          | list （taskInf:）          |

taskInfo：

| Fields         | Type           | Description            |
| ------------ | ---------------------------- | --------------  |
| `isExcute`   | Boolean        | isExcute          |
| `isCancel`   | Boolean        | isCancel  |
| `businessId` | String         | businessId  |
| `name`       | String         | name  |
| `busiType`   | Integer        | businessType  |
| `robotId`    | String         | robotId     |
| `isDel`      | Boolean        | isDel  |
| `taskId`     | Integer        | taskId  |
| `buildingId` | String         | buildingId     |
| `createTime` | Integer        | createTime  |
| `startName`  | Integer        | startName  |
| `endName`    | String         | endName     |
| `robotName`  | Boolean        | robotName  |
| `creatorName`| Boolean        | creatorName  |
| `startTime`  | Integer        | startTime(ms)  |




### Request Example

```javascript
...
let task = {
	"pageNum": 1, 
	"pageSize": 10, 
	"busiIds": ["6461a0449a3fd283a5c0bbd7"], 
	"robotId": "", 
	"executeStatus": 1, 
	"orderField": 1, 
	"orderType": -1, 
	"dataItems": ["taskPts"], 
	"isTaskStatic": true, 
	"fields": ["cStartTime", "cEndTime", "mileage"] 
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
	"count": 12126,
	"list": [{
		"isExcute": true, 
		"isCancel": false, 
		"businessId": "xxxx",
		"name": "<name>", 
		"busiType": 1,
		"robotId": "xxxx", 
		"isDel": false, 
		"taskId": "xxxxx", 
		"buildingId": "xxxx", 
		"createTime": 1706234769745, 
		"startName": "", 
		"endName": "", 
		"robotName": "", 
		"creatorName": "xxx", 
		"startTime": 1709273534942 
	}] 
} 
...
```


