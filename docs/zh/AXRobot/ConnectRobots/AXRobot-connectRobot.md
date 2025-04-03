# 连接

## `connectRobot(req) -> {Promise}`

连接机器人

### 参数

| 名称  | 数据类型   | 说明     |
| ----- | ---------- | -------- |
| `req` | [ReqConnect](#reqconnect) | 连接参数 |

### 返回值 `Promise`

无

### 示例

???+ Example "connectRobot" 
    ```typescript
    // 初始化机器人操作实例
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
// 初始化机器人操作实例
...
ReqConnect {
    robotId?: string,
    robotIp?: string,
    timeOut?: number
}
```

### 示例

???+ Example "ReqConnect"

    === "AppMode.WAN_APP"
        ???+ note 
            机器人通过4G或wifi连接互联网。robotId 是必填项。


        ```typescript
        // 初始化机器人操作实例
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
                    robotId: '81822013xxxx', // 机器人sn
                })
            }
        } catch (e) {
            console.log(e)
        }


        ```

    
    === "AppMode.LOCAL_APP"
        ???+ note 
            上位机通过机器人底盘有线网连接。

        ```typescript
        // 初始化机器人操作实例
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
            通过机器人底盘wifi ap,连接机器人。

        ```typescript
        // 初始化机器人操作实例
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
            机器人底盘连接局域网。需要更换成机器人底盘在局域网的实际IP

        ```typescript
        // 初始化机器人操作实例
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
                    robotIp: '192.168.0.122' // 局域网的实际IP
                })
            }
        } catch (e) {
            console.log(e)
        }
        ```