# Update Current Task

## `updateTask(taskId, pts) -> {Promise.<boolean>}`

Update tasks.

### Parameters

| Name | Type | Description |
| -------- | ------ | --------------------------------------------- |
| `taskId` | string | task ID |
| `pts` | Array | List of task points; refer to the `taskPts` parameter for starting a task |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...

const success = await axRobot.updateTask("<taskId>", <pts>);
...
```
