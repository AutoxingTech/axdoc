# RequestQueueTaskParam

请求参数

## 属性

| 名称         | 数据类型                            | 说明                                               |
| ------------ | ----------------------------------- | -------------------------------------------------- |
| `pageNum`    | number                              | 当前页码  默认为 1                                       |
| `pageSize`   | number                              | 可每页记录数                                     |
| `businessId` | string                              | 业务Id 省略将返回所有业务的任务                                 |
| `botSn`      | string                              | 机器人sn 省略将不对特定机器人进行过滤 |
| `createTimeRange`| Array<number> | 任务创建时间范围  格式为毫秒级 UTC 时间戳                                 |
| `issueTimeRange` | Array<number>                   | 任务下发到机器人的时间范围 格式为毫秒级 UTC 时间戳                                 |
| `startTimeRange` | Array<number>                   | 任务开始时间 格式为毫秒级 UTC 时间戳                                         |
| `endTimeRange`   | Array<number>                   | 任务结束时间范围 格式为毫秒级 UTC 时间戳                                     |
| `endType`    | string                              | 任务结束类型标识                                 |
| `asc`        | boolean                             | 列表是否按创建时间升序 默认为 false，按创建时间降序 |

