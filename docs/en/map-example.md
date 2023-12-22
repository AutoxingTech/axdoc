# Map Display Example

Define the map container in the HTML file:

```html
...
<div id="map" style="width:100%;height:500px;"></div>
...
```

Initialize the map

```javascript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// create an instance of AXRobot
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP);
const success = await axRobot.init();

if (success) {
// create map
const axMap = axRobot.createMap("map"); // map is the id of the HTML container tag

// Set the area to display on the map
axMap.setAreaMap("<areaId>"); // areaId is the map area identifier

// do something with map
```

[example](../example/#/showmap)
