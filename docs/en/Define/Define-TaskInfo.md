# TaskInfo

Mission information

## Attributes

| Name | Data Type | Description |
| ---------- | --------------------------------- | ------------------------------------------------------------ |
| `name` | string | task name |
| `robotId` | string | Robot ID |
| `runNum` | number | The number of task executions<br/>The default is 1; 0 means infinite loop |
| `taskType` | number | Task type<br/>0 - disinfecting<br/>1 - Back to the pile charging<br/>2 - Restaurant |
| `runType` | number | Run Type<br/>0 - Scheduled Disinfection<br/>1 - Temporary Disinfection<br/>20 - Express Delivery<br/>21 - Multi-Order Delivery<br/> 22 - Lead<br/>23 - Cruise<br/>24 - Return<br/>25 - Charging Pile |
| `curPt` | [TaskPoint](../../Define/Define-TaskPoint) | Robot current position |
| `taskPts` | [TaskPoint](../../Define/Define-TaskPoint)[] | list of task nodes |
| `backPt` | [TaskPoint](../../Define/Define-TaskPoint) | optional; the node to return after the task ends |
