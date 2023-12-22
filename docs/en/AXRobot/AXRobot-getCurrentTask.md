# Get Current Task

## `getCurrentTask() -> {Promise.<any>}`

Get information about the currently executing task.

### Return value `Promise.<any>`

| Name | Type | Description |
| ------ | ---- | -------- |
| `task` | any | task information |

### Example

```javascript
...
let task = await axRobot.getCurrentTask();
console.log(task.isCancel); // Whether the task has been canceled
console.log(task.runType); // run type; 0-timed disinfecting 1-temporary disinfecting 20-fast meal delivery 21-multi-point meal delivery 22-leading 23-cruising 24-returning 25-returning to pile charging
console.log(task.businessId); // The business ID to which the task belongs
console.log(task.robotId); // Robot ID
console.log(task.buildingId); // building ID
console.log(task.isExecute); // Whether it has been executed
console.log(task.taskType); // task type; 0-disinfect 1-recharge pile 2-restaurant
console.log(task.taskPts); // Task node information, please refer to the description of starting the task execution
console.log(task.createTime); // task creation time
console.log(task.runNum); // The number of times the task is run
console.log(task.name); // task name
console.log(task.busiType); // business type
console.log(task.isDel); // Is it deleted
console.log(task.taskId); // task ID
...
```
