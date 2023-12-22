# Set Server Info

## `setServerInfos(serverInfo) -> {Promise.<boolean>}`

Set service information for robot connection

### Parameters

| Name  | Data Type | Description |
| ------------ | --------------------------------- | ---------- |
| `serverInfo` | [ServerInfo](../../Define/Define-ServerInfo) | Server Info |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
let serverInfo = {
    ip: "http://127.0.0.1:8080/",
    type: -1,
    offline: 0
}
const success = await axRobot.setServerInfos(serverInfo);
...
```
