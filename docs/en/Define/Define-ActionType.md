# ActionType

Task Action Type

## Enum

| Value | Description                                                                                    |
| -------------------------------------- |------------------------------------------------------------------------------------------------|
| `ActionType.None` | 0:None                                                                                         |
| `ActionType.Changemap`     | 4:Switch map<br/>No parameters                                                                           |
| `ActionType.PlayAudio` | 5:Play sound<br/>[parameters](../../Define/ActionData/Define-ActionData-PlayAudio)             |
| `ActionType.OpenDoor` | 6:OpenDoor<br/>[parameters](../../Define/ActionData/Define-ActionData-OpenDoor)                |
| `ActionType.CallAutoDoor`  | 8:Automatic door<br/>No parameters                                                                       |
| `ActionType.CallGate`      | 8:fare gate  <br/>No parameters                                                                          |
| `ActionType.GoTo`          | 14:Head to the destination <br/>No parameters                                                            |
| `ActionType.Arrive`        | 16:arrive at the destination <br/>No parameters                                                          |
| `ActionType.Charge`        | 17:pile return charging <br/>No parameters                                                               |
| `ActionType.CloseDoor`     | 28:Close the box door<br/>[parameters](../../Define/ActionData/Define-ActionData-CloseDoor)            |
| `ActionType.Pause` | 18:Action Pause<br/>[parameter](../../Define/ActionData/Define-ActionData-Pause)               |
| `ActionType.GearOperation` | 32:sprayer action<br/>[parameters](../../Define/ActionData/Define-ActionData-GearOperation)    |
| `ActionType.StopAudio` | 36:stop playing sound<br/>[parameter](../../Define/ActionData/Define-ActionData-StopAudio)     |
| `ActionType.OpenLight` | 37:Open the light strip<br/>[parameters](../../Define/ActionData/Define-ActionData-OpenLight)  |
| `ActionType.CloseLight` | 38:Close the light strip<br/>[parameter](../../Define/ActionData/Define-ActionData-CloseLight) |
| `ActionType.InterAction`   | 40:Waiting for interaction<br/>[parameters](../../Define/ActionData/Define-ActionData-InterAction)     |
| `ActionType.SetSpeed`      | 41:Set Speed<br/>[parameters](../../Define/ActionData/Define-ActionData-SetSpeed)                      |
| `ActionType.Continue`      | 42:Continue<br/>No parameters                                                                            |
| `ActionType.JackingUp`     | 47:Jacking up<br/>No parameters                                                                          |
| `ActionType.JackingDown`   | 48:Jacking down<br/>No parameters                                                                        |
| `ActionType.RollerLoad`    | 54:Roller Load<br/>No parameters                                                                               |
| `ActionType.RollerUnLoad`  | 55:Roller Unload<br/>No parameters                                                                               
| `ActionType.TaskStart` | 1000:task start<br/>[parameters](../../Define/ActionData/Define-ActionData-TaskStart)          |
| `ActionType.TaskEnd` | 1001:task end<br/>[parameter](../../Define/ActionData/Define-ActionData-TaskEnd)               |
| `ActionType.WheelOverload` | 1002:Roller Overload<br/>No parameters                                                                              | 
