# TaskRequestParam

请求参数

## 属性

| 名称                | 数据类型    | 是否必须 | 说明                                               | 
| ------------------- | -------- - | ------- | -------------------------------------------------- |
| `pageNum`           | number     | 是      | 当前第几页                                          |
| `pageSize`          | number     | 是      | 当前页需要多少数据，最大200条                         |
| `busiIds`           | Array      | 是      | 业务id列表                                          |
| `robotId`           | number     | 否      | 机器人ID                                            |
| `executeStatus`     | number     | 否      | 1 等待 2 运行中 3 历史任务                           |
| `orderField`        | number     | 否      | 1 创建时间 2 sortNo 默认是1                          |
| `orderType`         | number     | 否      | -1 降序 1 升序 默认 -1                               |
| `dataItems`         | Array      | 否      | 查询结果需要输出的字段                                |
| `isTaskStatic`      | Boolean    | 否      | 是否启动统计查询                                     |
| `fields`            | Array      | 否      | 统计输出的字段                                       |



