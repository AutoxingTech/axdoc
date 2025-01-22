# ActionType

任务动作类型

sdk 版本 需不低于 1.0.133

## 枚举

| 值                         | 说明                                                     |
| -------------------------- | -------------------------------------------------------- |
| `ActionType.None`          | 无                                                       |
| `ActionType.PlayAudio`     | 播放声音<br/>[参数](../../Define/ActionData/Define-ActionData-PlayAudio)       |
| `ActionType.OpenDoor`      | 开箱门<br/>[参数](../../Define/ActionData/Define-ActionData-OpenDoor)          |
| `ActionType.CloseDoor`     | 关箱门<br/>[参数](../../Define/ActionData/Define-ActionData-CloseDoor)          |
| `ActionType.Pause`         | 动作暂停<br/>[参数](../../Define/ActionData/Define-ActionData-Pause)           |
| `ActionType.GearOperation` | 喷雾器动作<br/>[参数](../../Define/ActionData/Define-ActionData-GearOperation) |
| `ActionType.StopAudio`     | 停止播放声音<br/>[参数](../../Define/ActionData/Define-ActionData-StopAudio)   |
| `ActionType.OpenLight`     | 打开灯带<br/>[参数](../../Define/ActionData/Define-ActionData-OpenLight)       |
| `ActionType.CloseLight`    | 关闭灯带<br/>[参数](../../Define/ActionData/Define-ActionData-CloseLight)      |
| `ActionType.InterAction`     | 等待交互<br/>[参数](../../Define/ActionData/Define-ActionData-InterAction)    |
| `ActionType.SetSpeed`      | 设置速度<br/>[参数](../../Define/ActionData/Define-ActionData-SetSpeed)       |
| `ActionType.Continue`      | 继续<br/>参数无        |
| `ActionType.JackingUp`     | 顶升-举起<br/>参数无     |
| `ActionType.JackingDown`   | 顶升-放下<br/>参数无     |
| `ActionType.RollerLoad`    | 滚筒-装载 --- 暂未开通 type: 54<br/>参数无       |
| `ActionType.RollerUnLoad`  | 滚筒-卸载 --- 暂未开通 type: 55<br/>参数无    |
| `ActionType.TaskStart`     | 任务开始<br/>[参数](../../Define/ActionData/Define-ActionData-TaskStart)       |
| `ActionType.TaskEnd`       | 任务结束<br/>[参数](../../Define/ActionData/Define-ActionData-TaskEnd)         |

