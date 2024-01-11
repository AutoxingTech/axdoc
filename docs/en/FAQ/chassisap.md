# Robot WIFI-related issues

## Chassis Access Methods

- Ethernet (Wired Connection) - Recommended
- WiFi (Wireless Connection) - Debugging

???+ question "Wired Connection for Business Equipment (Recommended)"

    === "Wired connection"
        ???+ note "Business Device Settings"
            Business Equipment:<br>
                ip:192.168.25.202<br>
                mask:255.255.255.0<br>

            Please refer to the access method SDK
            [connectRobot AppMode.LOCAL_APP](../../AXRobot/ConnectRobots/AXRobot-connectRobot/#__tabbed_1_2)

    === "wifi connection-AP mode"
        <a name="wifi_ap"></a>

        ???+ note "AP mode"
            Hotspot name: Chassis serial number (sn)<br>
            Default password: 12345678<br>
            DHCP: Enable<br>
            Chassis IP: 192.168.12.1<br>

            

            Access method

            - SDK please refer to [connectRobot AppMode.LAN_APP](../../AXRobot/ConnectRobots/AXRobot-connectRobot/#__tabbed_1_3)
            - RESTAPI accessed via 192.168.12.1




    === "wifi connection-STA mode"

        ???+ note "STA mode"
            
            Need to know the WiFi IP assigned to the chassis and access through this IP

---
## How to Set the Chassis WiFi Operating Mode
<a name="setup_wifi_mode"></a>
Chassis working mode

- AP mode (default)
- STA mode


???+ question "Switching method"

    - AP Mode: Automatically switches to STA mode when connected to any WiFi. If the connection fails, it will automatically switch back to AP mode.
    - STA Mode: Press the power button 10 times consecutively, with each press not exceeding 1 second. This will reset the WiFi mode to AP mode.

---
## Chassis WiFi Connection to Other APs

???+ question "method"

    1. Set the chassis WiFi mode [to AP mode](?h=AP#setup_wifi_mode)
    - [Connect your computer to the chassis hotspot](?h=AP#wifi_ap)
    - Access http://192.168.12.1:8000/wifi_setup via a browser to make modifications
