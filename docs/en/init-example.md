# SDK Initialization Example

The SDK can be used normally after the initialization is completed. The following is an example of SDK initialization code:

``` javascript

import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// create an instance of AXRobot
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP);

// Initialize the AXRobot instance
const successed = await axRobot.init();
if (successed) {
   try {
     // connect to the specified robot
     const res = await axRobot.connectRobot({
       robotId: "<robotId>"
     });
     console.log("connect success: " + res.robotId);
     // do something with robot
   } catch(err) {
     console.log(err.errText)
   }
} else {
   // initialization failed
}

```

> * **appId** - the application ID, which can be applied to relevant operators
> * **appSecret** - data request key, which can be provided to relevant operators
> * **AppMode** - [AppMode](../Define/Define-AppMode)


[example](https://service.autoxing.com/sdk/v1.0/example/#/)
