# 获取任务详情

## 方法

## `getTaskDetail(taskId) -> {Promise.<any>}`

获取任务详情数据。

### 参数

| 名称               | 类型                                                        | 说明     |
| ------------------ | ------------------------------------------------ | -------- |
| `taskId` | string |  任务Id |

### 返回值 `Promise.<any>`

| 名称         | 类型             | 说明                         |
| ------------ | --------------- | ---------------------------  |
| `taskId`      | Integer         | 总数据长度                    |
| `name`       | Object          | 数据集合 （具体如下）          |
| `taskPts`      | Array         | 任务执行点位集合                    |
| `taskPts.ext`      | Object         | 扩展字段                    |
| `taskPts.ext.name`      | String         | 点位名称                    |
| `taskPts.areaId`      | String         | 区域Id                    |
| `runType`      | Integer         | 执行类型                    |
| `businessId`      | String         | 业务Id                    |
| `backPt`      | Object         | 返航点                    |
| `backPt.areaId`      | String         | 返航点区域Id                    |
| `backPt.ext`      | Object         | 返航点扩展                    |
| `backPt.ext.id`      | String         | 返航点Id                    |
| `backPt.ext.name`      | String         | 返航点名称                    |
| `backPt.key`      | String         | 返航点key                    |
| `backPt.stepActs`      | Array         | 返航点动作                    |
| `backPt.stepActs.data`      | Object         | 返航点动作数据                    |
| `backPt.stepActs.data.color`      | Integer         |                     |
| `backPt.stepActs.data.feature`      | Integer         |                     |
| `backPt.stepActs.data.mode`      | Integer         |                     |
| `backPt.stepActs.type`      | Integer         |                     |
| `backPt.stopRadius`      | Integer         |                     |
| `backPt.type`      | Integer         | 返航点类型                    |
| `backPt.x`      | Number         | 返航点x                    |
| `backPt.y`      | Number         | 返航点y                    |
| `backPt.yaw`      | Integer         | 返航点yaw                    |
| `speed`      | Integer         | 速度                    |
| `taskType`      | Integer         | 任务类型                    |
| `runNum`      | Integer         | 执行次数                    |
| `busiType`      | Integer         | 业务类型                    |
| `ignorePublicSite`      | Boolean         |                     |
| `isCancel`      | Boolean         | 是否取消                    |
| `isFinish`      | Boolean         | 是否完成                    |
| `robotId`      | String         | 机器人Id                    |
| `robotName`      | String         | 机器人名称                    |
| `runMode`      | Integer         | 运行模式                    |
| `buildingId`      | String         | 楼宇id                    |
| `isExcute`      | Boolean         | 是否执行                    |
| `createTime`      | Integer         | 创建时间                    |
| `routeMode`      | Integer         | 路线模式                    |
| `isDel`      | Boolean         | 是否删除                    |
| `taskState`      | String         | 任务状态：waiting：等待中，running：运行中，abort: 任务终止，cancel: 任务取消，success:任务完成                    |
| `useTime`      | Integer         | 耗时，单位：ms                    |
| `taskLogs`      | Array         | 任务日志                    |
| `taskLogs._id`      | String         | 任务日志Id                    |
| `taskLogs.taskType`      | Integer         | 任务类型                    |
| `taskLogs.logType`      | Integer         | 日志类型                    |
| `taskLogs.logName`      | String         | 日志名称                    |
| `taskLogs.timestamp`      | Integer         | 日志时间                    |
| `taskLogs.createTime`      | Integer         | 创建时间                    |
| `taskTracks`      | Object         | 任务轨迹                    |
| `data.taskTracks.65b0b1xxxxxxxdea1`      |    Array      |                     |
| `data.taskTracks.65b0b1xxxxxxxdea1.timestamp`      | Integer         |                     |
| `taskTracks.65b0b1xxxxxxxdea1.x`      | Number         |                     |
| `taskTracks.65b0b1xxxxxxxdea1.y`      | Number         |                     |
| `taskTracks.65b0b1xxxxxxxdea1.yaw`      | Number         |                     |


### 请求示例

```javascript
...
let taskInfo = await axRobot.getTaskDetail(taskId);
...
```

### 响应数据示例

```JSON
...
{
	"taskId": "61xxxxxxxxxxxxxx99", // 任务Id
	"name": "多点任务1706079197009", // 任务名称
	"taskPts": [{
		"ext": {
			"name": "3"
		}, //扩展字段
		"areaId": "65bxxxxxxxxxxa1" //区域Id
	}], //任务执行点位集合
	"runType": 21, //执行类型
	"businessId": "655xxxxxxxxxeeb", //业务Id
	"backPt": {
		"areaId": "6xxxxxxxa1",
		"ext": {
			"id": "65xxxxxxea2",
			"name": "返航中"
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
	}, //返航点
	"speed": -1,
	"taskType": 2, //任务类型
	"runNum": 1, //执行次数
	"busiType": 5, //业务类型
	"ignorePublicSite": true,
	"isCancel": false, //是否取消
	"isFinish": false, //是否完成
	"robotId": "8981307a02163yT",
	"robotName": "63yT",
	"runMode": 1, //运行模式
	"buildingId": "64xxxxxxxc", //楼宇id
	"isExcute": false, //是否执行
	"createTime": 1706079196905, //创建时间
	"routeMode": 1, //路线模式
	"isDel": false, //是否删除
	"taskState": "success", //任务状态：waiting：等待中，running：运行中，abort: 任务终止，cancel: 任务取消，success:任务完成
	"useTime": 29078, //耗时，单位：ms
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
		{
			"_id": "65b0b3e28171a93d2ca362dd",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "play-audio",
			"Data": {
				"audioId": "/storage/xxxxxx.mp3",
				"channel": 1,
				"duration": -1,
				"forcePlay": true,
				"interval": -1,
				"mode": 1,
				"num": 1,
				"volume": 50
			},
			"timestamp": 1706079198463,
			"createTime": 1706079202391
		},
		{
			"_id": "65b0b3e28171a93d2ca362de",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "set-speed",
			"Data": {
				"speed": 1.2
			},
			"timestamp": 1706079198586,
			"createTime": 1706079202393
		},
		{
			"_id": "65b0b3f48171a93d2ca362df",
			"taskType": "restaurant",
			"logType": "state",
			"logName": "dest-arrive",
			"Data": {
				"current": {
					"id": "65bxxxxxxx4",
					"index": 0,
					"name": "3"
				}
			},
			"timestamp": 1706079217941,
			"createTime": 1706079220441
		},
		{
			"_id": "65b0b3f48171a93d2ca362e0",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "play-audio",
			"Data": {
				"audioId": "/storage/xxxx.mp3",
				"duration": -1,
				"forcePlay": true,
				"interval": -1,
				"mode": 1,
				"num": 1,
				"volume": 50
			},
			"timestamp": 1706079217949,
			"createTime": 1706079220443
		},
		{
			"_id": "65b0b3f48171a93d2ca362e1",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "turn-on-light",
			"Data": {
				"color": 5,
				"feature": 3,
				"mode": 1
			},
			"timestamp": 1706079217959,
			"createTime": 1706079220445
		},
		{
			"_id": "65b0b3fd8171a93d2ca362e2",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "turn-on-light",
			"Data": {
				"color": 4,
				"feature": 1,
				"mode": 1
			},
			"timestamp": 1706079226522,
			"createTime": 1706079229665
		},
		{
			"_id": "65b0b4188171a93d2ca362eb",
			"taskType": "restaurant",
			"logType": "state",
			"logName": "dest-arrive",
			"Data": {
				"current": {
					"id": "65bxxxxxxx6cdea2",
					"name": "返航中",
					"type": 9
				}
			},
			"timestamp": 1706079251803,
			"createTime": 1706079256550
		},
		{
			"_id": "65b0b4188171a93d2ca362ec",
			"taskType": "restaurant",
			"logType": "event",
			"logName": "turn-on-light",
			"Data": {
				"color": 4,
				"feature": 1,
				"mode": 1
			},
			"timestamp": 1706079251814,
			"createTime": 1706079256552
		},
		{
			"_id": "65b0b42d8171a93d2ca362ed",
			"taskType": "restaurant",
			"logType": "state",
			"logName": "task-end",
			"Data": {
				"endType": "success"
			},
			"timestamp": 1706079274736,
			"createTime": 1706079277619
		}
	], //任务日志
	"taskTracks": {
		"65b0b1xxxxxxxdea1": [{
				"timestamp": 1706079198600,
				"x": 0.0725,
				"y": -0.005,
				"yaw": 1.53
			},
			{
				"timestamp": 1706079199700,
				"x": 0.075,
				"y": -0.0025,
				"yaw": 1.53
			},
			{
				"timestamp": 1706079200756,
				"x": 0.07,
				"y": 0.0375,
				"yaw": 1.57
			},
			{
				"timestamp": 1706079201816,
				"x": 0.0875,
				"y": 0.075,
				"yaw": 1.15
			},
			{
				"timestamp": 1706079202876,
				"x": 0.1525,
				"y": 0.1325,
				"yaw": 0.14
			},
			{
				"timestamp": 1706079203926,
				"x": 0.59,
				"y": 0.125,
				"yaw": -0.09
			},
			{
				"timestamp": 1706079205012,
				"x": 1.47,
				"y": 0.085,
				"yaw": -0.03
			},
			{
				"timestamp": 1706079206051,
				"x": 2.6775,
				"y": 0.2525,
				"yaw": 0.23
			},
			{
				"timestamp": 1706079207089,
				"x": 3.82,
				"y": 0.6125,
				"yaw": 0.21
			},
			{
				"timestamp": 1706079208132,
				"x": 4.74,
				"y": 0.73,
				"yaw": -0.13
			},
			{
				"timestamp": 1706079209169,
				"x": 5.1275,
				"y": 0.65,
				"yaw": -0.4
			},
			{
				"timestamp": 1706079210253,
				"x": 5.31,
				"y": 0.5475,
				"yaw": -1.15
			},
			{
				"timestamp": 1706079211285,
				"x": 5.315,
				"y": 0.5125,
				"yaw": 4.7
			},
			{
				"timestamp": 1706079212379,
				"x": 5.3125,
				"y": 0.5025,
				"yaw": -1.5
			},
			{
				"timestamp": 1706079213407,
				"x": 5.24,
				"y": 0.27,
				"yaw": -0.53
			},
			{
				"timestamp": 1706079214434,
				"x": 5.2475,
				"y": 0.265,
				"yaw": -0.18
			},
			{
				"timestamp": 1706079215457,
				"x": 5.25,
				"y": 0.2625,
				"yaw": -0.07
			},
			{
				"timestamp": 1706079216481,
				"x": 5.245,
				"y": 0.26,
				"yaw": -0.01
			},
			{
				"timestamp": 1706079217514,
				"x": 5.2625,
				"y": 0.2625,
				"yaw": 0.02
			},
			{
				"timestamp": 1706079218578,
				"x": 5.255,
				"y": 0.2625,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079219594,
				"x": 5.26,
				"y": 0.2625,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079220617,
				"x": 5.26,
				"y": 0.265,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079221638,
				"x": 5.2625,
				"y": 0.265,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079223262,
				"x": 5.26,
				"y": 0.265,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079224280,
				"x": 5.2575,
				"y": 0.265,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079226309,
				"x": 5.2625,
				"y": 0.265,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079226548,
				"x": 5.2625,
				"y": 0.265,
				"yaw": 0.01
			},
			{
				"timestamp": 1706079227612,
				"x": 5.26,
				"y": 0.2625,
				"yaw": 0.08
			},
			{
				"timestamp": 1706079228649,
				"x": 5.2425,
				"y": 0.265,
				"yaw": 1.08
			},
			{
				"timestamp": 1706079229689,
				"x": 5.21,
				"y": 0.44,
				"yaw": 2.24
			},
			{
				"timestamp": 1706079230729,
				"x": 4.76,
				"y": 0.6325,
				"yaw": 3.1
			},
			{
				"timestamp": 1706079231785,
				"x": 4.08,
				"y": 0.5025,
				"yaw": 3.36
			},
			{
				"timestamp": 1706079232817,
				"x": 3.0825,
				"y": 0.2375,
				"yaw": 3.38
			},
			{
				"timestamp": 1706079233846,
				"x": 2.245,
				"y": 0.0025,
				"yaw": 3.33
			},
			{
				"timestamp": 1706079234872,
				"x": 1.5925,
				"y": -0.0575,
				"yaw": 3.05
			},
			{
				"timestamp": 1706079235899,
				"x": 1.05,
				"y": 0.02,
				"yaw": 2.91
			},
			{
				"timestamp": 1706079236938,
				"x": 0.76,
				"y": 0.0925,
				"yaw": 2.76
			},
			{
				"timestamp": 1706079237967,
				"x": 0.765,
				"y": 0.0925,
				"yaw": 2.76
			},
			{
				"timestamp": 1706079238999,
				"x": 0.7675,
				"y": 0.095,
				"yaw": 2.76
			},
			{
				"timestamp": 1706079240031,
				"x": 0.7625,
				"y": 0.105,
				"yaw": 2.76
			},
			{
				"timestamp": 1706079241061,
				"x": 0.7475,
				"y": 0.1075,
				"yaw": 2.68
			},
			{
				"timestamp": 1706079242086,
				"x": 0.535,
				"y": 0.2375,
				"yaw": 2.49
			},
			{
				"timestamp": 1706079243131,
				"x": 0.405,
				"y": 0.3325,
				"yaw": 2.49
			},
			{
				"timestamp": 1706079244163,
				"x": 0.3975,
				"y": 0.3325,
				"yaw": 2.48
			},
			{
				"timestamp": 1706079245192,
				"x": 0.38,
				"y": 0.3575,
				"yaw": 2.26
			},
			{
				"timestamp": 1706079246227,
				"x": 0.38,
				"y": 0.35,
				"yaw": 2.24
			},
			{
				"timestamp": 1706079247250,
				"x": 0.3775,
				"y": 0.35,
				"yaw": 2.42
			},
			{
				"timestamp": 1706079248289,
				"x": 0.3775,
				"y": 0.3525,
				"yaw": 2.79
			},
			{
				"timestamp": 1706079249329,
				"x": 0.3725,
				"y": 0.3725,
				"yaw": 3.78
			},
			{
				"timestamp": 1706079250351,
				"x": 0.39,
				"y": 0.39,
				"yaw": 3.97
			},
			{
				"timestamp": 1706079251378,
				"x": 0.3875,
				"y": 0.39,
				"yaw": 4.02
			},
			{
				"timestamp": 1706079252441,
				"x": 0.3875,
				"y": 0.39,
				"yaw": 4.02
			},
			{
				"timestamp": 1706079253468,
				"x": 0.3575,
				"y": 0.3325,
				"yaw": 4.35
			},
			{
				"timestamp": 1706079254490,
				"x": 0.31,
				"y": 0.19,
				"yaw": 4.16
			},
			{
				"timestamp": 1706079255511,
				"x": 0.2275,
				"y": 0.1275,
				"yaw": 3.15
			},
			{
				"timestamp": 1706079256528,
				"x": 0.17,
				"y": 0.1625,
				"yaw": 2.02
			},
			{
				"timestamp": 1706079257547,
				"x": 0.155,
				"y": 0.17,
				"yaw": 1.73
			},
			{
				"timestamp": 1706079258567,
				"x": 0.1475,
				"y": 0.175,
				"yaw": 1.42
			},
			{
				"timestamp": 1706079259596,
				"x": 0.135,
				"y": 0.1725,
				"yaw": 1.13
			},
			{
				"timestamp": 1706079260617,
				"x": 0.125,
				"y": 0.1875,
				"yaw": 0.99
			},
			{
				"timestamp": 1706079261641,
				"x": 0.13,
				"y": 0.19,
				"yaw": 0.91
			},
			{
				"timestamp": 1706079262669,
				"x": 0.1275,
				"y": 0.195,
				"yaw": 0.86
			},
			{
				"timestamp": 1706079263691,
				"x": 0.1125,
				"y": 0.185,
				"yaw": 0.88
			},
			{
				"timestamp": 1706079264719,
				"x": 0.09,
				"y": 0.1475,
				"yaw": 0.95
			},
			{
				"timestamp": 1706079265739,
				"x": 0.085,
				"y": 0.1225,
				"yaw": 1.11
			},
			{
				"timestamp": 1706079266770,
				"x": 0.0875,
				"y": 0.1175,
				"yaw": 1.15
			},
			{
				"timestamp": 1706079267793,
				"x": 0.08,
				"y": 0.0925,
				"yaw": 1.31
			},
			{
				"timestamp": 1706079268811,
				"x": 0.09,
				"y": 0.0725,
				"yaw": 1.44
			},
			{
				"timestamp": 1706079269830,
				"x": 0.085,
				"y": 0.055,
				"yaw": 1.54
			},
			{
				"timestamp": 1706079270848,
				"x": 0.095,
				"y": 0.035,
				"yaw": 1.6
			},
			{
				"timestamp": 1706079271866,
				"x": 0.0975,
				"y": 0.015,
				"yaw": 1.61
			},
			{
				"timestamp": 1706079272895,
				"x": 0.1,
				"y": 0.0025,
				"yaw": 1.6
			},
			{
				"timestamp": 1706079273913,
				"x": 0,
				"y": 0,
				"yaw": 1.6
			},
			{
				"timestamp": 1706079274740,
				"x": -0.1,
				"y": -0.2,
				"yaw": 0.8
			},
			{
				"timestamp": 1706079274753,
				"x": -0.1,
				"y": -0.2,
				"yaw": 0.8
			}
		]
	} //任务轨迹
} //数据体
...
```


