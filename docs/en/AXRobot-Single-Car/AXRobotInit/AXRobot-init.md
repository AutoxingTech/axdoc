# Initialize

## `init() -> {Promise.<boolean>}`

Initialize the instance

### Return value `Promise.<boolean>`

Whether the initialization was successful

* `true` - success
* `fales` - failures

### Example

```javascript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP);
const successed = await axRobot.init();
if (successed) {
   // Initialization successful
   ...
} else {
   // initialization failed
   ...
}
```
