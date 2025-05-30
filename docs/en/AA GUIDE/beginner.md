# Novice on the road (bicycle control)

Due to feedback from many friends that using the documentation directly is still relatively difficult to get started with, in order to facilitate everyone's faster and better understanding of the Yixing Robot JS SDK, we have extracted the following novice on road operations. You can simply copy the code and run it directly; You can also extract certain code snippets and run them directly.

The prerequisite for controlling all operations of the JS SDK bicycle is to first connect to the vehicle. Steps:
-Step 1: To use the SDK, you must first create a new AXRobot instance
-Step 2: After creating the instance, the SDK initializes the init
-Step 3: Connect the car to the ConnectRobot

After successfully connecting the car, you can start controlling the car and control its behavior. The most commonly used operations include obtaining the robot status, subscribing to the robot status, displaying the map, initiating simple positioning tasks, initiating complex tasks, etc.


he following example provides a complete example for reference.

|  Step1->Step2->Step3 |      Step...     | 
| ----- | ----------------- | 
| new AXRobot-> init -> connectRobot  | -> getState |
|							| -> setAreaMap|
|							| -> subscribeRealState|
|							| -> getPoiList|
|							| -> getOnePoi -> addTaskSimple|


(We will continue to add common examples based on customer feedback in the future)

```typescript
  
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// new AXRobot
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP, "<serverUrl>", "<websocketUrl>");

try {
	// init
	const successed = await axRobot.init();
	if (successed) {
		// connectRobot
	const res = await axRobot.connectRobot({
		robotId: "<robotId>"
	});
	console.log("connect success: " + res.robotId);

	// getState
	const stateObj = await axRobot.getState()
	console.log("robotState", stateObj)

	// map
	if (stateObj.areaId) {
		// areaId
		const areaId = stateObj.areaId
		console.log("areaId", areaId)
		// createMap
		const axMap = await axRobot.createMap("map");
		// setAreaMap
		axMap.setAreaMap(areaId);
	}

	// subscribeRealState
	axRobot.subscribeRealState({
		onStateChanged: state => {
		console.log("robot state onStateChanged", state)
		}
	})

	// get all pois
	const result = await axRobot.getPoiList({
		robotId: "<robotId>"
	});
	const poiList = result.list
	console.log("poiList", poiList)

	// get one poi
	if (poiList.length > 0) {
		const poi = poiList[0]
		// addTaskSimple
		const isOk = await axRobot.addTaskSimple(poi)
		if (isOk) {
		console.log("Add task success")
		}
	}
		// do something with robot

	} else {
		console.log("init failed")
	}
} catch(err) {
	console.log(err.errText ? err.errText : err)
}

```
