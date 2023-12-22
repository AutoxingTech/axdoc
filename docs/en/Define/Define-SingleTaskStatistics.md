# SingleTaskStatistics

Single Task Statistics Info

## Attributes

| Name | Data Type | Description |
| -------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `taskId` | string   | task Id                                                                                                                                                                                                          |
| `fields` | string[] | Required data items<br/>mileage<br/>cStartTime<br/>cEndTime<br/>disinfect<br/>taskFinishCount<br/>taskPauseCount<br/>taskCancelCount |

## Example

```json
{
  "taskId": "322751f4-1c00-45c2-bcf3-0e42aa9fa2c4",
  "fields": [
    "cStartTime",
    "cEndTime",
    "mileage",
    "disinfect",
    "taskCancelCount",
    "errCount",
    "taskFinishCount",
    "taskPauseCount"
  ]
}
```
