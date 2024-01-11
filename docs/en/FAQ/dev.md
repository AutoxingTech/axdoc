
# Development Recommendation
---

Business equipment interacts with the chassis through wired network connections for command and information exchange.

???+ info
    It is recommended that business equipment use the Android operating system.


``` mermaid
graph 

    a[your service] <-->|wifi 4G etc| b
    
    b[Business device] <-->|eth| chassis["chassis"]
    
```

???+ question "Wired Connection for Business Equipment (Recommended)"
    
    Business equipment:<br>
    IP: 192.168.25.202<br>
    Subnet Mask: 255.255.255.0<br>

    For SDK access, please refer to
    [connectRobot AppMode.LOCAL_APP](../../AXRobot/ConnectRobots/AXRobot-connectRobot/#__tabbed_1_2)
---
