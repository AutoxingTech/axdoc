# 获取任务记录列表（支持分页）

## 方法

## `getQueueTaskList(params) -> {Promise.<any>}`

列表包括未分配任务和已分配任务，主要用于管理界面查询任务

### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `params` | [RequestQueueTaskParam](../../8.数据定义/Define-RequestQueueTaskParam.md) | 任务信息 |

### 返回值 `Promise.<any>`
| 名称         | 类型            | 说明                          |
| ------------ | ---------------------------- | --------------  |
| `count`      | number         | 符合条件的数据总数              |
| `tasks`      | object         | 任务信息列表（taskInfo如下）            |

taskInfo:

| 名称         | 类型            | 说明                          |
| ------------ | ---------------------------- | --------------  |
| `sn`         | string         | 任务记录标识                   |
| `taskId`     | string         | 任务标识                       |
| `businessId` | string         | 任务所属业务标识                |
| `botSn`      | string         | 执行任务的机器人 SN             |
| `content`    | object         | 任务内容 SN 具体内容业务定义     |
| `queueWeight`| string         | 队列权重 数值越小越靠前          |
| `createTime` | integer        | 任务创建时间  毫秒级 UTC 时间戳  |
| `issueTime`  | integer        | 任务下发时间  毫秒级 UTC 时间戳  |
| `startTime`  | integer        | 任务开始时间  毫秒级 UTC 时间戳  |
| `endTime`    | integer        | 任务结束时间  毫秒级 UTC 时间戳  |
| `endType`    | string         | 任务结束类型 具体内容业务定义     |

### 请求示例

```javascript
...
let params = {
  "pageSize": 10,
  "pageNum": 0,
  "businessId": "<businessId>",
  "botSn": "<botSn>",
  "createTimeRange": [
    0,
    0
  ],
  "issueTimeRange": [
    0
  ],
  "startTimeRange": [
    0
  ],
  "endTimeRange": [
    0
  ],
  "endType": "string",
  "asc": true
}
let result = await axRobot.getQueueTaskList(params);
if (result && result.data) {
  let taskList = result.data.tasks
}
...
```
### 响应数据示例

```JSON
...
{
  "count": 0,
  "tasks": [
    {
      "sn": "string",
      "taskId": "string",
      "businessId": "string",
      "botSn": "string",
      "content": {},
      "queueWeight": "string",
      "createTime": 0,
      "issueTime": 0,
      "startTime": 0,
      "endTime": 0,
      "endType": "string"
    },
    ...
  ]
}
...
```




