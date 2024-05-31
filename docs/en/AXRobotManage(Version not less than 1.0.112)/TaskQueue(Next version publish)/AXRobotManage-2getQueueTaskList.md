# getQueueTaskList

## Method

## `getQueueTaskList(params) -> {Promise.<any>}`

Obtain a task record list (supports pagination), which includes unassigned and assigned tasks, mainly used for querying tasks in the management interface.

### Parameters

| Fields         | Type           | Description            |
| ------ | ----------------------------- | -------- |
| `params` | [RequestQueueTaskParam](../../../Define/Define-RequestQueueTaskParam) | taskInfo |

### Return Value `Promise.<any>`
| Fields         | Type           | Description            |
| ------------ | ---------------------------- | --------------  |
| `count`      | number         | count              |
| `tasks`      | object         | tasks（taskInfo：）            |

taskInfo:

| Fields         | Type           | Description            |
| ------------ | ---------------------------- | --------------  |
| `sn`         | string         | sn                   |
| `taskId`     | string         | taskId                       |
| `businessId` | string         | businessId                |
| `botSn`      | string         | botSn             |
| `content`    | object         | content（task）    |
| `queueWeight`| string         | queueWeight         |
| `createTime` | integer        | createTime  |
| `issueTime`  | integer        | issueTime  |
| `startTime`  | integer        | startTime  |
| `endTime`    | integer        | endTime  |
| `endType`    | string         | endType     |

### Request example

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
### Response data example

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




