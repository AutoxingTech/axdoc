# Subscribe To Task Status

## Methods

## `subscribeTaskState(listener) -> {void}`

Subscribe to task status.

### Parameters

| Name | Type | Description |
| ---------- | ----------------------------------------- | ------------ |
| `listener` | [OnTaskListener](#/Define-OnTaskListener) | task status callback |

### Return value `void`

### Example

```javascript
...
axRobot.startTask({
   onTaskChanged: (state: any) => {
     console.log(state.actType); // task state action type 1000-task start 14-departure 16-arrive 40-wait for interaction 1001-task complete
     console.log(state.data); // specific task status data
   }
});
...
```
