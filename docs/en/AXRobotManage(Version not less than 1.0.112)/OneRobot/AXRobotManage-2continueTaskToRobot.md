# Specify robot continue task
## Method

## `continueTaskToRobot(robotId） -> {Promise.<boolean>}`

SDK does not require a connection to a robot, and this method allows for the continuation of a paused task for a specified robot

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
const success = await axRobot.continueTaskToRobot(robotId）;
...
```



