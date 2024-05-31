# setTaskOrder

## Method

## `setTaskOrder(taskSn, refTaskSn, isFront) -> {Promise.<boolean>}`

Set the order of individual tasks in the queue.

### Parameters

| Fields         | Type           | Description            |
| --------- | ---------------------- | ------------------                        |
| `taskSn`     | string                 | taskSn                      |
| `refTaskSn`  | string                 | refTaskSn      |
| `isFront`    | boolean                | isFront    |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed

### Example

```javascript
...
const success = await axRobot.setTaskOrder(taskSn, refTaskSn, isFront);
...
```



