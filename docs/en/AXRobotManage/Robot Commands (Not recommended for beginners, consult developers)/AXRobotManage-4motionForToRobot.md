````markdown
# Motion Control for Specified Robot
## Method

## `motionForToRobot(type, robotId) -> {Promise.<boolean>}`

SDK does not need to connect to the robot. Through this method, you can control a specified robot.

### Parameters

| Name       | Type                                         | Description         |
| --------- | -----------------------------                | ------------ |
| `type`    | [MotionType](../../Define/Define-MotionType.md) | Motion type      |
| `robotId` | number                                       | Robot identifier    |

### Return Value `Promise.<boolean>`

Whether successful

* `true` - Success
* `false` - Failure

### Example

```javascript
...
const success = await axRobot.motionForToRobot(MotionType.Forward, robotId);
...
```




````
