
# 开发推荐
---

业务设备通过有线网络连接与底盘进行指令和信息的交互

???+ info
    推荐 业务设备 使用android系统


``` mermaid
graph 

    a[your service] <-->|wifi 4G etc| b
    
    b[Business device] <-->|eth| chassis["chassis"]
    
```

???+ question "业务设备有线连接（推荐）"
    
    业务设备:<br>
        ip:192.168.25.202<br>
        mask:255.255.255.0<br>

    访问方法 SDK 请参考
    [connectRobot AppMode.LOCAL_APP](../../AXRobot/ConnectRobots/AXRobot-connectRobot/#__tabbed_1_2)

---
