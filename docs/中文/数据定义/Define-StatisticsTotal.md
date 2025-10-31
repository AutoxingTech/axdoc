# StatisticsTotal

总统计数据信息

## 属性

| 名称        | 数据类型 | 说明                                                                                                                             |
| ----------- | -------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `startTime` | number   | 起始时间,单位：毫秒,以当天的 00:00:00 开始,最长时间为一个月                                                                      |
| `endTime`   | number   | 结束数据,单位：毫秒,以当天的 11:59:59 结束                                                                                       |
| `busIds`    | string[] | 非必填, 业务 id 集合                                                                                                             |
| `deviceIds` | string[] | 非必填, 机器人 sn 集合                                                                                                           |
| `dataItems` | string[] | 所需数据项, <br/>mileage - 总里程<br/>duration - 总时长<br/>taskMileage - 任务里程<br/> taskDuration - 任务时长<br/>chargingCount -  充电次数<br/> errCount - 底盘 error 次数<br/>locerrCount - 定位丢失次数<br/>warnCount - 警告次数<br/>dryBurnCount - 干烧次数<br/>obstructCount - 遇障次数<br/>taskCancelCount - 任务取消次数<br/>taskCount - 任务次数<br/>taskFinishCount - 任务完成次数<br/>taskPauseCount - 任务暂停次数<br/>disinfectCount - 消杀次数<br/>onSprayCount - 打开喷雾次数<br/>sprayMileage - 喷雾里程<br/>remoteCount - 远控次数<br/>low10BatCount - 电量低于 10%次数<br/>low20BatCount - 电量低于 20%次数<br/>emergencyCount - 急停次数<br/>gohomeCount - 回桩次数<br/>manualCount - 手动次数<br/>dispatchCount - 调度次数<br/>modspeedCount - 修改速度次数 |

## 示例

```json
{
  "startTime": 1682870400000,
  "endTime": 1685548799000,
  "dataItems": ["taskDuration","taskMileage","mileage","duration","taskCount"]
}
```
