# getTaskQueueRobot

## Method

## `getTaskQueueRobot(businessId, robotSn) -> {Promise.<any>}`

Obtain the exclusive task queue for the specified robot (tasks waiting to be assigned)

### 请求Parameters

| Fields         | Type           | Description            |
| ------------ | ---------------------------- | -------- |
| `businessId` | string                        | businessId |
| `robotSn`    | string                        | robotSn |


### Return Value `Promise.<any>`

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
let list = await axRobot.getTaskQueueRobot(businessId, robotSn);
...
```
### Response data example

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




