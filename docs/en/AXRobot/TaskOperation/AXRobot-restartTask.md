# Restart Current Task

## Methods

## `restartTask(taskId) -> {Promise.<boolean>}`

Resume a paused or ended task.

### Parameters

| Name | Type | Description |
| -------- | ------ | -------- |
| `taskId` | string | task ID |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.restartTask("<taskId>");
...
```
