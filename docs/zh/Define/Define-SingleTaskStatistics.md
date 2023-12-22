# SingleTaskStatistics

单任务统计信息

## 属性

| 名称     | 数据类型 | 说明                                                                                                                                                                                                             |
| -------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `taskId` | string   | 任务 id                                                                                                                                                                                                          |
| `fields` | string[] | 所需数据项<br/>mileage - 里程<br/>cStartTime - 起始时间<br/>cEndTime - 结束时间<br/>disinfect - 消杀详情<br/>taskFinishCount - 任务完成次数<br/>taskPauseCount - 任务暂停次数<br/>taskCancelCount - 任务取消次数 |

## 示例

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
