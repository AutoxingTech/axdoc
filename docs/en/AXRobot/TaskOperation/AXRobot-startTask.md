# Start Task

## Methods

## `startTask(task) -> {Promise.<boolean>}`

Start the task.

### Parameters

| Name | Type | Description |
| ------ | ----------------------------- | -------- |
| `task` | [TaskInfo](../../../Define/Define-TaskInfo) | task info |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
let task = {
   name: "More Food Delivery",
   runNum: 1,
   taskType: 2,
   runType: 21,
   taskPts: [
     {
       x: 0.11,
       y: 1.22,
       yaw: 89,
       areaId: "xxxxxxxxxxxxxxx",
       type: -1,
       ext: {},
       stepActs: [
         {
           type: ActionType.PlayAudio,
           data: {...}
         },
         ...
       ]
     },
     ...
   ]
}
const success = await axRobot.startTask(task);
...
```
