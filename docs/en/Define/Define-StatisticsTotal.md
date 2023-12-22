# StatisticsTotal

Statistics Total Info

## Attributes

| Name | Data Type | Description |
| ----------- | -------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `startTime` | number   | Start time, unit: milliseconds, starting at 00:00:00 of the current day, and the maximum time is one month |
| `endTime`   | number   | End data, unit: millisecond, end at 11:59:59 of the current day                  |
| `busIds`    | string[] | Optional, business ids                                                                                                             |
| `deviceIds` | string[] | Optional, robot sn collection                                                                                                           |
| `dataItems` | string[] | Required data items <br/>mileage<br/>duration<br/>taskMileage<br/> taskDuration<br/>chargingCount<br/> errCount<br/>locerrCount<br/>warnCount<br/>dryBurnCount<br/>obstructCount<br/>taskCancelCount<br/>taskCount<br/>taskFinishCount<br/>taskPauseCount<br/>disinfectCount<br/>onSprayCount<br/>sprayMileage<br/>remoteCount<br/>low10BatCount<br/>low20BatCount<br/>emergencyCount<br/>gohomeCount<br/>manualCount<br/>dispatchCount<br/>modspeedCount |

## Example

```json
{
  "startTime": 1682870400000,
  "endTime": 1685548799000,
  "dataItems": ["taskDuration","taskMileage","mileage","duration","taskCount"]
}
```
