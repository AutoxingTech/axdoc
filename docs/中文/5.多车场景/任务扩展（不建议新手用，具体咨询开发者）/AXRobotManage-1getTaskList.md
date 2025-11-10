# 获取任务列表

## 方法

## `getTaskList(taskRequestParam) -> {Promise.<any>}`

获取任务列表。

### 参数

| 名称               | 类型                                                        | 说明     |
| ------------------ | ------------------------------------------------ | -------- |
| `taskRequestParam` | [TaskRequestParam](../../8.数据定义/Define-TaskRequestParam) | 请求参数对象 |

### 返回值 `Promise.<any>`

| 名称         | 类型             | 说明                         |
| ------------ | --------------- | ---------------------------  |
| `count`      | Integer         | 总数据长度                    |
| `list`       | Object          | 数据集合 （taskInfo具体如下）          |

taskInfo：

| 名称         | 类型            | 说明                          |
| ------------ | ---------------------------- | --------------  |
| `isExcute`   | Boolean        | 是否执行          |
| `isCancel`   | Boolean        | 是否取消  |
| `businessId` | String         | 业务Id  |
| `name`       | String         | 任务名称  |
| `busiType`   | Integer        | 业务类型  |
| `robotId`    | String         | 机器人sn     |
| `isDel`      | Boolean        | 是否删除  |
| `taskId`     | Integer        | 任务Id  |
| `buildingId` | String         | 楼宇Id     |
| `createTime` | Integer        | 创建时间  |
| `startName`  | Integer        | 任务起点  |
| `endName`    | String         | 任务终点     |
| `robotName`  | Boolean        | 机器人名称  |
| `creatorName`| Boolean        | 创建人  |
| `startTime`  | Integer        | 任务开始时间，单位：ms  |




### 请求示例

```javascript
...
let task = {
	"pageNum": 1, //当前第几页
	"pageSize": 10, //当前页需要多少数据，最大200条
	"busiIds": ["6461a0449a3fd283a5c0bbd7"], //业务id列表
	"robotId": "", //机器人ID
	"executeStatus": 1, //1 等待 2 运行中 3 历史任务
	"orderField": 1, //1 创建时间 2 sortNo 默认是1
	"orderType": -1, //-1 降序  1  升序  默认 -1
	"dataItems": ["taskPts"], //查询结果需要输出的字段
	"isTaskStatic": true, //是否启动统计查询
	"fields": ["cStartTime", "cEndTime", "mileage"] //统计输出的字段
}
const result = await axRobot.getTaskList(taskRequestParam);
if (result && result.data) {
	let list = result.data.list;
}
...
```

### 响应数据示例

```JSON
...
{
	"count": 12126, //总数据长度
	"list": [{
		"isExcute": true, //是否执行
		"isCancel": false, //是否取消
		"businessId": "xxxx", //业务Id
		"name": "充电任务", //任务名称
		"busiType": 1, //业务类型
		"robotId": "xxxx", //机器人sn
		"isDel": false, //是否删除
		"taskId": "xxxxx", //任务Id
		"buildingId": "xxxx", //楼宇Id
		"createTime": 1706234769745, //创建时间
		"startName": "", //任务起点
		"endName": "充电桩", //任务终点
		"robotName": "", //机器人名称
		"creatorName": "xxx", //创建人
		"startTime": 1709273534942 //任务开始时间，单位：ms
	}] //数据集合
} //数据体
...
```


