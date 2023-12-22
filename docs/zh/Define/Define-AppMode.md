# AppMode

应用模式

## 枚举

| 值                         | 说明                                                     |
| -------------------------- | -------------------------------------------------------- |
| `AppMode.WAN_APP`          | 广域网模式，主要针对小程序、移动终端App、PC端web等                                                      |
| `AppMode.LOCAL_APP`     | 本地模式，主要针对上位机终端App等      |
| `AppMode.LAN_APP`      | 局域网模式，主要针对Wi-Fi局域网内移动终端（如pad、手机）等         |


```javascript

const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.LOCAL_APP);



```