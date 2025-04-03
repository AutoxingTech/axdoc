# deleteQueueTask

## Method

## `deleteQueueTask(taskSn) -> {Promise.<boolean>}`

Delete the specified task, which can only be deleted in the assigned state

### Parameters

| Fields         | Type           | Description            |
| ------ | ----------------------------- | -------- |
| `taskSn` | string | taskSn |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed

### Example

```javascript
...
const success = await axRobot.deleteQueueTask(taskSn);
...
```



