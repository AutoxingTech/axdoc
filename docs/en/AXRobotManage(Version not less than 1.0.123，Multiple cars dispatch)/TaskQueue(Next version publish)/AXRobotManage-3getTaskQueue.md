# getTaskQueue

## Method

## `getTaskQueue(businessId) -> {Promise.<any>}`

Get the task queue for the specified business (tasks waiting to be assigned)

### Request example


| Fields         | Type           | Description            |
| ------------ | ---------------------------- | -------- |
| `businessId` | string                        | businessId |

### Return Value `Promise.<any>`   
List of task data waiting to be assigned  

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
let list = await axRobot.getTaskQueue(businessId);
...
```
### Response data example

```JSON
...
[
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
...
```




