# 添加任务

## 方法

## `addQueueTask(queueTask) -> {Promise.<boolean>}`

将创建一个新的任务，并进入队列等待分配

### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `queueTask` | [QueueTaskInfo](../../8.数据定义/Define-QueueTaskInfo.md) | 任务信息 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
let queueTask = {
  businessId: "<businessId>",
  botSn: "<robotSn>"
  content: {
    name: "多点送餐",
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



