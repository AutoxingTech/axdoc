# AppMode

App Mode

## Enum

| Value                         | Description                                                    |
| -------------------------- | -------------------------------------------------------- |
| `AppMode.WAN_APP`          | Wide Area Network (WAN) mode is primarily designed for mini-programs, mobile terminal apps, and PC web.                                                     |
| `AppMode.LOCAL_APP`     |  Local mode is mainly intended for upper computer terminal apps, and so on. |
| `AppMode.LAN_APP`      | Local Area Network (LAN) mode is primarily aimed at mobile terminals within Wi-Fi LAN, such as pads and smartphones.         |


```javascript

const axRobot = new AXRobot("<appId>", "<appSecret>", AppMode.LOCAL_APP);



```