# 机器人WIFI相关问题

## 底盘访问方式

- eth 有线连接（推荐）
- wifi 无线连接 (调试)

???+ question "业务设备有线连接（推荐）"

    === "有线连接"
        ???+ note "业务设备设置"
            业务设备:<br>
                ip:192.168.25.202<br>
                mask:255.255.255.0<br>

            访问方法 SDK 请参考
            [connectRobot AppMode.LOCAL_APP](../../AXRobot/ConnectRobots/AXRobot-connectRobot/#__tabbed_1_2)

    === "wifi连接-AP模式"
        <a name="wifi_ap"></a>

        ???+ note "AP模式"
            热点名称：底盘序列号(sn)<br>
            默认密码：12345678<br>
            DHCP: 开启<br>
            底盘IP：192.168.12.1<br>

            

            访问方法 

            - SDK 请参考 [connectRobot AppMode.LAN_APP](../../AXRobot/ConnectRobots/AXRobot-connectRobot/#__tabbed_1_3)
            - RESTAPI 通过 192.168.12.1 访问




    === "wifi连接-STA模式"

        ???+ note "STA模式"
            
            需要知道分配给底盘的WIFI IP，并通过这个IP访问

---

## 如何设置底盘wifi工作模式
<a name="setup_wifi_mode"></a>
底盘的工作模式

- AP 模式 (默认)
- STA 模式


???+ question "切换方法"

    - AP 模式 连接任意wifi会自动切换成STA模式，连接失败后会自动切换回AP模式
    - STA 模式 连续按电源键10次，每次间隔不超过1秒，会将wifi模式重置为AP模式

---
## 底盘wifi连接其他AP的方法

???+ question "方法"

    1. 将底盘wifi模式[设置为AP模式](?h=AP#setup_wifi_mode)
    - [电脑连接底盘热点](?h=AP#wifi_ap)
    - 浏览器访问 http://192.168.12.1:8000/wifi_setup 进行修改

