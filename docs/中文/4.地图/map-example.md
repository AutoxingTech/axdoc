# 地图显示示例

在 HTML 文件中定义地图容器：

```html
...
<div id="map" style="width:100%;height:500px;"></div>
...
```

初始化地图

```typescript
import { AXRobot, AppMode } from "@autoxing/robot-js-sdk";

// 创建 AXRobot 实例
const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.WAN_APP);
const success = await axRobot.init();

if (success) {
// 创建地图
const axMap = axRobot.createMap("map"); // map 为 HTML 容器标签的 id

// 设置地图显示的区域
axMap.setAreaMap("<areaId>");  // areaId 为地图区域标识

// do something with map
```

[示例](https://service.autoxing.com/sdk/v1.0/example/#/showmap)