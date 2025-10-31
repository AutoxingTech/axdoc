# 连接机器人

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

    === "robotId"
    
        ```typescript
          // 一般用于广域网连接机器人
          ...
          if (初始化成功) {
            try {
              const res = await axRobot.connectRobot({
                  robotId: "<robotId>"
              });
              
              console.log("connect success: " + res.robotId);
              // do something
              } catch(err) {
              console.log(err.errText);
            }
          }

        ```

    === "robotIp" 

        ```typescript
          // 一般用于局域网连接机器人
          ...
          if (初始化成功) {
            try {
              const res = await axRobot.connectRobot({
                  robotIp: "<robotIp>"
              });
              
              console.log("connect success: " + robotIp);
              // do something
              } catch(err) {
              console.log(err.errText);
            }
          }
          
        ```

## ReqConnect  


```typescript
// 连接参数
...
ReqConnect {
    robotId?: string, //  机器人sn： 一般用于广域网连接 robotId和robotIp 二选一
    robotIp?: string, // 机器人IP ： 一般用于局域网连接 robotId和robotIp 二选一
    timeOut?: number // 可选，连接超时时间，单位：秒
}
```

### 示例

???+ Example "ReqConnect"

    === "AppMode.WAN_APP"
        ???+ note 
            广域网：机器人通过4G或wifi连接互联网。robotId 是必填项。


        ```typescript
        // 初始化机器人操作实例
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.WAN_APP)

        try {
            let isOk = await this.axRobot.init()
            //console.log(isOk)
            if (isOk) {
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
            本地：上位机通过机器人底盘有线网连接。

        ```typescript
        // 初始化机器人操作实例
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.LOCAL_APP)

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
            本地：通过机器人底盘wifi ap,连接机器人。

        ```typescript
        // 初始化机器人操作实例
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.LAN_APP) 

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
            局域网：机器人底盘连接局域网。需要更换成机器人底盘在局域网的实际IP

        ```typescript
        // 初始化机器人操作实例
        ...
        this.axRobot = new AXRobot(
            "<appId>", 
            "<appSecret>",
            AppMode.LAN_APP)

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