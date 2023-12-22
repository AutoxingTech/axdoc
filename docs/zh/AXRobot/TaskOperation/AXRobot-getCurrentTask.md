# 获取当前任务

## `getCurrentTask() -> {Promise.<any>}`

获取当前正在执行的任务信息。

### 返回值 `Promise.<any>`

| 名称   | 类型 | 说明     |
| ------ | ---- | -------- |
| `task` | any  | 任务信息 |

### 示例

```javascript
...
let task = await axRobot.getCurrentTask();
console.log(task.isCancel); // 任务是否已取消
console.log(task.runType); // 运行类型；0-定时消杀 1-临时消消杀 20-快捷送餐 21-多点送餐 22-引领 23-巡游 24-返航 25-回桩充电
console.log(task.businessId); // 任务所属业务标识
console.log(task.robotId); // 机器人标识
console.log(task.buildingId); // 楼宇标识
console.log(task.isExcute); // 是否已执行
console.log(task.taskType); // 任务类型；0-消杀  1-回桩充电  2-餐厅
console.log(task.taskPts); // 任务节点信息，具体参考开始执行任务说明
console.log(task.createTime); // 任务创建时间
console.log(task.runNum); // 任务运行次数
console.log(task.name); // 任务名称
console.log(task.busiType); // 业务类型
console.log(task.isDel); // 是否已删除
console.log(task.taskId); // 任务标识
...
```

