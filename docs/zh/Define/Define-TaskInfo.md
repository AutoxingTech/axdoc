# TaskInfo

任务信息

## 属性

| 名称       | 数据类型                          | 说明                                                                                                                                                           |
| ---------- | --------------------------------- |--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name`     | string                            | 任务名称                                                                                                                                                         |
| `routeMode` | number                                       | 1按任务点顺序算路,2按最短路径算路 默认为1                                                                                                                                      |
| `runMode` | number                                       | 1 灵活躲避障碍 4 按轨迹行驶  默认为1 4严格按轨道                                                                                                                                |
| `detourRadius` | number                                       | 0 不避障  1:避障半径1米                                                                                                                               |
| `ignorePublicSite` | boolen                                       | /是否忽略公共站点,默认是不忽略                                                                                                                                             
| `robotId`  | string                            | 机器人标识                                                                                                                                                        |
| `runNum`   | number                            | 任务执行次数<br/>默认为1；0 表示无限循环                                                                                                                                     |
| `taskType` | number                            | 任务类型：默认-1<br/>0 - 消杀<br/>1 - 回桩充电<br/>2 - 餐厅 <br/>3 酒店<br/> 4 送物(五合一)<br/> 5 工厂 <br/> 6 底盘小程序                                                                     |
| `runType`  | number                            | 运行类型<br/>0 定时消杀<br/>1 临时消杀<br/>20 快捷送餐<br/>21 多点送餐<br/>22 直达<br/>23 巡游<br/>24 返航<br/>25 回桩<br/>26召唤<br/>27 餐厅生日模式任务<br/>28引领<br/>29顶升任务<br/>30顶升迅游<br/>31灵活搬运<br/>32辊筒任务 |
| `curPt`    | [TaskPoint](../../Define/Define-TaskPoint)   | 机器人当前位置                                                                                                                                                      |
| `pts`  | [TaskPoint](../../Define/Define-TaskPoint)[] | 任务节点列表                                                                                                                                                       |
| `backPt`   | [TaskPoint](../../Define/Define-TaskPoint)   | 可选；任务结束后返回的节点                                                                                                                                                |























