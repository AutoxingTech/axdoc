# setJackAction

## `setJackAction(type) -> {Promise.<boolean>}`

Set the lifting and lowering actions of the robot

### Parameters

| Name  | Data Type | Description                |
| ---------- |--------|----------------------------|
| `type`     | number | type: 0 jacking 1  go down |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
const success = await axRobot.setJackAction(0);
...
```
