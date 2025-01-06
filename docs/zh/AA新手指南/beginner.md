# 新手上路（单车控制）

因很多朋友反馈直接使用文档还是上手相对困难，为方便大家能更快更好的了解autoxing robot-js-sdk，提取下面新手上路操作。您可以直接复制代码，直接运行即可；也可摘取某些代码片段，直接运行即可。

js-sdk单车控制所有的操作的前提必须先连接上车，步骤：

-  step1：首先想要使用sdk必须先创建 AXRobot 私有化实例 new AXRobot
-  step2：创建好私有化实例后，sdk初始化 init
-  step3：连接车 connectRobot

连接车成功后，就可以开始控制车，可以对车的行为进行控制，最常用的操作如：获取机器人状态、订阅机器人状态、地图展示、发起简单点位任务、发起复杂任务等。

下方示例提供了一个完整的示例，可以参考。

|  Step1->Step2->Step3 |      Step...     | 
| ----- | ----------------- | 
| 实例 -> 初始化 -> 连接车  | -> 获取机器人状态 |
|							| -> 地图展示|
|							| -> 订阅机器人状态|
|							| -> 获取机器人所有点位数据|
|							| -> 获取机器人某个点位 -> 发起简单点位任务|

（后期根据客户反馈会继续增加常用示例）

```typescript
  
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// 创建 AXRobot 私有化实例
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP, "<serverUrl>", "<websocketUrl>");

try {
	// init
	const successed = await axRobot.init();
	if (successed) {
		// 连接指定机器人
	const res = await axRobot.connectRobot({
		robotId: "<robotId>"
	});
	console.log("connect success: " + res.robotId);

	// 获取机器人状态
	const stateObj = await axRobot.getState()
	console.log("robotState", stateObj)

	// 地图展示
	if (stateObj.areaId) {
		// 获取机器人区域id
		const areaId = stateObj.areaId
		console.log("areaId", areaId)
		// 创建地图
		const axMap = await axRobot.createMap("map"); // map 为 HTML 容器标签的 id
		// 设置地图显示的区域
		axMap.setAreaMap(areaId);  // areaId 为地图区域标识
	}

	// 订阅机器人状态
	axRobot.subscribeRealState({
		onStateChanged: state => {
		console.log("订阅机器人状态更新onStateChanged", state)
		}
	})

	// 获取机器人所有点位数据
	const result = await axRobot.getPoiList({
		robotId: "<robotId>"
	});
	const poiList = result.list
	console.log("poiList", poiList)

	// 获取机器人某个点位
	if (poiList.length > 0) {
		const poi = poiList[0]
		// 发起简单点位任务，让车动起来
		const isOk = await axRobot.addTaskSimple(poi)
		if (isOk) {
		console.log("任务发起成功")
		}
	}
		// do something with robot

	} else {
		console.log("初始化失败")
	}
} catch(err) {
	console.log(err.errText ? err.errText : err)
}

```
