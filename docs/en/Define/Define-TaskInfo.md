# TaskInfo

Mission information

## Attributes

| Name | Data Type                                    | Description                                                                                                                                                                                          |
| ---------- |----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | string                                       | task name                                                                                                                                                                                            |
| `robotId` | string                                       | Robot ID                                                                                                                                                                                             |
| `routeMode`        | number  | 1 Route calculation by sequence of task points, 2 Route calculation by shortest path. Default is 1.                                                                                       |
| `runMode`          | number  | 1 Flexible obstacle avoidance, 2 Travel according to track. Default is 1. 3 Strictly follow track.                                                                                          |
| `detourRadius` | number | 0 No obstacle avoidance, 1: Obstacle avoidance radius of 1 meter.
| `ignorePublicSite` | boolean | Whether to ignore public sites, default is false.                                                                                                                                              |
| `runNum`           | number  | Number of task executions. Default is 1; 0 indicates infinite loop.                                                                                                                           |
| `taskType`         | number  | Task type: 0 - Disinfection, 1 - Return to charging station, 2 - Restaurant, 3 - Hotel, 4 - Delivery (Five-in-one), 5 - Factory, 6 - Chassis mini program.                                                                                                   |
| `runType`          | number  | Run type: 0 - Scheduled disinfection, 1 - Ad hoc disinfection, 20 - Quick meal delivery, 21 - Multi-point meal delivery, 22 - Guidance, 23 - Patrol, 24 - Return, 25 - Charging station, 26 - Summon, 27 - Restaurant birthday mode task, 28 - Guidance, 29 - Lifting task, 30 - Lifting Patrol, 31 - Flexible handling, 32 - Roller task.| `runNum` | number                                       | The number of task executions<br/>The default is 1; 0 means infinite loop                                                                                                                            |
| `curPt` | [TaskPoint](../../Define/Define-TaskPoint)   | Robot current position                                                                                                                                                                               |
| `pts` | [TaskPoint](../../Define/Define-TaskPoint)[] | list of task nodes                                                                                                                                                                                   |
| `backPt` | [TaskPoint](../../Define/Define-TaskPoint)   | optional; the node to return after the task ends                                                                                                                                                     |
