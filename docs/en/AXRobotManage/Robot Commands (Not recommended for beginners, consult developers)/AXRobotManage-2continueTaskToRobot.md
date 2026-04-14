````markdown
# Continue Task for Specified Robot
## Method

## `continueTaskToRobot(robotId) -> {Promise.<boolean>}`

SDK does not need to connect to the robot. Through this method, you can continue the paused task for a specified robot.

### Parameters

| Name   | Type                          | Description     |
| ------ | ----------------------------- | -------- |
| `robotId` | string | Robot identifier |

### Return Value `Promise.<boolean>`

Whether successful

* `true` - Success
* `false` - Failure

### Example

```javascript
...
const success = await axRobot.continueTaskToRobot(robotId);
...
```




````
