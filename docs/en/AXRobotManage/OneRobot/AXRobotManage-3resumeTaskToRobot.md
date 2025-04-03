# Specify robot resume task
## Method

## `resumeTaskToRobot(robotId） -> {Promise.<boolean>}`

SDK does not require a robot connection, and this method can achieve recovery tasks for a specified robot

### Parameters

| Fields         | Type           | Description            |
| ------ | ----------------------------- | -------- |
| `robotId` | string | robotId |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed

### Example

```javascript
...
const success = await axRobot.resumeTaskToRobot(robotId）;
...
```



