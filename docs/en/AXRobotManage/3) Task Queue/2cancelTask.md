````markdown
# Cancel Task

## Method (Version: 1.0.138 and above)

## `cancelQueueTaskById(taskId) -> {Promise.<Boolean>}`

Cancel queue task by task ID

### Parameters

| Name         | Type    | Description     |
| ------------ | -------| -------- |
| `taskId` | string |  Task ID |

### Return Value `Promise.<Boolean>`




### Request Example

```javascript
...
try {
  const res =await this.axRobot.cancelQueueTaskById(this.taskId)
  console.log('cancelQueueTaskById Success:', res)
  // cancelTaskV3 Success: true
} catch (error) {
  console.log('cancelQueueTaskById Error:', error)
}
...
```

### Response Data Example

```JSON
...
true or false
...
```



````
