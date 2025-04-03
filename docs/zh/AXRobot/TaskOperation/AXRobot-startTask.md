# 开始执行任务

## 方法

## `startTask(task) -> {Promise.<boolean>}`

开始执行任务。

### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `task` | [TaskInfo](../../../Define/Define-TaskInfo) | 任务信息 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
let task = {
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
const success = await axRobot.startTask(task);
...
```



