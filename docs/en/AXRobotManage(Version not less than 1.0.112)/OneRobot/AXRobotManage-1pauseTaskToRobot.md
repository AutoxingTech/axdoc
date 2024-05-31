# Specify robot pause task
## Method

## `pauseTaskToRobot(robotId） -> {Promise.<boolean>}`

SDK does not require a connection to a robot, and this method can be used to pause the executing task of a specified robot

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
const success = await axRobot.pauseTaskToRobot(robotId）;
...
```



