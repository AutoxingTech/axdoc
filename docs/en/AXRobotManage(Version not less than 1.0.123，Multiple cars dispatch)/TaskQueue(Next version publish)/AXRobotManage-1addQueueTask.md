# addQueueTask

## Method

## `addQueueTask(queueTask) -> {Promise.<boolean>}`

A new task will be created and queued for allocation.

### Parameters

| Fields         | Type           | Description            |
| ------ | ----------------------------- | -------- |
| `queueTask` | [QueueTaskInfo](../../../Define/Define-QueueTaskInfo) | QueueTaskInfo |

### Return Value `Promise.<boolean>`

success

* `true` - success
* `false` - failed


### Example

```javascript
...
let queueTask = {
  businessId: "<businessId>",
  botSn: "<robotSn>"
  content: {
    name: "<name>",
    runNum: 1,
    taskType: 2,
    runType: 21,
    pts: [
      {
        x: 0.11,
        y: 1.22,
        yaw: 89, 
        areaId: "xxxxxxxxxxxxxx",
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
}

const success = await axRobot.addQueueTask(queueTask);
...
```



