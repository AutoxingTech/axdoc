# 获取当前任务

## `getCurrentTask() -> {Promise.<any>}`

获取当前正在执行的任务信息。

### 返回值 `Promise.<any>`

| 名称   | 类型 | 说明     |
| ------ | ---- | -------- |
| `taskInfo` | any  | 任务信息 |

### 示例
???+ Example "getCurrentTask"

	```javascript
	...
	let taskInfo = await axRobot.getCurrentTask();
	console.log(taskInfo.isCancel); // 任务是否已取消
	console.log(taskInfo.runType); // 运行类型；0-定时消杀 1-临时消消杀 20-快捷送餐 21-多点送餐 22-引领 23-巡游 24-返航 25-回桩充电
	console.log(taskInfo.businessId); // 任务所属业务标识
	console.log(taskInfo.robotId); // 机器人标识
	console.log(taskInfo.buildingId); // 楼宇标识
	console.log(taskInfo.isExcute); // 是否已执行
	console.log(taskInfo.taskType); // 任务类型；0-消杀  1-回桩充电  2-餐厅
	console.log(taskInfo.taskPts); // 任务节点信息，具体参考开始执行任务说明
	console.log(taskInfo.createTime); // 任务创建时间
	console.log(taskInfo.runNum); // 任务运行次数
	console.log(taskInfo.name); // 任务名称
	console.log(taskInfo.busiType); // 业务类型
	console.log(taskInfo.isDel); // 是否已删除
	console.log(taskInfo.taskId); // 任务标识
	...
	```

	```javascript

	taskInfo = {
		"isCancel": false, //是否已取消
		"dispatchType": 0,
		"runType": 20, //运行类型
		"businessId": "60d998a1fcccxxxxxxxxxx", //业务id
		"backPt": {
			"ext": {
				"name": "ChargingPoint"
			}, //扩展字段，强制为object类型
			"areaId": "62a9a29a0249axxxxxxxxxx",
			"x": 3.70775374139248,
			"y": 14.108656413399421,
			"actType": -1,
			"type": 9,
			"yaw": 180
		},
		"robotId": "61822012000xxxxxx", //机器人ID
		"buildingId": "60a4c374059xxxxxxxxxx", //建筑物id
		"isExcute": false, //是否已执行
		"taskType": 2, //0 消杀 1回充电桩 2 餐厅
		"taskPts": [
			{
				"ext": {
					"name": "TaskPoint1",
					"xxx": "xxx"
				}, //扩展字段，强制为object类型
				"stepActs": [
					{
						"data": {
							"pauseTime": 30 //暂停时间,单位：秒，0代表不暂停，仅在type=18时设置
						}, //动作自定义数据
						"type": 18 //动作类型 5:播放音频，6，开箱门，18：暂停，28：关舱门，32：开关喷雾，36：关闭音频 37: 开启灯带 38: 关闭灯带
					}
				], //任务点动作类别
				"areaId": "62a9a29a0249axxxxxxxxxx",
				"x": 2.41806081987761,
				"y": 14.800125903065009,
				"actType": -1,
				"isPass": true, //任务点是否已经过，若无true,则下次执行任务不参与算路
				"yaw": 0
			},
			{
				"ext": {
					"name": "TaskPoint2",
					"xxx": "xxx"
				}, //扩展字段，强制为object类型
				"stepActs": [
					{
						"data": {
							"url": "音频在线地址",
							"playMode": 2,
							"intervalTime": 20
						}, //动作自定义数据
						"type": 5 //动作类型 5:播放音频，6，开箱门，18：暂停，28：关舱门，32：开关喷雾，36：关闭音频 37: 开启灯带 38: 关闭灯带
					}
				], //任务点动作类别
				"areaId": "62a9a29a0249axxxxxxxxxx",
				"x": 2.4106838026227706,
				"y": 11.768194034402768,
				"actType": -1,
				"isPass": false, //任务点是否已经过，若无true,则下次执行任务不参与算路
				"yaw": 0
			}
		], //待更新的任务点列表
		"createTime": 1662953493608, //创建时间
		"runNum": 1,
		"appId": "ax3e0e444xxxxxxxx",
		"name": "api消杀测试10", //任务名称
		"busiType": 0, //业务类型
		"isDel": false, //是否已删除
		"taskId": "bba7059d-2e7d-4f17-9fe1-xxxxxxxxxx", //任务ID
		"routeData": {}
	}

	```