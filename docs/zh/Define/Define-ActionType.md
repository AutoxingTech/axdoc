# ActionType

任务动作类型

sdk 版本 需不低于 1.0.133

## 枚举

| 值                          | 说明                                                                         |
|----------------------------|----------------------------------------------------------------------------|
| `ActionType.None`          | 0:无                                                                        |
| `ActionType.Changemap`     | 4:切换地图<br/>参数无                                                             |
| `ActionType.PlayAudio`     | 5:播放声音<br/>[参数](../../Define/ActionData/Define-ActionData-PlayAudio)       |
| `ActionType.OpenDoor`      | 6:开箱门<br/>[参数](../../Define/ActionData/Define-ActionData-OpenDoor)         |
| `ActionType.CallAutoDoor`  | 8:呼自动门<br/>参数无                                                             |
| `ActionType.CallGate`      | 8:呼闸机 <br/>参数无                                                             |
| `ActionType.GoTo`          | 14:前往目的地 <br/>参数无                                                          |
| `ActionType.Arrive`        | 16:到达目的地 <br/>参数无                                                          |
| `ActionType.Charge`        | 17:回桩 <br/>参数无                                                             |
| `ActionType.CloseDoor`     | 28:关箱门<br/>[参数](../../Define/ActionData/Define-ActionData-CloseDoor)       |
| `ActionType.Pause`         | 18:动作暂停<br/>[参数](../../Define/ActionData/Define-ActionData-Pause)          |
| `ActionType.GearOperation` | 32:喷雾器动作<br/>[参数](../../Define/ActionData/Define-ActionData-GearOperation) |
| `ActionType.StopAudio`     | 36:停止播放声音<br/>[参数](../../Define/ActionData/Define-ActionData-StopAudio)    |
| `ActionType.OpenLight`     | 37:打开灯带<br/>[参数](../../Define/ActionData/Define-ActionData-OpenLight)      |
| `ActionType.CloseLight`    | 38:关闭灯带<br/>[参数](../../Define/ActionData/Define-ActionData-CloseLight)     |
| `ActionType.InterAction`   | 40:等待交互<br/>[参数](../../Define/ActionData/Define-ActionData-InterAction)    |
| `ActionType.SetSpeed`      | 41:设置速度<br/>[参数](../../Define/ActionData/Define-ActionData-SetSpeed)       |
| `ActionType.Continue`      | 42:继续<br/>参数无                                                              |
| `ActionType.JackingUp`     | 47:顶升-举起<br/>参数无                                                           |
| `ActionType.JackingDown`   | 48:顶升-放下<br/>参数无                                                           |
| `ActionType.RollerLoad`    | 54:滚筒-装载<br/>参数无                                                           |
| `ActionType.RollerUnLoad`  | 55:滚筒-卸载<br/>参数无                                                           |
| `ActionType.TaskStart`     | 1000:任务开始<br/>[参数](../../Define/ActionData/Define-ActionData-TaskStart)    |
| `ActionType.TaskEnd`       | 1001:任务结束<br/>[参数](../../Define/ActionData/Define-ActionData-TaskEnd)      |
| `ActionType.WheelOverload` | 1002:滚筒过载<br/>参数无                                                          |

