# Connect

## `connectRobot(req) -> {Promise}`

Connect the robot

### Parameters

| Name | Data Type | Description |
| ----- | ---------- | -------- |
| `req` | [ReqConnect](#reqconnect) | connection parameters |

### Return value `Promise`

none

### Example
???+ Example "connectRobot"

    ``` javascript
    // Initialize the robot operation instance
    ...
    try {
    const res = await axRobot.connectRobot({
        robotId: "<robotId>"
    });

    console.log("connect success: " + res.robotId);
    // do something
    } catch(err) {
    console.log(err.errText);
    }
    ```

## ReqConnect  


```typescript
...
ReqConnect {
    robotId?: string,
    robotIp?: string,
    timeOut?: number
}
```

### Example
???+ Example "ReqConnect"
    === "AppMode.WAN_APP"
        ???+ note 
            The robot connects to the internet via 4G or wifi. `robotId` is a required field.


        ```typescript
        // Initialize robot operation instance
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.WAN_APP) // dev

        try {
            let isOk = await this.axRobot.init()
            //console.log(isOk)
            if (isOk === true) {
                let res = await this.axRobot.connectRobot({
                    robotId: '81822013xxxx', // Robot SN
                })
            }
        } catch (e) {
            console.log(e)
        }


        ```


    === "AppMode.LOCAL_APP"
        ???+ note 
            The upper computer connects to the robot chassis via a wired connection.

        ```typescript
        // Initialize robot operation instance
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.LOCAL_APP) // dev

        try {
            let isOk = await this.axRobot.init()
            //console.log(isOk)
            if (isOk === true) {
                let res = await this.axRobot.connectRobot({})
            }
        } catch (e) {
            console.log(e)
        }


        ```


    === "AppMode.LAN_APP"
        ???+ note 
            Connect to the robot via the robot chassis WiFi AP.

        ```typescript
        // Initialize robot operation instance
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.LAN_APP) // dev

        try {
            let isOk = await this.axRobot.init()
            //console.log(isOk)
            if (isOk === true) {
                let res = await this.axRobot.connectRobot({})
            }
        } catch (e) {
            console.log(e)
        }


        ```

        ???+ note 
            The robot chassis connects to the local network. Replace with the actual IP of the robot chassis on the local network.

        ```typescript
        // Initialize robot operation instance
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.LAN_APP) // dev

        try {
            let isOk = await this.axRobot.init()
            //console.log(isOk)
            if (isOk === true) {
                let res = await this.axRobot.connectRobot({
                    robotIp: '192.168.0.122' // Actual IP on the local network
                })
            }
        } catch (e) {
            console.log(e)
        }
        ```