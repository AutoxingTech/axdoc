# Connect

## `connectRobot(req) -> {Promise}`

Connect the robot

### Parameters

| Name | Data Type | Description |
| ----- | ---------- | -------- |
| `req` | ReqConnect | connection parameters |

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
