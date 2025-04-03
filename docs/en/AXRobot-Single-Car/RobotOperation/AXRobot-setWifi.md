# Set Wifi

## `setWifi(ssId, password) -> {Promise.<boolean>}`

Set robot chassis wifi

### Parameters

| Name  | Data Type | Description |
| ---------- | ------ | ------- |
| `ssId`     | string | wifi name |
| `password` | string | password    |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example

```javascript
...
const success = await axRobot.setWifi("test-wifi", "123456");
...
```
