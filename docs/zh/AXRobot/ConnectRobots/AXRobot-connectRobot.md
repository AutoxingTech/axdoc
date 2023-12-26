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
                robotId: '81822013xxxx', // 机器人sn
                robotIp: '192.168.12.1' // 
            })
        }
    } catch (e) {
        console.log(e)
    }


    ```