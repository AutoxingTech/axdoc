# Set Network Mode

## `setRouteMode(mode) -> {Promise.<boolean>}`

Set Robot Network Mode

### Parameters

| Name  | Data Type | Description |
| ------ | ------ | ------------------------ |
| `mode` | number | Network Mode<br/> 0: Head shell supply network<br/> 1: Chassis wifi network supply<br/> 2: Chassis 4G network supply<br/> 3: Chassis supply network |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
const success = await axRobot.setRouteMode(0);
...
```

