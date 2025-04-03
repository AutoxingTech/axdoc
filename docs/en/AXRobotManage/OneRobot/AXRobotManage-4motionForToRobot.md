# Specify robot motion control
## Method

## `motionForToRobot(type, robotId） -> {Promise.<boolean>}`

SDK does not require a robot connection, and this method can achieve control over a specified robot

### Parameters

| Fields         | Type           | Description            |
| --------- | -----------------------------                | ------------ |
| `type`    | [MotionType](../../Define/Define-MotionType) | MotionType      |
| `robotId` | number                                       | robotId    |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed

### Example

```javascript
...
const success = await axRobot.motionForToRobot(MotionType.Forward, robotId);
...
```



