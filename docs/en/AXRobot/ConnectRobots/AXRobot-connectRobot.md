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

```typescript
// Initialize robot operation instance
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
            robotId: '8182201xxxx', // Robot SN
            robotIp: '192.168.12.1' // 
        })
    }
} catch (e) {
    console.log(e)
}


```