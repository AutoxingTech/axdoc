# 获取指定机器人的已分配任务列表

## 方法

## `getTaskQueueIssued(businessId, robotSn) -> {Promise.<any>}`

结果中的任务顺序即队列顺序

### 请求参数

| 名称         | 类型                          | 说明     |
| ------------ | ---------------------------- | -------- |
| `businessId` | string                        | 业务标识 |
| `robotSn`    | string                        | 机器人标识 |


### 返回值 `Promise.<any>`

data:

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
let list = await axRobot.getTaskQueueIssued(businessId, robotSn);
...
```
### 响应数据示例

```JSON
...
{
  "status": 200,
  "message": "string",
  "data": [
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
    }
  ]
}
...
```




