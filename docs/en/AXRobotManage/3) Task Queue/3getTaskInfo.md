````markdown
# Get Task Details

## Method (Version: 1.0.138 and above)

## `getQueueTaskDetails(taskId, needDetail) -> {Promise.<any>}`

Get task details by task ID

### Parameters

| Name         | Type    | Description     |
| ------------ | -------| -------- |
| `taskId` | string |  Task ID |
| `needDetail` | boolean |  Whether detailed information is needed, default false <BR/>false or not passed: returns brief information<BR/>true: returns detailed information (including task points, actions, etc.)<BR/>Version: 1.0.139 and above|

### Return Value `Promise.<any>`

Task details

| Name         | Type           | Description            |
| ------------ | ------------- | --------------  |
| `taskId` | string |  Task identifier |
| `taskType` | integer |  Task type<BR/>0 Disinfection<BR/>1 Return to charging station<BR/>2 Restaurant<BR/>3 Hotel<BR/>4 Delivery (5-in-1)<BR/>5 Factory<BR/>6 Chassis mini program<BR/>7 Charging scheduling |
| `creatorName` | string |  Task creator name |
| `taskStatus` | integer |  Task status code<BR/>-1 Unknown status<BR/>0 Pending assignment (queue task only)<BR/>1 Assigned pending execution<BR/>2 Executing<BR/>3 Paused<BR/>4 Completed<BR/>5 Cancelled (cancelled before execution)<BR/>6 Cancelled (cancelled during execution)<BR/>7 Cancelled (cancelled while pending assignment, queue task only)<BR/>8 Failed |
| `taskStatusName` | string |  Task status name (Chinese)<BR/>Unknown<BR/>Pending assignment<BR/>Assigned pending execution<BR/>Executing<BR/>Paused<BR/>Completed<BR/>Cancelled (before execution)<BR/>Cancelled (during execution)<BR/>Cancelled (pending assignment)<BR/>Failed |
| `taskStatusNameEN` | string |  Task status name (English)<BR/>unknown<BR/>waiting_assign<BR/>pending<BR/>running<BR/>paused<BR/>completed<BR/>cancelled_before_exec<BR/>cancelled_during_exec<BR/>cancelled_waiting<BR/>failed |
| `businessId` | string |  Business identifier |
| `robotId` | string |  Robot identifier for task execution |
| `createTime` | integer |  Task creation time, unit: milliseconds |
| `updateTime` | integer |  Task update time, unit: milliseconds |
| `issueTime` | integer |  Task issue time, unit: milliseconds |
| `startTime` | integer |  Task start execution time, unit: milliseconds |
| `endTime` | integer |  Task end time, unit: milliseconds |
| `endType` | string |  Task end type<BR/>success Completed successfully<BR/>cancel Cancelled<BR/>error Abnormal termination |
| `dispatchType` | integer |  Dispatch type<BR/>0 No dispatch (normal task)<BR/>1 RCS dispatch<BR/>2 Queue task |
| `sourceType` | integer |  Task source type<BR/>0 Unknown source<BR/>1 Head shell APP<BR/>2 Chassis mini program<BR/>3 Caller<BR/>4 Chassis<BR/>5 Dispatch<BR/>6 Secondary development<BR/>7 Tablet APP |



### Request Example

```javascript
...
try {
  const res = await this.axRobot.getQueueTaskDetails(this.taskId)
  console.log('getQueueTaskDetails Success:', res)
} catch (error) {
  console.log('getQueueTaskDetails Error:', error)
}
...
```





````
